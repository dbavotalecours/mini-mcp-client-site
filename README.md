# MINI_MCP_CLIENT

## Runtime local MCP pour agents IA sur Windows

MINI_MCP_CLIENT est un projet en bêta privée.

Il ne remplace pas Claude, Codex, Gemini, Qwen, GLM ou Ollama.  
Il leur fournit plutôt une couche locale MCP pour connecter des agents IA à des outils Windows comme :

- fichiers locaux ;
- terminal / commandes système ;
- SQLite ;
- workflows ;
- logs ;
- tests ;
- mémoire procédurale.

## Objectif

Le but est de permettre à un agent IA d’exécuter, tracer, tester et rejouer des actions locales de façon plus contrôlée.

Schéma simple :

```text
LLM / humain
→ mcp_cli.py
→ daemon local
→ MCPClient
→ outils MCP
→ preuves / logs / tests / mémoire