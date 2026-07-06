# Démonstration privée en 5 minutes

Ce script sert à présenter MINI_MCP_CLIENT sans exposer le code source privé ni des données sensibles.

La démonstration doit rester sobre : montrer le couloir local MCP, le daemon, l’inventaire des outils et quelques surfaces de diagnostic.

## Video clips

Ces clips courts peuvent être utilisés comme aperçu public contrôlé. Ils ne montrent pas de clé API, token, fichier `.env`, log privé, base SQLite complète, prompt interne ou code source privé.

| Clip | Description |
| --- | --- |
| [CLI capabilities](assets/videos/01_cli_capabilities.mp4) | Shows Python, mcp_cli.py and the main capabilities: doctor, tools, watch, flow, scaffold, improve and apprentice. |
| [Local daemon status](assets/videos/02_daemon_status.mp4) | Shows a filtered diagnostic: client_exists, llm_available, daemon_running, daemon_status, daemon_port, tools_count and server_errors. |
| [MINI_MCP_FLOW validation](assets/videos/03_flow_validation.mp4) | Shows flow list and flow validate on health_check_mini_mcp with nodes, edges, errors and warnings. |
| [Controlled dry-run](assets/videos/04_flow_dry_run.mp4) | Shows flow run --dry-run health_check_mini_mcp and the planned execution steps without running real actions. |

## Avant de commencer

À dire clairement :

> MINI_MCP_CLIENT est en bêta privée. Cette démonstration montre la surface de pilotage et de diagnostic. Elle ne publie pas le code complet du runtime.

Utiliser un environnement propre, sans secrets visibles.

Adapter le chemin local :

```powershell
cd "$env:USERPROFILE\Documents\MINI_MCP_CLIENT"
```

Ne pas afficher :

- clés API ;
- logs privés ;
- base SQLite ;
- prompts privés ;
- rapports internes sensibles ;
- dossiers personnels ;
- captures contenant des données privées ;
- corrections réelles en direct ;
- commandes destructives.

## 1. Diagnostic général

Commande :

```powershell
.\.venv\Scripts\python.exe mcp_cli.py --json doctor
```

Ce que cela prouve :

- le projet sait diagnostiquer son environnement ;
- le daemon et les outils peuvent être détectés ;
- les fournisseurs LLM configurés peuvent être listés sans montrer leurs clés.

À dire dans la vidéo :

> Ici, je ne montre pas le code complet. Je montre seulement le diagnostic public du runtime local : état général, daemon, outils et configuration détectée.

À ne pas montrer :

- valeurs de clés API ;
- fichiers `.env` ;
- logs internes complets.

## 2. Démarrer ou confirmer le daemon local

Commande :

```powershell
.\.venv\Scripts\python.exe mcp_cli.py --json daemon --ensure --wait 90
```

Ce que cela prouve :

- le daemon local peut être démarré ou réutilisé ;
- le client garde un point d’entrée local stable ;
- le runtime évite de tout redémarrer à chaque commande.

À dire :

> Le daemon local est le cœur persistant. Il garde les connexions MCP prêtes et répond seulement depuis la machine locale.

À ne pas montrer :

- logs de démarrage détaillés s’ils contiennent des chemins ou données privées.

## 3. Vérifier l’état du daemon

Commande :

```powershell
.\.venv\Scripts\python.exe mcp_cli.py --json daemon --status
```

Ce que cela prouve :

- le daemon répond ;
- le nombre d’outils est visible ;
- le backend actif peut être identifié ;
- l’état est lisible par un humain ou un autre LLM.

À dire :

> Cette commande prouve que le couloir local est actif : CLI, daemon, MCPClient, outils.

## 4. Lister les outils MCP

Commande :

```powershell
.\.venv\Scripts\python.exe mcp_cli.py --json tools --detail
```

Ce que cela prouve :

- les outils locaux sont inventoriés ;
- les schémas d’entrée sont disponibles ;
- un LLM peut savoir comment appeler les outils sans deviner.

À dire :

> Le LLM ne doit pas improviser les outils. Il peut lire les schémas disponibles et travailler dans un cadre plus contrôlé.

À ne pas montrer :

- outils internes sensibles ;
- chemins personnels inutiles ;
- données de configuration privée.

## 5. Lister les workflows disponibles

Commande :

```powershell
.\.venv\Scripts\python.exe mcp_cli.py --json flow list
```

Ce que cela prouve :

- MINI_MCP_CLIENT peut organiser des actions sous forme de workflows ;
- le runtime ne se limite pas à une commande isolée ;
- l’ordre, l’état et les résultats peuvent être inspectés.

À dire :

> Les workflows permettent d’encadrer des séquences d’actions au lieu de laisser un agent agir sans structure.

À ne pas montrer :

- workflows privés sensibles ;
- détails internes non nécessaires.

## 6. Vérifier la mémoire procédurale

Commande :

```powershell
.\.venv\Scripts\python.exe mcp_cli.py --json apprentice stats
```

Ce que cela prouve :

- le système peut compter et inspecter des traces ou méthodes apprises ;
- la mémoire procédurale est traitée comme un objet vérifiable ;
- la démonstration reste sur des statistiques, sans exposer les contenus privés.

À dire :

> Cette partie sert à montrer l’idée de mémoire procédurale : garder des méthodes utiles, mais sans publier leur contenu privé.

## Conclusion de la démo

À dire :

> MINI_MCP_CLIENT n’est pas un remplaçant de Codex, Claude ou Gemini. C’est une couche locale MCP pour exécuter, tracer, tester et rejouer le travail d’agents IA avec des outils Windows.

Prochaine étape :

- proposer une démonstration privée plus ciblée ;
- proposer un diagnostic bêta ;
- vérifier si le cas d’usage du client est compatible avec le niveau actuel du projet.
