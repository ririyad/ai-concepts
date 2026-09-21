# AI Atlas

A single-page field guide to **AI development terminology** — what each term means, how nearby concepts differ, and a course or paper that actually covers it.

**Live site:** [https://ririyad.github.io/ai-concepts/](https://ririyad.github.io/ai-concepts/)

## Local preview

Open [`index.html`](index.html) in a browser, or serve the folder:

```bash
python -m http.server 8080
```

Then visit `http://localhost:8080`.

## What’s inside

- **Concept map** — neighborhood graph for each term (left → right relationships), with definitions, examples, and aligned reading links
- **Guided path** — a structured walk through the glossary
- **In practice** — short system walkthroughs (e.g. RAG) with linked terms
- **Common mix-ups** — pairs people often conflate
- **Check yourself** — a lightweight self-quiz

Progress (“understood” marks) and theme preference stay in your browser only. No build step, no backend, no live model calls.

## Publishing

The site is a static `index.html` deployed with [GitHub Pages](https://pages.github.com/) via Actions (see `.github/workflows/deploy-pages.yml`). Pushes to `main` publish automatically once Pages is set to **GitHub Actions** under the repo’s Settings → Pages.
