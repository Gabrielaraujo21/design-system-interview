# Ato 2 — Gerar a camada de texto (.dsproj.json)

Ao fim da entrevista, produza **dois arquivos** (se não puder escrever arquivos, entregue o conteúdo no chat para a pessoa salvar):

1. **`brand-brief.md`** — resumo legível da marca + **as referências e o porquê de cada uma** (o designer usa isso nas decisões visuais). Seções: identidade, posicionamento, público, personalidade/manifesto, voz & tom, diferenciais, e **Referências** (cada link + o que emprestar dele).
2. **`<NomeDaMarca>.dsproj.json`** — projeto para o Design System Builder, **só campos de texto**.

## Schema (preencha só o texto; deixe o design no padrão)

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
    "logoNota": "", "typo-display": "", "typo-h1": "", "typo-h2": "",
    "typo-body": "", "typo-caption": "", "typo-cta": "", "fotoDesc": "",
    "mascoteNome": "", "mascoteEspecie": "", "mascotePersonalidade": ""
  },
  "selects": { "fotoEstilo": "", "fotoLuz": "", "scaleBase": "15", "scaleRatio": "1.25" },
  "pillars": [], "difere": [],
  "ruleGood": [], "ruleBad": [], "checkItems": [],
  "S": { "hasMascote": false }
}
```

## Você PREENCHE (texto)

`clientName, setor, cidade, foco, posicionamento, naoParece, manifesto, persona1, persona2, tomVoz, palavrasSim (vírgula), palavrasNao (vírgula), ctaPadrao, canalConversao`; os arrays `pillars` (3-4) e `difere` (até 3); opcional `fotoDesc`, `ruleGood`, `ruleBad`; e `S.hasMascote` (`true` só se a marca já tem mascote). Personas e manifesto em **texto corrido** dentro da string.

## Você NÃO toca (design — é do designer humano)

Cores, fontes, `typo-*`, `mood`, `radius`, `shadow`, `motion`, `btnStyle`, `dsBg`, logo, `fotoEstilo`, `fotoLuz`. Deixe fora do objeto `S` tudo que for design — o loader do builder faz `Object.assign` e mantém os defaults. **Nunca invente hex, nome de fonte ou tom visual.**

## Validação
- `_type` = exatamente `"v4-design-system-project"` (senão o builder recusa).
- JSON válido (sem vírgula sobrando). Nome do arquivo sem espaços (use `_`).

## Entrega
Diga: "Pronto! Abra o Design System Builder em `https://gabrielaraujo21.github.io/design-system-builder/` → 1ª etapa → **📂 Abrir projeto salvo** → selecione este `.dsproj.json`. Os textos já entram preenchidos; agora é a parte do designer: cores, fontes e tokens. Ao terminar, exporte o Design System e o Prompt Lovable na etapa Revisão."

Depois siga para o **Ato 3**: pergunte se a pessoa tem a copy da landing page.
