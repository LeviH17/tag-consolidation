# In-app mock (`in-app-mock.html`)

A second, complementary prototype of the Tag Manager — this one drawn **inside the real app shell** rather than as a standalone page.

Open `in-app-mock.html` in a browser. No dependencies; fonts are embedded.

## Why this one exists

`index.html` (on `main`) is the deeper exploration of the tag-management UX itself: three tag kinds, three layouts (folder tree / grouped / board), labels, and "Applied to" badges with per-surface counts.

This file answers a different question — **what the screen looks like as a page of the actual product**:

- The real **main sidebar** from `pendulum-webapp-next`, with the new menu item in place (top level, after Alerts) so nav placement can be judged in context.
- The standard **page anatomy** every screen inherits: page header with actions, filters bar, widget/table grid.
- The **Brand Dashboard** rendered alongside it (switchable from the sidebar) so the new screen can be compared against an existing one for visual consistency.
- Styling uses the **actual design tokens** from `src/webapp/styles/globals.css` — the same semantic colors, chart palette, radii, and Inter type scale, in both light and dark themes.

## What's interactive

- **Sidebar** — switch between Tag Manager and Brand Dashboard.
- **Tabs** — Categories / Dashboard Tags.
- **Filters** — Type, Criticality, Used in, Owner, plus free-text search and folder-rail scoping. They combine, update the row count, show a "Clear filters" affordance, and render an empty state when nothing matches.
- **Selection** — per-row checkboxes, select-all-visible, and a bulk action bar. Rows filtered out are deselected so the count reflects what a bulk action would actually touch.

Buttons that would open dialogs (New Folder, New Category, row kebabs) are stubs.

## Known gaps vs `index.html`

This mock does **not** yet include labels (cross-cutting tagging), the alternate layouts, or per-surface instance counts on the "Used in" chips. Where the two disagree, `index.html` is the more considered treatment of the tag-management UX; this file is the more considered treatment of how it sits in the app.

Terminology also differs and needs reconciling: this mock uses **Categories** / **Dashboard Tags** for two kinds, where `index.html` uses **Regular Tags** / **Search Categories** / **Influencer Risk Categories** for three.
