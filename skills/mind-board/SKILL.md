---
name: mind-board
description: Monta um conselho (board) de 3 a 5 minds pra opinar sobre uma decisão importante do seu negócio, cada uma com parecer próprio, depois tensões e uma resolução. Use quando a pessoa pedir "monta um board", "conselho de minds", "quero várias opiniões", "board sobre...", ou tiver uma decisão estratégica grande (preço, lançamento, contratação, posicionamento, mudar de rumo).
---

# Mind Board — conselho de 3 a 5 minds

Como ter um conselho consultivo: cada mind dá um parecer, elas discordam entre si, e no fim sai uma resolução. Para decisões grandes. Para algo menor, usar `mind-consulta` (1 mind) ou `mind-debate` (2-3 minds).

## Passo 1 — Entender o negócio ANTES de convocar (obrigatório)

1. Ler o `CLAUDE.md` da raiz do vault.
2. Procurar no vault notas ligadas à decisão (palavras-chave nos `.md`, **ignorando `minds/`**), incluindo `decisoes/` anteriores. Ler as 3 a 5 mais relevantes.
3. Resumir: o que vende, pra quem, situação atual, restrições (tempo, dinheiro, equipe), o que já tentou, números que a pessoa informou.
4. Se faltar algo essencial, fazer **uma** pergunta. Em modo automático, seguir e listar as suposições.

## Passo 2 — Montar o board

Se a pessoa não escolheu, usar a tabela (todas existem em `minds/`):

| Problema | Board sugerido |
|---|---|
| Preço / oferta | `alex_hormozi` + `eugene_schwartz` + `todd_brown` + `ramit_sethi` + `seth_godin` |
| Crescimento / escala | `paul_graham` + `sean_ellis` + `alex_hormozi` + `eliyahu_goldratt` + `avinash_kaushik` |
| Lançamento / funil | `russel_brunson` + `frank_kern` + `dan_kennedy` + `thiago_finch` + `joao_lozano` |
| Copy / anúncio | `eugene_schwartz` + `gary_halbert` + `john_caples` + `robert_collier` + `claude_hopkins` |
| Tráfego pago | `molly_pittman` + `pedro_sobral` + `savannah_sanchez` + `andrew_foxwell` |
| Conteúdo / marca pessoal | `gary_vee` + `seth_godin` + `dan_koe` |
| Produto / o que construir | `marty_cagan` + `jeff_patton` + `steve_jobs` + `don_norman` |
| Contratação / time | `lou_adler` + `hung_lee` + `mariana_torres` + `jose_amorim` |
| Estratégia / posicionamento | `peter_thiel` + `naval_ravikant` + `elon_musk` + `simon_wardley` |
| Decisão sob incerteza / vieses | `daniel_kahneman` + `naval_ravikant` + `kapil_gupta` |
| Serviço de IA / agência | `liam_ottley` + `alex_hormozi` + `greg_isenberg` |
| Produto com IA / técnico | `andrej_karpathy` + `paul_graham` + `kent_beck` |
| Decisão pessoal / carreira | `kapil_gupta` + `naval_ravikant` + `tim_ferriss` |

Para outras áreas, consultar `minds/CATALOGO.md`. Entre 3 e 5 membros.

Para cada membro, ler `minds/{nome}/system_prompts/COGNITIVE_OS.md` e, se ajudar, os frameworks em `minds/{nome}/synthesis/`, `artifacts/` ou `heuristics/` ligados ao tema. Se a pasta não existir, listar `minds/` e trocar — nunca inventar mind.

## Passo 3 — Reunião do board

```markdown
## Briefing
**Situação:** [2-3 linhas, com o contexto do vault]
**Decisão necessária:** [...]
**Restrições:** [...]
**Suposições:** [o que não estava no vault]
**Board:** [Mind 1] (área), [Mind 2] (área), [Mind 3] (área)

## [Mind 1] — Parecer
**Minha avaliação:** [2-4 parágrafos, frameworks da mind aplicados ao negócio]
**Minha recomendação:** [ação concreta]
**O que eu NÃO faria:** [armadilha]

## [Mind 2] — Parecer
[mesmo formato + pelo menos uma discordância de algo que outra mind disse]

(... até 5 membros)

## Pontos de tensão
| Tema | Posição A | Posição B |
|---|---|---|

## Resolução do board (moderador, fora das personas)
**Consenso:** [...]
**Divergência principal:** [...]
**Recomendação:** [caminho sugerido]
**Próximo passo hoje:** [1 ação]
**Risco a vigiar:** [...]
```

## Passo 4 — Salvar

Salvar em `decisoes/AAAA-MM-DD-board-tema.md` (criar `decisoes/` se não existir; se o arquivo já existir, acrescentar `-2`), com o cabeçalho:

```markdown
---
data: AAAA-MM-DD
tipo: board
minds: [a, b, c]
pergunta: "..."
---
```

Dizer à pessoa o caminho do arquivo.

## Regras

1. **3 a 5 membros.** Menos de 3 não é board; mais de 5 vira barulho.
2. **Cada membro fala uma vez**, a não ser que a pessoa peça outra rodada.
3. **Dissenso obrigatório:** todo membro, menos o primeiro, discorda de algo.
4. **Frameworks reais:** só conceitos que estão nos arquivos da mind.
5. **Reconstrução, não a pessoa:** falar "a mind do X". Sem vínculo nem endosso da pessoa real.
6. **Mind não é fonte de número:** não inventar preço, meta, percentual ou benchmark. Usar só números da pessoa; se faltar, escrever "definir com dado seu".
7. **A pessoa decide.** O board recomenda.
