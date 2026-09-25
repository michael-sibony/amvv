# Origine du code

Ce dépôt est une copie du code source d'[OpenCode](https://github.com/anomalyco/opencode)
(licence MIT, voir `LICENSE`), importée depuis le commit `6df0d5d` de `anomalyco/opencode`.

Modifications par rapport à l'original :
- Suppression de `.github/workflows/` (CI liée à l'infrastructure d'OpenCode).
- Ajout de `public/index.html` et `vercel.json` (page statique pour le projet Vercel existant).

## Démarrer

```bash
curl -fsSL https://bun.sh/install | bash   # OpenCode utilise Bun
bun install
bun dev                                      # lance OpenCode depuis les sources
```

Ensuite, dans OpenCode, `/connect` pour ajouter une IA (OpenRouter, Gemini, DeepSeek, GPT,
Claude, Ollama en local, etc.).
