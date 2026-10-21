# Instalador do pacote Minds (para o Claude Code)

Este arquivo é para o **Claude Code** que está ajudando um aluno. Quando o aluno pedir algo como *"Instala as minds desse repositório no meu vault: https://github.com/theodarosa12/minds-coda"*, siga os passos abaixo. Fale com o aluno em português simples, sem jargão.

## Regra de ouro

**Nunca sobrescrever nem apagar nada do aluno.** Só acrescentar. Se um arquivo ou pasta com o mesmo nome já existir, manter o do aluno e avisar no final.

## Passos

1. **Achar o vault.** O vault é a pasta onde o Claude Code foi aberto (diretório atual). Se não parecer um vault (sem notas `.md` e sem pasta `.obsidian/`), perguntar ao aluno qual é a pasta antes de continuar.

2. **Baixar o pacote numa pasta temporária** (fora do vault):
   - Com git: `git clone --depth 1 https://github.com/theodarosa12/minds-coda.git <pasta-temporária>`
   - Sem git: baixar `https://github.com/theodarosa12/minds-coda/archive/refs/heads/main.zip` e descompactar na pasta temporária.
   - Se o aluno passou um caminho local em vez do link, usar esse caminho direto (não precisa baixar).

3. **Copiar as minds** do pacote `minds/` para `minds/` na raiz do vault, sem sobrescrever o que já existe:
   `rsync -a --ignore-existing <pacote>/minds/ <vault>/minds/`
   (sem rsync: `cp -Rn`, ou copiar pasta por pasta pulando o que já existe).

4. **Copiar o catálogo** `<pacote>/CATALOGO.md` para `<vault>/minds/CATALOGO.md` (só se ainda não existir).

5. **Copiar as skills** de `<pacote>/skills/` para `<vault>/.claude/skills/` (criar a pasta se não existir). São três: `mind-consulta`, `mind-debate`, `mind-board`. Se já existir uma skill com o mesmo nome, não sobrescrever; avisar.

6. **Criar a pasta `decisoes/`** na raiz do vault, se não existir. É onde os resultados ficam salvos.

7. **Acrescentar UMA linha no `CLAUDE.md` do vault** (criar o arquivo se não existir; se já existir, só acrescentar no final, sem mexer no resto; se a linha já estiver lá, não repetir):

   ```
   - Minds: especialistas reconstruídos em `minds/` (lista em `minds/CATALOGO.md`). Use as skills `mind-consulta`, `mind-debate` e `mind-board`; resultados vão em `decisoes/`.
   ```

   Não colar conteúdo de mind no CLAUDE.md.

8. **Apagar a pasta temporária** do passo 2 (só ela).

9. **Conferir:** contar as pastas em `<vault>/minds/` (sem contar o CATALOGO.md), confirmar que as três skills estão em `<vault>/.claude/skills/` e que a linha está no CLAUDE.md. Informar os números reais da contagem.

10. **Mostrar ao aluno** a mensagem final abaixo (ajustando a contagem real e listando o que foi pulado por já existir, se houver).

## Mensagem final para o aluno

```
Pronto! Instalei [N] minds na pasta minds/ do seu vault e 3 comandos novos.

Os 3 comandos (é só pedir com essas palavras):
1. mind-consulta — uma mind analisa seu problema.
   Ex.: "consulta a mind alex_hormozi: devo subir o preço do meu serviço?"
2. mind-debate — 2 ou 3 minds discordam e no fim vem uma síntese.
   Ex.: "faz um debate entre alex_hormozi e seth_godin sobre meu preço"
3. mind-board — um conselho de 3 a 5 minds para uma decisão grande.
   Ex.: "monta um board pra decidir se eu lanço meu curso agora"

Antes de responder, elas leem o seu CLAUDE.md e suas notas, pra falar do SEU negócio.
Cada resultado fica salvo em decisoes/.
Lista de todas as minds: minds/CATALOGO.md

Se os comandos não aparecerem, feche e abra o Claude Code de novo.

Lembrete: cada mind é uma reconstrução feita por IA a partir de material público.
Não é a pessoa, não tem vínculo nem endosso dela, e não é fonte de números.
```
