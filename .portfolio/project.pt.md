---
description: >-
  um experimento de chat com ia e jeito de terminal.
metaDescription: >-
  um chat com ia inspirado em terminais, com atalhos de teclado,
  respostas em markdown e uma conversa que fica na memória do navegador.
summary: >-
  fiz o shell como um chat com ia focado em uma conversa. ele tem um cursor
  próprio, mensagens com várias linhas, histórico de prompts pelo teclado
  e respostas em markdown. as chamadas à api da openai passam pelo servidor,
  e a conversa fica na memória do navegador. é um experimento de desenvolvimento.
highlights:
  - um campo de texto e uma conversa
  - atalhos de teclado e histórico de prompts
  - cursor próprio sobre um campo de texto nativo
  - respostas em markdown e opção de reduzir animações
---

o shell abre com um campo de texto e um cursor em bloco. você escreve,
o assistente responde, e a conversa vai preenchendo a tela.

fiz a interface pensando no teclado. enter envia a mensagem, shift+enter
abre uma nova linha, e as setas trazem de volta os prompts anteriores.
control ou command + l limpa a conversa.

o cursor tem um visual próprio, mas o campo de texto por baixo é nativo.
dá para editar e selecionar texto como de costume. as respostas usam markdown
e aparecem palavra por palavra depois de recebidas. quem prefere reduzir
as animações vê a resposta sem esse efeito.

## um experimento pequeno

o chat chama a api da openai pelo servidor. a conversa fica na memória do
navegador e desaparece ao recarregar a página ou limpar o chat. as chamadas
também desativam o armazenamento das respostas na api.

é um experimento de desenvolvimento, sem contas ou histórico salvo.
ainda faltam os controles de acesso e de uso necessários para abrir
o chat como um serviço público.
