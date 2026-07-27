# Ato 3 — Prompt Lovable

Só aqui quando a pessoa **tem a copy** da LP. Objetivo: um prompt que, colado no Lovable, gera a LP dentro da marca.

## Entradas
1. **A copy real** (em bloco ou por seção).
2. **Os tokens** — peça o **"Prompt Lovable" exportado pelo builder** (Revisão → Copiar Prompt): traz cores, fontes, hierarquia, sombra, movimento e tokens semânticos. Sem export, peça ao menos cores (com papel) e fontes.
3. **Referências estruturais** (do `brand-brief.md`) — só para layout, nunca cor/fonte.

## Regras invioláveis
- **Tokens exatos** — nunca invente cor ou fonte.
- **Referência empresta só a estrutura** — diga isso no prompt.
- **Copy real, nunca inventada** — onde faltar, `🔤 [pendente]`, sem lorem ipsum.
- **Contraste AA** para texto sobre cor; fundo claro predominante; CTAs para o canal de conversão.

## Estrutura do prompt final (adapte às seções que a copy tiver)

```
Crie uma landing page em React + Tailwind para **<marca>**, <setor> em <cidade>.
Tom: <tom de voz>. Nunca deve parecer: <naoParece>.

### Referências estruturais (só layout — nunca copiar cor, fonte ou texto)
- <URL> — <o que emprestar: ex. "hero em split, cards 3 colunas">

### Design tokens (obrigatórios — nunca usar fora desta lista)
<colar o bloco de tokens exportado do builder>

### Voz & copy
- Tom: <tom> · Usar: <palavras> · Nunca: <proibidas>
- CTA converte via <canal>, texto: "<CTA padrão>"

### Seções (com a copy real)
Hero: Headline "<copy>", Sub "<copy>", CTA "<CTA>"
<demais seções com a copy; onde faltar, 🔤 [pendente]>

### Regras finais
- Fundo claro; cor só em CTAs, ícones e cards. Botão flutuante → <canal>. Mobile-first. Texto sobre cor só com contraste AA.
```

## Se AINDA não tem copy
Entregue o esqueleto pra orientar quem vai escrever: **Hero** (headline, sub, CTA) · **Diferenciais** (3 provas) · **Serviços/oferta** · **Sobre/autoridade** (do manifesto) · **Depoimentos/números** · **Localização/contato** (se físico) · **FAQ** · **CTA final**. Diga: "Escreva a copy dessas seções e volte com ela + os tokens do builder que eu monto o prompt."
