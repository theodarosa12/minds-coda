# Minds · Setup CODA

Consultores virtuais pro teu segundo cérebro. Cada mind é um arquivo que ensina a IA a pensar como uma pessoa específica: os frameworks dela, como decide, como fala e o que ela recusa.

> Ele já te conhece. Agora ele chama quem sabe.

## Como usar

1. Copia a pasta `minds/` pra dentro do teu vault.
2. Acrescenta UMA linha no teu `CLAUDE.md`:
   ```
   Quando eu pedir conselho de uma mind, leia minds/{nome}/system_prompts/COGNITIVE_OS.md antes de responder.
   ```
3. Testa: "quais minds eu tenho?"

A mind fica na pasta e só entra na conversa quando tu chama. Não cola ela no `CLAUDE.md`: ela é longa e ocuparia toda conversa.

## Três jeitos de usar

- **Consulta:** uma mind olha um problema teu. Ex.: "Pede pro alex_hormozi olhar o preço da minha oferta."
- **Debate:** duas ou três minds discordam entre si, e a síntese sai da briga.
- **Board:** um conselho de minds, cada uma com um ângulo (oferta, marca, produto, risco).

## Importante

- A mind **não é a pessoa**. É uma reconstrução feita a partir de conteúdo público e pode errar.
- Não tem vínculo com as pessoas retratadas nem endosso delas.
- Use pra pensar melhor, não como fonte de dado ou de número. Quem decide é tu.

Página com o banco de skills e a explicação visual: https://theodacodamindsbancodeskills.vercel.app
