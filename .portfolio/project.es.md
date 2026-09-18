---
description: >-
  Un experimento de chat con IA, con una interfaz inspirada en los terminales y
  control mediante el teclado.
metaDescription: >-
  Shell explora una interfaz de chat centrada en una única conversación, con
  entrada multilínea, historial de prompts y respuestas en Markdown.
summary: >-
  Shell explora una interfaz de chat centrada en una única conversación. La
  aplicación se abre con un campo de texto y un cursor de bloque; los mensajes
  van ocupando la pantalla a medida que avanza la conversación. Combina el
  lenguaje visual de los terminales con entrada multilínea, historial de prompts
  y respuestas en Markdown.
highlights:
  - entrada nativa con presentación personalizada
  - estado de la conversación en la memoria del navegador
  - OpenAI Responses API
  - un experimento de desarrollo
---

Shell explora una interfaz de chat centrada en una única conversación. La aplicación se abre con un campo de texto y un cursor de bloque; los mensajes van ocupando la pantalla a medida que avanza la conversación.

Combina el lenguaje visual de los terminales con entrada multilínea, historial de prompts y respuestas en Markdown.

## Entrada nativa con presentación personalizada

El cursor de bloque se dibuja sobre un campo de texto nativo. Su apariencia es personalizada, mientras que la edición, la selección y la introducción de texto siguen basándose en el comportamiento estándar del navegador.

Los controles del teclado permiten enviar mensajes, insertar saltos de línea, recuperar prompts anteriores y limpiar la conversación. Los estados de espera y error también se anuncian a las tecnologías de asistencia.

Las respuestas se reciben completas antes de mostrarse con una animación que las revela palabra por palabra. El efecto se desactiva cuando se prefiere reducir el movimiento.

## Estado de la conversación e integración con el modelo

El navegador mantiene la conversación activa en memoria y la envía a una Server Action con cada mensaje nuevo. El servidor valida la estructura y el orden de los mensajes antes de llamar a la OpenAI Responses API. La clave de API permanece en el servidor y las solicitudes desactivan el almacenamiento de respuestas de la API.

Recargar la página o limpiar el chat elimina el historial local. La limpieza también invalida las respuestas en curso, lo que evita que una solicitud que termine más tarde vuelva a poblar la conversación.

El alcance actual es un experimento de desarrollo: una sesión temporal, sin cuentas, historial persistente ni los controles de uso necesarios para operar como un servicio público.
