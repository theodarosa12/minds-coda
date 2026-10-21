---
name: mind-consulta
description: Uma mind (reconstrução de um especialista, ex. Alex Hormozi, Seth Godin, Naval) analisa um problema do seu negócio usando o contexto do seu vault. Use quando a pessoa pedir "consulta a mind X", "o que o Hormozi faria", "pergunta pro [especialista] sobre...", "quero a opinião de uma mind" ou quiser UMA perspectiva especializada sobre preço, oferta, copy, conteúdo, produto, time ou decisão.
---

# Mind Consulta — uma mind analisa o seu problema

Uma "mind" é um arquivo que reconstrói o jeito de pensar de um especialista (frameworks, critérios, tom). Esta skill faz UMA mind olhar para o problema do aluno **com o contexto do negócio dele**, não no vácuo.

## Passo 1 — Entender o negócio ANTES de chamar a mind (obrigatório)

1. Ler o `CLAUDE.md` da raiz do vault (é onde a pessoa descreve quem é e o que faz).
2. Procurar no vault notas ligadas ao tema da pergunta (ex.: preço, oferta, clientes, metas). Buscar por palavras-chave nos arquivos `.md`, **ignorando a pasta `minds/`**. Ler as 3 a 5 mais relevantes, incluindo decisões anteriores em `decisoes/` sobre o mesmo tema.
3. Montar um resumo curto do contexto: o que a pessoa vende, pra quem, situação atual, restrições, o que já tentou, números que ELA informou.
4. Se faltar algo essencial, fazer **uma** pergunta por vez. Se estiver rodando sem conversa (modo automático), seguir em frente e listar as suposições no resultado.

## Passo 2 — Escolher e carregar a mind

- Se a pessoa disse qual mind, usar essa. Se não, olhar `minds/CATALOGO.md` e sugerir 1 que combine com o problema (dizer por quê em 1 linha).
- Ler, a partir da raiz do vault:
  - `minds/{nome}/system_prompts/COGNITIVE_OS.md` (principal)
  - Se existir e ajudar: arquivos de frameworks em `minds/{nome}/synthesis/`, `minds/{nome}/artifacts/` ou `minds/{nome}/heuristics/` (ler só o que tiver relação com o tema; não precisa ler tudo).
- Se a pasta não existir, listar `minds/` e mostrar os nomes disponíveis. Não inventar mind.

## Passo 3 — Análise da mind

Falar em primeira pessoa, no estilo da mind, usando **só frameworks e ideias que estão nos arquivos dela**, aplicados ao contexto do Passo 1.

Formato:

```markdown
## Contexto usado
- [3-5 bullets do que veio do vault: negócio, situação, restrições]
- Suposições: [o que não estava no vault e foi assumido]

## [Nome da mind] — Análise

**Minha leitura do problema:**
[diagnóstico aplicado ao negócio da pessoa]

**O que eu faria:**
[2-4 ações concretas, em ordem]

**Framework usado:**
[nome do framework/princípio e de qual arquivo da mind ele veio]

**O que eu NÃO faria:**
[armadilha que essa mind enxerga]

## Próximo passo
[uma ação que a pessoa consegue fazer hoje]
```

## Passo 4 — Salvar

Salvar o resultado em `decisoes/AAAA-MM-DD-tema.md` (data de hoje, tema curto em minúsculas com hífen; criar a pasta `decisoes/` se não existir; se o arquivo já existir, acrescentar `-2`). Começar o arquivo com:

```markdown
---
data: AAAA-MM-DD
tipo: consulta
minds: [nome]
pergunta: "..."
---
```

No fim, dizer à pessoa o caminho do arquivo salvo.

## Regras

1. **A mind é uma reconstrução, não a pessoa.** Não dizer "o Hormozi recomenda" como se fosse ele; dizer "a mind do Hormozi". Ela não tem vínculo nem endosso da pessoa real.
2. **A mind não é fonte de número.** Não inventar preço, percentual, meta, benchmark ou métrica. Usar só números que a pessoa deu ou que estão nas notas dela. Se a recomendação precisa de um número que não existe, escrever "definir com dado seu" e explicar como medir.
3. **Contexto primeiro.** Conselho genérico, que serviria pra qualquer negócio, é falha. Toda recomendação tem que citar algo do contexto do Passo 1.
4. **Frameworks reais.** Não inventar conceito que não está nos arquivos da mind.
5. **A pessoa decide.** A mind recomenda; não impõe.
