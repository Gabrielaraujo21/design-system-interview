# Prompt Lovable Final — Receita

Este é o Ato 3. Só entra aqui quando a pessoa **tem a copy** da landing page. O objetivo é entregar um prompt que, colado no Lovable, gera a LP já dentro da marca.

## Entradas necessárias

1. **A copy real** da LP (colada em bloco ou por seção).
2. **Os tokens do design system** — peça o texto do **"Prompt Lovable" exportado pelo builder** (etapa Revisão → Copiar Prompt). Ele já traz cores, fontes, hierarquia, radius, sombra, movimento e tokens semânticos com estados. Se a pessoa não tiver exportado ainda, peça pelo menos as cores (com papel) e as fontes; o resto marque como `🔤 [pegar do builder]`.
3. **As referências estruturais** da entrevista (do `brand-brief.md`) — os sites que a pessoa admira, usados **só para estrutura/layout**, nunca para cor ou fonte.

## Regras invioláveis do prompt

- **Tokens exatos.** Use os hex, fontes e valores do builder. Nunca invente cor nem fonte.
- **Referência empresta só a estrutura.** Deixe explícito no prompt: "as referências abaixo servem só de inspiração de layout/hierarquia — cores, fontes e textos são sempre os desta marca".
- **Copy real, nunca inventada.** Use a copy que a pessoa deu, literal. Onde faltar texto, escreva `🔤 [pendente: descrever o que falta]` — nunca preencha com lorem ipsum nem invente promessa de cliente.
- **Acessibilidade.** Para texto sobre cor, use só pares com contraste AA (o builder já lista os pares aprovados no Prompt Lovable exportado).
- **Fundo claro predominante**, CTAs levando ao canal de conversão definido na entrevista.

## Estrutura do prompt final

Monte assim (adapte às seções que a copy realmente tiver):

```
Crie uma landing page em React + Tailwind para **<marca>**, <setor> em <cidade>.
Tom da marca: <tom de voz>. A marca nunca deve parecer: <naoParece>.

### Referências estruturais (só layout/hierarquia — nunca copiar cor, fonte ou texto)
- <URL 1> — <o que emprestar: ex. "hero em split, cards em grade de 3">
- <URL 2> — <...>

### Design tokens (obrigatórios — nunca usar fora desta lista)
<colar aqui o bloco de tokens do "Prompt Lovable" exportado pelo builder:
cores com papel, fontes, hierarquia, radius, botões, sombra, movimento, tokens semânticos, pares de contraste AA>

### Voz & copy
- Tom: <tom>
- Usar: <palavras da marca>
- Nunca usar: <palavras proibidas>
- Todo CTA converte via <canal>, texto padrão: "<CTA padrão>"

### Seções da página (com a copy real)
<Para cada seção, título + copy exata fornecida pela pessoa. Ex.:>

Seção 1 — Hero
- Headline: "<copy real>"
- Subheadline: "<copy real>"
- CTA: "<CTA>" → <canal>

Seção 2 — <nome>
- <copy real, bullets, etc.>

<...repita para todas as seções que a copy cobrir...>

### Regras finais
- Fundo claro em toda a página; cor entra por CTAs, ícones e cards.
- Botão de conversão flutuante fixo levando a <canal>.
- Responsivo (mobile-first) nos breakpoints do design system.
- Onde faltar copy, deixar 🔤 [pendente], nunca inventar.
```

## Esqueleto de seções (quando a pessoa AINDA NÃO tem copy)

Se a resposta for "não tenho a copy ainda", entregue este esqueleto para orientar quem vai escrever — cada item é uma vaga de copy a preencher:

1. **Hero** — headline (promessa principal), subheadline (para quem/como), CTA.
2. **Prova rápida / diferenciais** — 3 provas concretas (vêm dos diferenciais da entrevista).
3. **Serviços / oferta** — o que vende, em blocos, cada um com micro-CTA.
4. **Sobre / autoridade** — quem é a marca, por que confiar (puxa do manifesto).
5. **Depoimentos / números** — provas sociais.
6. **Localização / contato** (se físico) — endereço, mapa, horário.
7. **FAQ** — objeções principais do público.
8. **CTA final** — última chamada para o canal de conversão.

Diga: "Escreva a copy dessas seções (ou das que fizerem sentido) e volte aqui — com a copy e os tokens do builder eu monto o prompt final do Lovable."
