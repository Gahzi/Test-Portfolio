# Wireframe S664 — Static Clone

A lightweight, GitHub Pages–ready site inspired by Cargo's **Wireframe S664** template.

## Quick Start

1. **Create a repo** on GitHub named `<username>.github.io` (or any repo if you use Pages from `/docs`).
2. Upload this folder's contents.
3. Enable **GitHub Pages** in *Settings → Pages*:
   - **Source**: `main` branch
   - **Root**: `/` (or `/docs` if you move files there)
4. Visit `https://<username>.github.io/`

### Editing

- Replace images in `assets/` with your own.
- Update titles, links, and copy in `index.html`, `about.html`, and `projects/sample-project.html`.
- Tweak layout in `styles.css` (grid spans, gaps, max width).
- Duplicate `projects/sample-project.html` per project.

### Notes

- This is **not** an official Cargo theme, just a similar minimalist layout for static hosting.
- No build step. Pure HTML/CSS/JS.

## GitHub CLI one‑shot setup (recommended)

```bash
# 1) Install GitHub CLI: https://cli.github.com/
# 2) Authenticate once
gh auth login

# 3) Create a new public repo (change the name if you like)
gh repo create wireframe-s664 --public --source . --remote origin --push

# 4) Enable Pages and let the workflow deploy
gh api -X PUT repos/{owner}/{repo}/pages --input - <<< '{"source":{"branch":"main","path":"/"}}' || true

# 5) Check deployment URL
gh api repos/{owner}/{repo}/pages | jq -r '.html_url'
```

> Replace `{owner}` and `{repo}` above if your gh CLI does not auto-expand them.
