# Unified Smart Tags — V1 Prototype

Interactive prototype for Pendulum's unified Smart Tags & Categories management experience.

One library of categories shared across **Influencer Vetting**, **Influencer Monitoring**, and **Smart Alerts**, organized by **folder** (use case) and **label** (cross-cutting).

## What it shows

- **Three layouts**, switchable via the segmented control:
  - **Folder tree** — folder sidebar + table with Folder / Labels / "Used in" columns
  - **Grouped** — collapsible folder sections with label-chip filtering
  - **Board** — folders as columns, tags as draggable cards
- **Foldering** by use case + cross-cutting **labels** as faceted filters
- **"Used in"** V / M / A indicators per category (Vetting / Monitoring / Alerts)
- **Preview tag picker** — modal showing the same categories reused across all three surfaces

## Run it

It's a single static file with no dependencies. Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

> Prototype only — buttons like "New folder" / "New smart tag" are stubs that describe the intended dialog.
