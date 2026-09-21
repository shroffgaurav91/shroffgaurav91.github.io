# tools/

Source for personal tools that are **not** part of the published website.
`_config.yml` excludes this directory from the Jekyll build, so nothing here
is served from shroffgaurav91.github.io.

## on-my-plate.html

A quick-capture inbox for tasks other people hand you — "look into this IPO",
"order groceries" — so they can be written down in one gesture from whichever
device is nearby, instead of opening a document and navigating to the right spot.

Hosted as a **private Claude artifact**, not on the public site. Capture data
lives in the artifact's own database, never in this repository.

- One text box, fixed to the bottom of the screen (thumb reach on a phone).
- Enter saves. Pasting a multi-line list creates one item per line, and strips
  `-`, `*` and `1.` bullet prefixes.
- Items are auto-sorted into Money / Errand / Home / Work / Other by keyword;
  tap the category chip on any row to cycle it.
- Grouped by capture day (Today / Yesterday / weekday / date).
- Syncs live across devices via the `db` capability. If `db` is unavailable the
  page falls back to `localStorage` and says so in the header rather than
  pretending to sync.

To redeploy after editing, publish this file to the existing artifact URL rather
than as a new one, so the URL and its stored items are preserved.
