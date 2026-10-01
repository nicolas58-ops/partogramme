# Partogramme

Suivi du travail en salle de naissance : patientes, grossesses, examens (partogramme
avec courbe), enfants, praticiens, export Excel. Données 100 % fictives (TP).

## Lancer en local

Python n'est PAS installé sur ce PC : ne pas utiliser `python -m http.server`.
À la place, depuis le dossier `Projets/` (parent) :

```
node serveur-local.js partogramme 8000
```

(`serveur-local.js` est un petit serveur statique écrit avec Node, qui se trouve
dans le dossier parent.)

## Supabase

- Projet : `zvtpwfqlohcpgqfnclso` (les tables : `patiente`, `grossesse`, `examen`,
  `orientation`, `enfant`, `praticien`, toutes avec RLS ouverte car données fictives).
- `config.js` contient l'URL du projet et la clé publishable (clé publique, pas secrète).
  Ce fichier EST versionné : il faut le publier sur GitHub, sinon le site en ligne
  reste vide avec une erreur `supabaseUrl is required`. S'il manque (PC réinitialisé),
  le recréer avec `window.SUPABASE_URL` et `window.SUPABASE_KEY` (via MCP `supabase` :
  URL du projet + clé publishable).
- Le jeton d'accès personnel Supabase (pour le MCP) est dans `.mcp.json` du dossier
  parent (entête `Authorization`), pas dans ce dossier.