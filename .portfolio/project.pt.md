---
description: "Um chat com IA em estilo terminal, construído com a API Responses da OpenAI."
metaDescription: "Shell é uma interface de chat com IA em estilo terminal, construída com Next.js e a API Responses da OpenAI."
summary: "Shell é um chat com IA em estilo terminal centrado em uma única conversa. Ele combina controles orientados ao teclado, respostas legíveis em Markdown e uma interface mínima em tela cheia."
highlights:
  - "Chat com IA"
  - "Interface de terminal"
  - "Next.js"
  - "API da OpenAI"
  - "Markdown"
  - "Acessibilidade"
---

## Produto

Visitantes escrevem prompts com várias linhas, percorrem prompts anteriores com as setas e limpam a conversa com um atalho de teclado conhecido. O assistente responde no idioma da mensagem mais recente.

A interface usa a objetividade de um terminal sem fingir ser uma linha de comando. A conversa continua sendo a única superfície principal.

## O que construí

Construí a interface de chat em tela cheia com um cursor de bloco personalizado, histórico de prompts, estados de espera e erro e anúncios de status acessíveis.

As respostas renderizam GitHub Flavored Markdown com segurança e aparecem palavra por palavra. A animação é desativada quando o visitante prefere movimento reduzido.

## Decisões de engenharia

Uma Server Action do Next.js valida a conversa antes de chamar a API Responses da OpenAI. A chave da API permanece no servidor, e as solicitações desativam o armazenamento de respostas pela OpenAI.

As mensagens permanecem na memória do navegador e desaparecem após recarregar a página ou limpar a conversa. O projeto ainda não inclui contas, histórico persistente, limites de uso ou os controles necessários para um serviço público em produção.
