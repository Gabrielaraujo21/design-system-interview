# Ato 3 — Prompt Lovable Final

Só entra aqui quando a pessoa **tem a copy** da LP. Objetivo: um prompt que, colado no Lovable, gera a LP já dentro da marca.

## Entradas
1. **A copy real** (colada em bloco ou por seção).
2. **Os tokens** — peça o texto do **"Prompt Lovable" exportado pelo builder** (Revisão → Copiar Prompt): traz cores, fontes, hierarquia, radius, sombra, movimento e tokens semânticos com estados. Sem export, peça ao menos cores (com papel) e fontes; o resto marque `🔤 [pegar do builder]`.
3. **Referências estruturais** (do `brand-brief.md`) — usadas só para layout, nunca para cor/fonte.

## Regras invioláveis
- **Tokens exatos** — nunca invente cor ou fonte.
- **Referência empresta só a estrutura** — deixe explícito no prompt.
- **Copy real, nunca inventada** — onde faltar, `🔤 [pendente]`, sem lorem ipsum nem promessa suposta.
- **Contraste AA** para texto sobre cor; **fundo claro predominante**; CTAs para o canal de conversão.

## Estrutura do prompt final (adapte às seções que a copy tiver)

```
Crie uma landing page em React + Tailwind para **<marca>**, <setor> em <cidade>.
Tom da marca: <tom de voz>. A marca nunca deve parecer: <naoParece>.

### Referências estruturais (só layout — nunca copiar cor, fonte ou texto)
- <URL 1> — <o que emprestar: ex. "hero em split, cards 3 colunas">
- <URL 2> — <...>

### Design tokens (obrigatórios — nunca usar fora desta lista)
<colar o bloco de tokens do "Prompt Lovable" exportado do builder>

### Voz & copy
- Tom: <tom> · Usar: <palavras> · Nunca usar: <proibidas>
- Todo CTA converte via <canal>, texto padrão: "<CTA padrão>"

### Seções (com a copy real)
Seção 1 — Hero: Headline "<copy>", Subheadline "<copy>", CTA "<CTA>" → <canal>
Seção 2 — <nome>: <copy real>
<...repita para cada seção; onde faltar, 🔤 [pendente]...>

### Regras finais
- Fundo claro; cor entra por CTAs, ícones e cards.
- Botão de conversão flutuante fixo → <canal>.
- Responsivo (mobile-first). Texto sobre cor só com contraste AA.
```

## Se a pessoa AINDA NÃO tem copy
Entregue este esqueleto (cada item é uma vaga de copy a escrever):
1. **Hero** — headline (promessa), subheadline (para quem/como), CTA.
2. **Diferenciais** — 3 provas concretas (da entrevista).
3. **Serviços / oferta** — em blocos, com micro-CTA.
4. **Sobre / autoridade** — quem é a marca (puxa do manifesto).
5. **Depoimentos / números** — prova social.
6. **Localização / contato** (se físico).
7. **FAQ** — objeções do público.
8. **CTA final**.

Diga: "Escreva a copy dessas seções e volte com ela + os tokens do builder que eu monto o prompt do Lovable."
