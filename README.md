# Design System Interview — Skill V4

Uma skill que **entrevista você sobre a marca** e transforma as respostas na **camada de texto** de um design system (manifesto, personas, tom de voz, palavras da marca, diferenciais, CTA). Ela exporta um arquivo `.dsproj.json` pronto para carregar no **Design System Builder v3** — onde o designer completa a parte visual (cores, fontes, tokens) — e, ao final, monta o **Prompt Lovable** para gerar a landing page a partir da sua copy.

> **Filosofia:** a skill cuida do **texto**; o designer humano cuida do **design**. E nada acontece sem **referências** — são elas que traduzem gosto em decisão visual.

## O que ela faz, em 3 atos

1. **Entrevista** de marca guiada, com foco em referências obrigatórias.
2. **Exporta** `brand-brief.md` (resumo + referências) e `<Marca>.dsproj.json` (texto preenchido, design intocado).
3. **Fecha o ciclo**: pergunta se você tem a copy da LP e, se tiver, gera o Prompt Lovable final (tokens do builder + referências estruturais + copy real).

## Instalação

### Claude Code (terminal)
```bash
git clone https://github.com/Gabrielaraujo21/design-system-interview.git ~/.claude/skills/design-system-interview
```
Reinicie o Claude Code. A skill aparece automaticamente e é acionada quando você pede para estruturar uma marca / montar um design system. Você também pode chamá-la por `/design-system-interview`.

### Claude (app / claude.ai)
Empacote a pasta como `.skill` (ou suba o `SKILL.md` + `references/` + `assets/`) na área de Skills do seu perfil/projeto. Depois é só pedir para "entrevistar a marca" ou "montar o design system".

### Antigravity (e outros agentes)
O Antigravity lê `AGENTS.md`. Duas formas:
- **No projeto:** copie a pasta (ou só `AGENTS.md` + `references/` + `assets/`) para a raiz do workspace. O agente passa a seguir o fluxo automaticamente.
- **Como regra/workflow:** cole o conteúdo de `AGENTS.md` nas regras/instruções customizadas do Antigravity.

O mesmo `AGENTS.md` serve para Cursor, Gemini CLI, Codex e qualquer agente que respeite a convenção `AGENTS.md`.

## Como usar

Depois de instalada, comece com algo como:
> "Vamos estruturar uma marca nova." / "Faz a entrevista de marca comigo." / "Quero montar o design system do cliente X."

A skill conduz a entrevista, gera os arquivos e te guia até o Design System Builder e o Lovable.

## Pré-requisito: o Design System Builder

O `.dsproj.json` gerado é carregado no **Design System Builder v3** (arquivo `Design_System_Builder_v3.html`): 1ª etapa → **📂 Abrir projeto salvo**. O builder é onde o designer escolhe cores, fontes e tokens, valida contraste (WCAG), gera rampas tonais e exporta o Design System + o Prompt Lovable.

## Estrutura do repositório

```
design-system-interview/
├── SKILL.md          # entrada para Claude (Agent Skills)
├── AGENTS.md         # entrada portável (Antigravity, Cursor, Gemini, Codex…)
├── README.md         # este arquivo
├── references/
│   ├── interview.md          # roteiro da entrevista, fase a fase
│   ├── dsproj-schema.md      # schema do .dsproj.json + o que preencher
│   └── lovable-prompt.md     # receita do Prompt Lovable + esqueleto de LP
└── assets/
    └── project-template.dsproj.json   # esqueleto do projeto
```

## Licença

Uso interno V4 Company. Adapte à vontade.
