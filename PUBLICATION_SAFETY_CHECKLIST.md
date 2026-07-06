# Checklist de sécurité avant publication

Cette checklist doit être utilisée avant toute mise à jour publique de la vitrine MINI_MCP_CLIENT.

Objectif : protéger le vrai projet privé, les secrets, les données locales et les promesses commerciales.

## Secrets et accès

- [ ] Aucune clé API.
- [ ] Aucun token.
- [ ] Aucun mot de passe.
- [ ] Aucun fichier `.env`.
- [ ] Aucun secret copié dans un exemple.
- [ ] Aucun lien privé ou URL de tunnel temporaire.

## Données privées

- [ ] Aucun log privé.
- [ ] Aucune base SQLite.
- [ ] Aucun rapport interne sensible.
- [ ] Aucun prompt privé.
- [ ] Aucune mémoire procédurale privée.
- [ ] Aucun fichier runtime du vrai projet.
- [ ] Aucun dossier personnel sensible.
- [ ] Aucun chemin personnel inutile.

## Images et captures

- [ ] Aucune capture contenant des clés, emails, noms de clients ou données privées.
- [ ] Aucune capture de base de données.
- [ ] Aucune capture de prompts internes.
- [ ] Aucune capture de logs complets.
- [ ] Aucune capture de fichiers privés.

## Code et configuration

- [ ] Ne pas publier le code source complet de MINI_MCP_CLIENT.
- [ ] Ne pas ajouter de fichiers runtime.
- [ ] Ne pas ajouter de GitHub Actions.
- [ ] Ne pas ajouter de licence open source par accident.
- [ ] Ne pas ajouter de fichiers binaires.
- [ ] Ne pas ajouter de fichiers de cache.
- [ ] Ne pas ajouter de dossiers générés.

## Démonstrations

- [ ] Les commandes montrées sont non destructives.
- [ ] Les sorties sont filtrées si elles contiennent des chemins ou données privées.
- [ ] Les corrections réelles en direct ne sont pas montrées sans préparation.
- [ ] Les données affichées sont adaptées à une vitrine publique.

## Positionnement public

- [ ] Ne pas promettre une AGI.
- [ ] Ne pas promettre une autonomie totale.
- [ ] Ne pas dire que MINI_MCP_CLIENT remplace Codex, Claude, Gemini ou Qwen.
- [ ] Ne pas promettre une sécurité absolue.
- [ ] Ne pas dire que le projet est production-ready enterprise.
- [ ] Ne pas inventer des fonctionnalités non confirmées.

## Formulations préférées

Utiliser :

- bêta privée ;
- runtime local MCP ;
- démonstration privée ;
- évaluation technique encadrée ;
- accompagnement limité ;
- code complet non public ;
- projet en validation terrain.

Éviter :

- AGI ;
- autonomie complète ;
- corrige tout automatiquement ;
- sécurité garantie ;
- remplacement des grands LLM ;
- open source complet.

## Dernière vérification

Avant publication :

- [ ] relire tous les fichiers Markdown ;
- [ ] vérifier qu’aucun fichier sensible n’est ajouté ;
- [ ] vérifier le diff Git complet ;
- [ ] vérifier que le message reste sobre et réaliste ;
- [ ] publier en branche ou pull request, pas directement sur `main`.
