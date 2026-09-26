# AI Atlas

A single-page, plain-language field guide to **AI terminology** — 105 concepts from “what is a model?” to inference, RAG, agents, and skills. Each term explains what it means in everyday words, how it connects to the others, how nearby terms differ, and links a course, paper, or official guide that actually covers it.

**Live site:** [https://ririyad.github.io/ai-concepts/](https://ririyad.github.io/ai-concepts/)

## Local preview

Open [`index.html`](index.html) in a browser, or serve the folder:

```bash
python -m http.server 8080
```

Then visit `http://localhost:8080`.

## What’s inside

- **Start here** — a landing page for newcomers: look up a word you heard, a 60-second primer (“AI in five ideas”), and three ways in
- **A–Z glossary** — every term with a one-line explanation, filterable by level (Essential · Good to know · Deep dive) and jumpable by letter
- **Concept map** — neighborhood graph for each term (left → right relationships). Every entry is layered: plain words, an analogy, an everyday example, and why it matters first; switch to *In depth* for the precise definition, a real-system example, a distinction worth keeping, and aligned reading. Mentions of other terms are linked, with a hover preview
- **Guided path** — 14 short steps through the essentials, plus deep dives grouped by topic
- **In practice** — eight walkthroughs, from what happens when you chat with AI to how a coding agent uses skills and tools
- **Mix-ups** — 27 pairs people often conflate (model vs chatbot, skill vs tool, jailbreak vs prompt injection…)
- **Quiz** — an essentials quiz in plain words, or a full quiz across every concept

Search understands everyday words and product names (“ChatGPT”, “run AI on my laptop”, “what is a skill”). Views and concepts have shareable links (`#glossary`, `#inference`). Progress (“understood” marks), theme, and reading depth stay in your browser only. Self-hosted fonts live under `assets/fonts/`. No build step, no backend, no live model calls.

## Editing the content

Everything lives in `index.html`. Inside the `<script>`: `DATA` holds one concept per line (plain-language layer, technical layer, level, aliases, search keywords, and `refs` into `SOURCES`); `E` holds the relationship edges; `PATH`, `FLOWS`, `COMPARES`, and `IDEAS` drive the guided path, walkthroughs, mix-ups, and primer; `XREF` lists the phrases that become inline links to a concept.

## Publishing

The site is a static `index.html` deployed with [GitHub Pages](https://pages.github.com/) via Actions (see `.github/workflows/deploy-pages.yml`). Pushes to `main` publish automatically once Pages is set to **GitHub Actions** under the repo’s Settings → Pages.
