# Schema do `.dsproj.json` (Design System Builder v3)

O Design System Builder carrega um projeto pela 1ª etapa → **📂 Abrir projeto salvo**. O arquivo precisa ter a estrutura abaixo. O validador do builder só exige `"_type": "v4-design-system-project"` — o resto é preenchido conforme disponível, e o que faltar fica no padrão.

Sua tarefa: preencher **apenas os campos de texto** e deixar o design intocado. Comece de `assets/project-template.dsproj.json` e substitua os valores.

## Estrutura completa

```json
{
  "_type": "v4-design-system-project",
  "_v": "3.4",
  "fields": {
    "clientName": "", "setor": "", "cidade": "", "foco": "",
    "posicionamento": "", "naoParece": "",
    "manifesto": "",
    "persona1": "", "persona2": "",
    "tomVoz": "", "palavrasSim": "", "palavrasNao": "",
    "ctaPadrao": "", "canalConversao": "",
    "logoNota": "",
    "typo-display": "", "typo-h1": "", "typo-h2": "",
    "typo-body": "", "typo-caption": "", "typo-cta": "",
    "fotoDesc": "",
    "mascoteNome": "", "mascoteEspecie": "", "mascotePersonalidade": ""
  },
  "selects": { "fotoEstilo": "", "fotoLuz": "", "scaleBase": "15", "scaleRatio": "1.25" },
  "pillars": [], "difere": [],
  "ruleGood": [], "ruleBad": [],
  "checkItems": [],
  "S": { "hasMascote": false }
}
```

## O que VOCÊ preenche (camada de texto)

| Campo | Vem de | Observação |
|---|---|---|
| `fields.clientName` | Fase 1 | nome da marca |
| `fields.setor` | Fase 1 | |
| `fields.cidade` | Fase 1 | |
| `fields.foco` | Fase 1 | |
| `fields.posicionamento` | Fase 1 | 1 frase |
| `fields.naoParece` | Fase 4 | "nunca deve parecer…" |
| `fields.manifesto` | Fase 4 | 2-3 frases que você redigiu e a pessoa aprovou |
| `fields.persona1` | Fase 3 | nome, idade, dor, desejo em texto corrido |
| `fields.persona2` | Fase 3 | opcional; deixe `""` se não houver |
| `fields.tomVoz` | Fase 5 | tom em 1 frase |
| `fields.palavrasSim` | Fase 5 | separadas por vírgula |
| `fields.palavrasNao` | Fase 5 | separadas por vírgula |
| `fields.ctaPadrao` | Fase 5 | |
| `fields.canalConversao` | Fase 5 | ex.: "WhatsApp" |
| `pillars` | Fase 4 | array de 3-4 strings |
| `difere` | Fase 6 | array de até 3 strings |
| `fields.fotoDesc` | Fase 7 | opcional |
| `ruleGood` / `ruleBad` | Fase 7 | opcional; arrays de strings |
| `S.hasMascote` | — | `true` só se a marca já tem mascote definido; senão `false` |

## O que você NÃO toca (camada de design — é do designer humano)

Deixe **fora** do seu JSON, ou nos valores do template, para o builder usar o padrão:

- `S.colors`, `S.fontH`, `S.fontB` — cores e fontes
- `S.mood` (tom visual), `S.radius`, `S.shadow`, `S.motion`
- `S.btnStyle`, `S.dsBg`, `S.logos`, `S.logoNames`, `S.logoBg`, `S.logoExtra`, `S.icons`
- `fields.typo-*` — hierarquia tipográfica (o designer gera pela escala modular)
- `selects.fotoEstilo`, `selects.fotoLuz` — o designer escolhe

Deixar esses campos de fora do objeto `S` é o correto: o loader faz `Object.assign` e mantém os defaults do builder para tudo que você não enviar. **Nunca invente um hex, um nome de fonte ou um tom visual.** Referências viram decisão visual na mão do designer, não na sua.

## Regras de validação

1. `_type` = exatamente `"v4-design-system-project"`, senão o builder recusa.
2. JSON válido (sem vírgula sobrando, aspas corretas). Cheque antes de entregar.
3. Nome do arquivo: `<NomeDaMarca>.dsproj.json` (sem espaços; use `_`).
4. Personas e manifesto vão em **texto corrido** dentro da string, não em sub-objetos.

## Exemplo preenchido (só texto)

```json
{
  "_type": "v4-design-system-project",
  "_v": "3.4",
  "fields": {
    "clientName": "Café Aurora",
    "setor": "Cafeteria artesanal de bairro",
    "cidade": "Curitiba, PR",
    "foco": "Cafés especiais, brunch e confeitaria própria",
    "posicionamento": "A cafeteria que trata café especial sem frescura — quente, acolhedora e do bairro",
    "naoParece": "Franquia genérica de shopping; cafeteria hipster inacessível; padaria comum",
    "manifesto": "O Café Aurora nasceu de uma ideia simples: café especial não precisa de cerimônia. A gente serve o melhor grão da cidade no balcão de bairro, com nome no copo e prosa no balcão.",
    "persona1": "Marina, 34 — designer em home office no bairro. Dor: cafeterias bonitas mas caras e esnobes. Desejo: um lugar de bairro pra trabalhar e ser reconhecida pelo nome.",
    "persona2": "Seu Antônio, 61 — vizinho aposentado. Dor: acha 'café gourmet' frescura. Desejo: um cafezinho bom, preço justo e prosa.",
    "tomVoz": "Fala como um amigo que entende de café — caloroso, direto, sem jargão de barista.",
    "palavrasSim": "vem tomar um café, do bairro, feito na hora, nosso grão, de casa",
    "palavrasNao": "gourmet, premium, experiência sensorial, exclusivo, mixologia",
    "ctaPadrao": "Vem tomar um café",
    "canalConversao": "WhatsApp",
    "logoNota": "", "typo-display": "", "typo-h1": "", "typo-h2": "",
    "typo-body": "", "typo-caption": "", "typo-cta": "", "fotoDesc": "",
    "mascoteNome": "", "mascoteEspecie": "", "mascotePersonalidade": ""
  },
  "selects": { "fotoEstilo": "", "fotoLuz": "", "scaleBase": "15", "scaleRatio": "1.25" },
  "pillars": ["Acolhedor", "Artesanal", "Especialista", "De bairro"],
  "difere": ["Torra própria toda semana", "Confeitaria de fermentação natural feita na casa", "4,9 estrelas em 800+ avaliações"],
  "ruleGood": [], "ruleBad": [], "checkItems": [],
  "S": { "hasMascote": false }
}
```
