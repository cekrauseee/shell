---
slug: shell
portfolioIndex: 4
name: cekrause/shell
repositoryUrl: https://github.com/cekrauseee/shell
description: >-
  An AI chat experiment with a terminal-inspired interface and keyboard
  controls.
metaDescription: >-
  Shell explores a chat interface built around a single conversation, with
  multiline input, prompt history, and Markdown responses.
summary: >-
  Shell explores a chat interface built around a single conversation. It opens
  with a text field and a block cursor; messages fill the screen as the
  conversation develops. The application combines the visual language of
  terminals with multiline input, prompt history, and Markdown responses.
highlights:
  - native text input with a custom presentation
  - conversation state in browser memory
  - OpenAI Responses API
  - a development experiment
---

Shell explores a chat interface built around a single conversation. It opens with a text field and a block cursor; messages fill the screen as the conversation develops.

The application combines the visual language of terminals with multiline input, prompt history, and Markdown responses.

## Native text input with a custom presentation

The block cursor is drawn over a native text field. Its appearance is custom, while editing, selection, and text entry continue to rely on the browser’s standard behavior.

Keyboard controls support sending messages, adding line breaks, retrieving earlier prompts, and clearing the conversation. Waiting and error states are also announced to assistive technologies.

Responses arrive in full before being displayed with a word-by-word reveal animation. The effect is disabled when reduced motion is preferred.

## Conversation state and model integration

The browser holds the active conversation in memory and sends it to a Server Action with each new message. The server validates the structure and order of the messages before calling the OpenAI Responses API. The API key stays on the server, and requests disable API response storage.

Reloading the page or clearing the chat removes the local history. Clearing also invalidates in-flight responses, preventing a request that finishes later from repopulating the conversation.

The current scope is a development experiment: a temporary session, without accounts, persistent history, or the usage controls needed to operate as a public service.
