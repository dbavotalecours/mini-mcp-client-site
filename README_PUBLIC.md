# MINI_MCP_CLIENT — présentation publique

MINI_MCP_CLIENT est un runtime local MCP pour agents IA sur Windows.

Il vise à connecter des LLM à des outils locaux de manière plus contrôlée, traçable et vérifiable. Le projet est actuellement en bêta privée.

Ce dépôt public est seulement une vitrine. Il ne contient pas le code complet du projet privé.

## Résumé court

MINI_MCP_CLIENT fournit un couloir local entre un LLM ou un humain et des outils Windows :

```text
LLM / humain
→ mcp_cli.py
→ daemon local
→ MCPClient
→ outils MCP
→ preuves / logs / tests / mémoire
```

Le but est de permettre à un agent IA de travailler avec des fichiers, un terminal, SQLite, des workflows et des tests, tout en conservant une trace exploitable de ce qui a été fait.

## Pourquoi ce projet existe

Un LLM peut proposer une correction, une commande ou une méthode.

Mais dans un environnement local réel, il faut aussi pouvoir répondre à des questions simples :

- qu’est-ce qui a été exécuté ?
- quel outil local a répondu ?
- quel test a été lancé ?
- où sont les preuves ?
- l’action est-elle rejouable ?
- l’échec est-il clair ou silencieux ?

MINI_MCP_CLIENT cherche à réduire cette zone floue.

## Différence avec un CLI LLM classique

Un CLI LLM classique permet de discuter avec un modèle, parfois avec accès au dépôt courant.

MINI_MCP_CLIENT se positionne plutôt comme une couche locale de pilotage MCP :

- il garde un daemon local ;
- il expose des outils MCP configurés ;
- il trace les appels ;
- il peut lancer des workflows ;
- il peut vérifier des tests ;
- il peut conserver des méthodes utiles ;
- il peut aider à rejouer ou diagnostiquer un travail.

Il est complémentaire à Codex, Claude, Gemini, Qwen, GLM, Ollama, POPI ou LM Studio.

## Exemples d’outils locaux concernés

Selon la configuration privée :

- fichiers locaux ;
- terminal Windows ;
- SQLite ;
- workflows ;
- logs ;
- tests ;
- mémoire procédurale ;
- watchdog d’exécution ;
- diagnostic du daemon ;
- inventaire des outils MCP.

## Positionnement prudent

MINI_MCP_CLIENT n’est pas vendu comme une intelligence autonome générale.

Il ne remplace pas les grands modèles.

Il sert plutôt à leur donner une couche locale de travail, avec un accent sur :

- la preuve ;
- le contrôle ;
- la traçabilité ;
- la validation ;
- la mémoire procédurale.

## Statut de publication

Le projet complet reste privé.

Ce dépôt public sert à :

- présenter l’idée ;
- expliquer le positionnement ;
- préparer une démonstration privée ;
- proposer un diagnostic bêta ;
- recueillir l’intérêt de développeurs et utilisateurs techniques.

Aucun code runtime complet, aucune base SQLite, aucun log privé, aucun prompt privé et aucune clé API ne sont publiés ici.

## Public cible

Cette vitrine s’adresse surtout à :

- développeurs Windows ;
- utilisateurs de LLM locaux ou distants ;
- utilisateurs de Codex, Claude, Gemini, Qwen, GLM, Ollama ou LM Studio ;
- builders MCP ;
- consultants IA ;
- petites équipes qui veulent tester des agents IA avec outils locaux ;
- personnes qui veulent automatiser prudemment des diagnostics, tests et workflows.

## Limites actuelles

MINI_MCP_CLIENT est encore en validation terrain.

À ce stade :

- le code complet n’est pas public ;
- les démonstrations sont encadrées ;
- l’usage dépend de la configuration locale ;
- certains scénarios restent expérimentaux ;
- aucune promesse de sécurité absolue n’est faite ;
- aucune promesse d’autonomie complète n’est faite.

## Contact et démonstration

Des démonstrations privées et évaluations techniques peuvent être proposées sur demande.

La meilleure prochaine étape est une courte discussion pour vérifier le contexte, le niveau de risque acceptable et le type d’outils locaux à tester.
