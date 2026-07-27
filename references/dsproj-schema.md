# Ato 2 — Gerar a camada de texto (.dsproj.json)

Ao fim da entrevista, produza **dois arquivos** (se não puder escrever arquivos, entregue no chat):

1. **`brand-brief.md`** — resumo da marca + **as referências e o porquê de cada uma** (o designer usa nas decisões visuais). Seções: identidade, posicionamento, público, personalidade/manifesto, voz & tom, diferenciais, Referências.
2. **`<Marca>.dsproj.json`** — projeto pro Design System Builder, **só campos de texto**.

## Schema (preencha só o texto)

```json
{
  "_type": "v4-design-system-project",
  "_v": "3.4",
  "fields": {
    "clientName": "", "setor": "", "cidade": "", "foco": "",
    "posicionamento": "", "naoParece": "", "manifesto": "",
    "persona1": "", "persona2": "",
    "tomVoz": "", "palavrasSim": "", "palavrasNao": "",
    "ctaPadrao": "", "canalConversao": ""
  },
  "pillars": [], "difere": [],
  "S": { "hasMascote": false }
}
```

## Regras
- Preencha: `clientName, setor, cidade, foco, posicionamento, naoParece, manifesto, persona1, persona2, tomVoz, palavrasSim` (vírgula), `palavrasNao` (vírgula), `ctaPadrao, canalConversao`; os arrays `pillars` (3-4) e `difere` (até 3). Personas e manifesto em texto corrido.
- **`_type` deve ser exatamente `v4-design-system-project`.** JSON válido, nome do arquivo sem espaços.
- ⚠️ **O objeto `S` deve ter APENAS `hasMascote`.** NUNCA inclua `colors`, `fontH`, `mood`, `radius` nem qualquer chave de design — o designer faz a parte visual no builder. Incluir `colors` (mesmo vazio) faz o builder falhar.
- **Nunca invente hex, fonte ou tom visual.** Cor e fonte são do designer, não seus.

## Entrega
Diga: "Pronto! Abra o builder em `https://gabrielaraujo21.github.io/design-system-builder/` → 1ª etapa → **📂 Abrir projeto salvo** → selecione este `.dsproj.json`. Os textos já entram; agora é a parte do designer (cores, fontes, tokens). No fim, exporte o Design System e o Prompt Lovable."

Depois vá ao **Ato 3**: pergunte se a pessoa tem a copy da landing page.
