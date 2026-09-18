---
description: >-
  Une expérimentation de chat IA, avec une interface inspirée des terminaux et
  une interaction au clavier.
metaDescription: >-
  Shell explore une interface de chat centrée sur une seule conversation, avec
  une saisie multiligne, un historique des prompts et des réponses en Markdown.
summary: >-
  Shell explore une interface de chat centrée sur une seule conversation.
  L’application s’ouvre sur un champ de texte et un curseur bloc ; les messages
  remplissent l’écran au fil de l’échange. Elle associe le langage visuel des
  terminaux à la saisie multiligne, à l’historique des prompts et à l’affichage
  des réponses en Markdown.
highlights:
  - saisie native avec présentation personnalisée
  - état de la conversation conservé en mémoire dans le navigateur
  - OpenAI Responses API
  - une expérimentation de développement
---

Shell explore une interface de chat centrée sur une seule conversation. L’application s’ouvre sur un champ de texte et un curseur bloc ; les messages remplissent l’écran au fil de l’échange.

Elle associe le langage visuel des terminaux à la saisie multiligne, à l’historique des prompts et à l’affichage des réponses en Markdown.

## Saisie native avec présentation personnalisée

Le curseur bloc est dessiné par-dessus un champ de texte natif. Son apparence est personnalisée, tandis que l’édition, la sélection et la saisie du texte reposent toujours sur le comportement standard du navigateur.

Les commandes clavier permettent d’envoyer des messages, d’insérer des retours à la ligne, de retrouver des prompts précédents et d’effacer la conversation. Les états d’attente et d’erreur sont également annoncés aux technologies d’assistance.

Les réponses sont reçues intégralement avant d’être affichées au moyen d’une animation qui les révèle mot par mot. Cet effet est désactivé lorsque la préférence pour réduire les animations est activée.

## État de la conversation et intégration du modèle

Le navigateur conserve la conversation active en mémoire et l’envoie à une Server Action avec chaque nouveau message. Le serveur vérifie la structure et l’ordre des messages avant d’appeler l’OpenAI Responses API. La clé API reste sur le serveur et les requêtes désactivent l’enregistrement des réponses de l’API.

Recharger la page ou effacer le chat supprime l’historique local. L’effacement invalide également les réponses en cours, ce qui empêche une requête terminée plus tard de repeupler la conversation.

Le périmètre actuel est celui d’une expérimentation de développement : une session temporaire, sans comptes, historique persistant ni contrôles d’utilisation nécessaires à l’exploitation comme service public.
