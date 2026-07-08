# MINI_MCP_CLIENT

MINI_MCP_CLIENT aide un LLM à utiliser des outils Windows locaux sans agir dans le noir : commandes tracées, résultats vérifiables, workflows dry-run, mémoire procédurale et preuve avant confiance.

Ce dépôt public est une vitrine pour un runtime MCP local en bêta privée. Il montre le concept, les surfaces de démonstration et les preuves terminal, sans publier le code complet du runtime privé.

## Private beta / technical demo

MINI_MCP_CLIENT is currently available only through private, guided evaluation. Interested developers, technical reviewers, builders or early partners can request:

- a private walkthrough;
- a short technical evaluation;
- a limited beta diagnostic;
- a developer or investor discussion.

[Request a private demo](https://github.com/dbavotalecours/mini-mcp-client-site/issues/new?template=private-demo-request.md)

For more context, see [Private beta offer](PRIVATE_BETA_OFFER.md).

## The problem

LLMs can read, diagnose, modify and test local projects. But once an AI agent starts using local tools, the important question becomes less “can it act?” and more:

- what tool was called?
- with what parameters?
- what result came back?
- what test or log proves the result?
- can the method be replayed, explained or audited later?
- did the model actually verify the work, or only sound confident?

MINI_MCP_CLIENT explores this gap: letting a LLM work with local Windows tools through an explicit, observable MCP path.

## The solution

The core path is intentionally simple:

```text
LLM
→ mcp_cli.py
→ local daemon
→ MCPClient
→ MCP tools
→ proofs / logs / tests / procedural memory
```

In practice, this means the LLM does not have to “guess” what happened. It can call local tools through a controlled CLI, receive structured results, inspect logs, run dry-runs, validate workflows, and reuse procedural memory from previous validated work.

MINI_MCP_CLIENT does not replace Codex, Claude, Gemini, Qwen, GLM, OpenAI, Ollama, LM Studio or local models. It gives them a local MCP workbench on Windows.

## Short terminal demos

These short clips show public-safe terminal surfaces only. They demonstrate the public-facing behavior without exposing private runtime code, secrets, internal prompts, logs or databases.

| Clip | What it shows |
| --- | --- |
| [CLI capabilities](assets/videos/01_cli_capabilities.mp4) | Python, `mcp_cli.py` and the main capabilities: doctor, tools, watch, flow, scaffold, improve and apprentice. |
| [Local daemon status](assets/videos/02_daemon_status.mp4) | A filtered diagnostic: `client_exists`, `llm_available`, `daemon_running`, `daemon_status`, `daemon_port`, `tools_count` and `server_errors`. |
| [MINI_MCP_FLOW validation](assets/videos/03_flow_validation.mp4) | `flow list` and `flow validate` on `health_check_mini_mcp`, with nodes, edges, errors and warnings. |
| [Controlled dry-run](assets/videos/04_flow_dry_run.mp4) | `flow run --dry-run health_check_mini_mcp` and planned execution steps without running real actions. |

## Why request a demo?

A guided demo is useful if you want to see how MINI_MCP_CLIENT behaves on a real Windows setup before discussing deeper access.

Typical demo angles:

1. **Diagnose a local project**  
   Show how a LLM can inspect a project through the CLI / daemon / MCPClient path, with visible commands and results.

2. **Run a Windows/MCP workflow with proofs**  
   Validate or dry-run a workflow, inspect the planned steps, then review logs, status and structured output.

3. **Replay or explain a method with procedural memory**  
   Show how LLMApprenticeAgent can retrieve a validated procedure, explain why it applies, and keep proof stronger than confidence.

## What you will see in 5 minutes

The current public clips are designed to answer the first practical questions quickly:

- **Is there a real CLI surface?** See `mcp_cli.py`, available commands and capabilities.
- **Is the daemon actually running?** See local daemon status and tool count.
- **Can workflows be validated before execution?** See `flow validate`.
- **Can actions be planned without running them?** See controlled dry-run behavior.

The private walkthrough can then go deeper into diagnostics, workflow orchestration, watcher behavior, procedural memory, and the proof-first loop.

## Demonstrable capabilities

Depending on the private configuration used, MINI_MCP_CLIENT can expose capabilities such as:

- local file tooling;
- controlled Windows terminal execution;
- SQLite-backed state and proof queries;
- local workflow validation and dry-run;
- structured logs;
- automated test runs;
- execution watchdog;
- daemon diagnostics;
- MCP tool inventory;
- procedural memory through LLMApprenticeAgent;
- session supervision concepts: activation plans, trigger history and final reports.

These functions are still under private-beta validation. They are not presented here as a public production product.

## What this project is not

MINI_MCP_CLIENT is not:

- an AGI claim;
- a promise of magical autonomy;
- a replacement for human technical review;
- a guarantee of absolute safety;
- an enterprise-ready public platform;
- an open-source release of the full private runtime.

The public repository is intentionally limited. The complete runtime source code is not distributed here.

## Private beta status

The project is currently in private beta. Demos and technical evaluations are guided and scoped.

The public repository exists to:

- explain the concept;
- show safe terminal demonstrations;
- collect private demo requests;
- support technical conversations with developers, reviewers and early partners.

## Support development

MINI_MCP_CLIENT is currently a private-beta project. Optional support helps continue public demos, documentation, testing and technical validation.

[Support development](https://buymeacoffee.com/dbavotalecours)

Support is optional. It does not grant access to private source code, secrets, private prompts, internal runtime files or confidential implementation details.

## Learn more

- [Public overview](README_PUBLIC.md)
- [5-minute demo script](DEMO_5_MINUTES.md)
- [Private beta offer](PRIVATE_BETA_OFFER.md)
- [Publication safety checklist](PUBLICATION_SAFETY_CHECKLIST.md)
