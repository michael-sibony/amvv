# Origine du code

Ce dépôt est une copie du code source d'[OpenCode](https://github.com/anomalyco/opencode)
(licence MIT, voir `LICENSE`), importée depuis le commit `6df0d5d` de `anomalyco/opencode`.

Modifications par rapport à l'original :
- Suppression de `.github/workflows/` (CI liée à l'infrastructure d'OpenCode).
- `vercel.json` : déploie l'interface web (`packages/app`) sur Vercel.
- `packages/app/src/entry.tsx` : si `VITE_OPENCODE_SERVER_HOST` est défini au build, l'interface hébergée vise ce serveur (ici `localhost:4096`).

## Démarrer

```bash
curl -fsSL https://bun.sh/install | bash   # OpenCode utilise Bun
bun install
bun dev                                      # lance OpenCode depuis les sources
```

Ensuite, dans OpenCode, `/connect` pour ajouter une IA (OpenRouter, Gemini, DeepSeek, GPT,
Claude, Ollama en local, etc.).

## Interface web hébergée (Vercel)

Le site Vercel n'héberge que l'interface. Le vrai travail (IA, fichiers, commandes) est fait
par OpenCode sur ton ordinateur. Pour l'utiliser :

```bash
bun dev serve --port 4096 --cors https://<ton-site>.vercel.app
```

Puis ouvre le site Vercel dans Chrome : il se connecte automatiquement à `http://localhost:4096`.
