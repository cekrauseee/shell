---
slug: shell
name: cekrause/shell
repositoryUrl: https://github.com/cekrauseee/shell
description: >-
  a small ai chat experiment with the feel of a terminal.
metaDescription: >-
  an ai chat experiment with a terminal-style interface, keyboard controls,
  markdown responses, and a conversation kept in browser memory.
summary: >-
  i built shell as a focused ai chat with a custom block cursor, multiline
  input, keyboard prompt history, and markdown responses. it calls the
  openai api through the server and keeps the conversation in browser
  memory. it is a development experiment.
highlights:
  - "a prompt and a single conversation"
  - "keyboard controls and prompt history"
  - "a custom cursor with native text input"
  - "markdown responses and reduced-motion support"
---

shell opens with a prompt and a block cursor. you write, the assistant
replies, and the conversation fills the screen.

i built the interface around the keyboard. enter sends a message, shift+enter
adds a line, and the arrow keys bring back earlier prompts. control or command
+ l clears the conversation.

the cursor is custom, but the input underneath is a native text field, so
ordinary editing and selection still work. responses use markdown and appear
word by word after they arrive. the animation is skipped for people who prefer
reduced motion.

## keeping the scope small

the chat calls the openai api through the server. the app keeps the
conversation in browser memory, so reloading or clearing the page removes it.
api response storage is disabled for these requests.

it's a development experiment, with no accounts or saved history. it also
doesn't have the access and usage controls needed to run as a public service.
