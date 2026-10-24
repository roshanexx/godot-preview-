# Godot Mobile Preview

Public **web build only** for the private Godot 4.6 source project.

The playable site will be at:
https://roshanexx.github.io/godot-preview-/

## Initial setup
1. Create a fine-grained GitHub personal access token scoped **only** to `roshanexx/Godot-Engine-`, with **Contents: Read-only**.
2. In **this public repository**, go to Settings → Secrets and variables → Actions → New repository secret. Name it `GODOT_SOURCE_READ_TOKEN` and paste the token. Never commit the token or paste it in chat.
3. Go to Settings → Pages → Build and deployment → Source: **GitHub Actions**.
4. Run Actions → **Publish Godot Web Preview** → Run workflow. The site updates on a successful run.

This repository is public. Its workflow reads the private source using a read-only token, builds the game in GitHub Actions, and deploys only the exported Web files to GitHub Pages. **Godot web exports can still contain extractable assets and code**, so do not put secrets into game source or exported resources.

For now publishing is manual. An automatic update trigger can be configured later without making the private repository public.
