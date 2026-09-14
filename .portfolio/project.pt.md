---
description: >-
  Um experimento de chat com IA, com interface inspirada em terminais e
  interação pelo teclado.
metaDescription: >-
  O Shell explora uma interface de chat concentrada em uma única conversa, com
  mensagens de várias linhas, histórico de prompts e respostas em Markdown.
summary: >-
  O Shell explora uma interface de chat concentrada em uma única conversa. A
  aplicação combina a linguagem visual dos terminais com mensagens de várias
  linhas, histórico de prompts e respostas em Markdown.
highlights:
  - entrada nativa com apresentação personalizada
  - histórico de prompts
  - respostas em Markdown
  - uma sessão temporária, sem contas ou histórico persistente
---

O Shell explora uma interface de chat concentrada em uma única conversa. A tela começa com um campo de texto e um cursor em bloco; as mensagens ocupam o espaço conforme a interação avança.

A aplicação combina a linguagem visual dos terminais com mensagens de várias linhas, histórico de prompts e respostas em Markdown.

## Entrada nativa com apresentação personalizada

O cursor em bloco é desenhado sobre um campo de texto nativo. A apresentação visual é personalizada, enquanto edição, seleção e entrada de texto continuam apoiadas no comportamento do navegador.

Os controles de teclado permitem enviar mensagens, inserir novas linhas, recuperar prompts anteriores e limpar a conversa. Estados de espera e erro também são anunciados para tecnologias assistivas.

As respostas são recebidas por completo antes de serem apresentadas com uma animação de revelação por palavras. A preferência por movimento reduzido desativa esse efeito.

## Estado da conversa e integração com o modelo

O navegador mantém a conversa ativa em memória e envia seu conteúdo a uma Server Action a cada nova mensagem. O servidor valida a estrutura e a ordem das mensagens antes de chamar a API Responses da OpenAI. A chave de acesso permanece no servidor, e as chamadas desativam o armazenamento de respostas da API.

Recarregar a página ou limpar o chat remove o histórico local. A limpeza também invalida respostas em andamento, evitando que uma chamada concluída depois volte a preencher a conversa.

O escopo atual é o de um experimento de desenvolvimento: uma sessão temporária, sem contas, histórico persistente ou controles de uso para operação como serviço público.
