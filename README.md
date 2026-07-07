# MINI_MCP_CLIENT

Runtime local MCP pour agents IA sur Windows.

MINI_MCP_CLIENT est un projet en bêta privée. Il connecte des LLM comme Codex, Claude, Gemini, Qwen, GLM, Ollama, LM Studio ou POPI à des outils locaux Windows, avec une approche centrée sur le contrôle, les preuves, les tests et la mémoire procédurale.

Ce dépôt public est une vitrine. Il ne contient pas le code source complet du runtime privé.

## Private beta / technical demo

MINI_MCP_CLIENT is available only through private, guided evaluation for now. Interested developers, technical reviewers, builders or early partners can request:

- a private walkthrough;
- a short technical evaluation;
- a limited beta diagnostic;
- a developer or investor discussion.

The complete runtime is not public in this repository. For access or a guided demo, see [Private beta offer](PRIVATE_BETA_OFFER.md), open an issue, or contact the maintainer through GitHub.

[Request a private demo](https://github.com/dbavotalecours/mini-mcp-client-site/issues/new?template=private-demo-request.md)

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

## Short terminal demos

These short clips show public-safe terminal surfaces only. This repository remains a public showcase for a private beta; it does not publish the full MINI_MCP_CLIENT runtime.

| Clip | Description |
| --- | --- |
| [CLI capabilities](assets/videos/01_cli_capabilities.mp4) | Shows Python, mcp_cli.py and the main capabilities: doctor, tools, watch, flow, scaffold, improve and apprentice. |
| [Local daemon status](assets/videos/02_daemon_status.mp4) | Shows a filtered diagnostic: client_exists, llm_available, daemon_running, daemon_status, daemon_port, tools_count and server_errors. |
| [MINI_MCP_FLOW validation](assets/videos/03_flow_validation.mp4) | Shows flow list and flow validate on health_check_mini_mcp with nodes, edges, errors and warnings. |
| [Controlled dry-run](assets/videos/04_flow_dry_run.mp4) | Shows flow run --dry-run health_check_mini_mcp and the planned execution steps without running real actions. |

For a private walkthrough or technical evaluation, open an issue or contact the maintainer through GitHub.

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

## Support development

MINI_MCP_CLIENT is currently a private-beta project. Optional support helps continue public demos, documentation, testing, and technical validation.

[Support development](https://buymeacoffee.com/dbavotalecours)

Support is optional and does not grant access to private source code, secrets, or confidential runtime internals.

## En savoir plus

- [Présentation publique détaillée](README_PUBLIC.md)
- [Script de démonstration 5 minutes](DEMO_5_MINUTES.md)
- [Offre bêta privée](PRIVATE_BETA_OFFER.md)
- [Checklist de sécurité avant publication](PUBLICATION_SAFETY_CHECKLIST.md)
