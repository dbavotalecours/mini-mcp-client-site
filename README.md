# MINI_MCP_CLIENT

Runtime local MCP pour agents IA sur Windows.

MINI_MCP_CLIENT est un projet en bêta privée. Il connecte des LLM comme Codex, Claude, Gemini, Qwen, GLM, Ollama, LM Studio ou POPI à des outils locaux Windows, avec une approche centrée sur le contrôle, les preuves, les tests et la mémoire procédurale.

Ce dépôt public est une vitrine. Il ne contient pas le code source complet du runtime privé.

## Le problème

Les agents IA peuvent aider à lire, diagnostiquer, modifier et tester des projets. Mais dès qu’ils travaillent avec des outils locaux, plusieurs questions deviennent importantes :

- quel outil a été appelé ?
- avec quels paramètres ?
- quel résultat a été obtenu ?
- quels tests prouvent que l’action est correcte ?
- comment rejouer ou auditer une méthode utile ?
- comment éviter de confondre promesse, intention et preuve réelle ?

MINI_MCP_CLIENT explore cette zone : faire travailler un LLM avec des outils Windows, mais avec un couloir local explicite et observable.

## La solution proposée

Le chemin central est volontairement simple :

```text
LLM / humain
→ mcp_cli.py
→ daemon local
→ MCPClient
→ outils MCP
→ preuves / logs / tests / mémoire
```

L’idée n’est pas de remplacer Codex, Claude, Gemini ou Qwen.

L’idée est de leur fournir une couche locale MCP pour exécuter, tracer, tester et rejouer du travail avec des outils Windows.

## Fonctionnalités démontrables

Selon la configuration privée utilisée, MINI_MCP_CLIENT peut exposer des capacités comme :

- lecture et écriture de fichiers locaux ;
- terminal Windows contrôlé ;
- accès SQLite ;
- workflows locaux ;
- logs structurés ;
- tests automatisés ;
- mémoire procédurale ;
- watchdog d’exécution ;
- diagnostics du daemon local ;
- inventaire des outils MCP disponibles.

Ces fonctions sont en validation terrain. Elles ne sont pas présentées ici comme un produit public complet.

## Ce que ce projet n’est pas

MINI_MCP_CLIENT n’est pas :

- une AGI ;
- un remplaçant de Codex, Claude, Gemini ou Qwen ;
- une promesse d’autonomie totale ;
- une solution de sécurité absolue ;
- une plateforme enterprise prête pour production ;
- un dépôt open source complet du runtime privé.

## Statut actuel

Le projet est en bêta privée.

Le dépôt public sert à expliquer le concept, préparer des démonstrations et recueillir de l’intérêt technique. Le code complet de MINI_MCP_CLIENT n’est pas distribué publiquement pour le moment.

## Démonstration privée

Des démonstrations privées et évaluations techniques encadrées peuvent être proposées sur demande.

Objectifs possibles :

- comprendre si MINI_MCP_CLIENT convient à votre usage ;
- voir une démonstration du couloir local MCP ;
- évaluer l’intégration avec vos outils Windows ;
- discuter d’un diagnostic bêta limité.

## En savoir plus

- [Présentation publique détaillée](README_PUBLIC.md)
- [Script de démonstration 5 minutes](DEMO_5_MINUTES.md)
- [Offre bêta privée](PRIVATE_BETA_OFFER.md)
- [Checklist de sécurité avant publication](PUBLICATION_SAFETY_CHECKLIST.md)
