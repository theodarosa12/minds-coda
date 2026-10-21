---
name: mind-debate
description: Debate entre 2 ou 3 minds que DISCORDAM sobre um problema do seu negócio — uma propõe, outra critica, a terceira traz o que faltou, e no fim vem uma síntese. Use quando a pessoa pedir "debate entre minds", "coloca X contra Y", "quero visões opostas", "faz um debate sobre..." ou tiver uma decisão com prós e contras reais (preço, oferta, posicionamento, canal, produto).
---

# Mind Debate — propor, criticar, sintetizar

Debate com dissenso forçado: as minds não podem concordar por educação. Serve pra decisões com trade-off real. **Não usar** pra pergunta com resposta única ou tarefa simples.

## Passo 1 — Entender o negócio ANTES do debate (obrigatório)

1. Ler o `CLAUDE.md` da raiz do vault.
2. Procurar no vault notas ligadas ao tema (palavras-chave nos `.md`, **ignorando `minds/`**), incluindo `decisoes/` anteriores. Ler as 3 a 5 mais relevantes.
3. Resumir o contexto: o que vende, pra quem, situação atual, restrições, números que a pessoa informou.
4. Se faltar algo essencial, fazer **uma** pergunta. Em modo automático, seguir e listar as suposições.

## Passo 2 — Escolher 2 ou 3 minds

Se a pessoa não escolheu, sugerir pela tabela (todas existem em `minds/`):

| Tema | Minds sugeridas |
|---|---|
| Preço / oferta | `alex_hormozi` × `eugene_schwartz` × `ramit_sethi` |
| Copy / anúncio | `eugene_schwartz` × `gary_halbert` × `john_caples` |
| Marketing / funil | `russel_brunson` × `frank_kern` × `dan_kennedy` |
| Estratégia de negócio | `paul_graham` × `peter_thiel` × `naval_ravikant` |
| Produto | `marty_cagan` × `jeff_patton` × `kent_beck` |
| Conteúdo / marca | `gary_vee` × `seth_godin` × `dan_koe` |
| Decisão pessoal / foco | `kapil_gupta` × `naval_ravikant` × `tim_ferriss` |

Para outras áreas, consultar `minds/CATALOGO.md`.

Para cada mind, ler `minds/{nome}/system_prompts/COGNITIVE_OS.md` e, se ajudar, os arquivos de frameworks em `minds/{nome}/synthesis/` ou `artifacts/` ligados ao tema. Se uma pasta não existir, listar `minds/` e escolher outra — nunca inventar mind.

## Passo 3 — Debate (uma rodada)

```markdown
## Contexto usado
- [3-5 bullets do vault] · Suposições: [...]

## [Mind A] — Proposta
**Minha leitura do problema:** [aplicada ao negócio da pessoa]
**O que eu faria:** [ação concreta]
**Framework:** [nome, vindo dos arquivos da mind]

## [Mind B] — Crítica
**Onde [Mind A] erra ou fica incompleta:** [discordância de verdade, não detalhe]
**Risco que ninguém considerou:** [...]
**O que eu faria diferente:** [alternativa]

## [Mind C] — O que os dois estão perdendo (se houver 3ª mind)
**Ponto cego:** [...]
**Minha posição:** [...]

## Síntese (moderador, fora das personas)
**Maior tensão:** [onde mais discordaram]
**Onde concordaram:** [se houver]
**Recomendação prática:** [caminho sugerido, pesando os argumentos e o contexto]
**Pergunta pra você decidir:** [1 pergunta clara]
```

## Passo 4 — Salvar

Salvar em `decisoes/AAAA-MM-DD-debate-tema.md` (criar `decisoes/` se não existir; se já existir o arquivo, acrescentar `-2`), com o cabeçalho:

```markdown
---
data: AAAA-MM-DD
tipo: debate
minds: [a, b, c]
pergunta: "..."
---
```

Dizer à pessoa o caminho do arquivo.

## Regras

1. **Máximo 3 minds**, **uma rodada**. Sem loop.
2. **Dissenso obrigatório:** a Mind B tem que discordar de algo central.
3. **Sem biografia:** não contar a história da pessoa; só pensar e falar como a mind.
4. **Frameworks reais:** só conceitos que estão nos arquivos da mind.
5. **Reconstrução, não a pessoa:** falar "a mind do X". Sem vínculo nem endosso da pessoa real.
6. **Mind não é fonte de número:** não inventar preço, meta, percentual ou benchmark. Usar só números da pessoa; se faltar, escrever "definir com dado seu".
7. **A pessoa decide.** A síntese sugere.
