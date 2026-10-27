# StatusPill

A workflow status as an uppercase pill with a dot in its own ink: submitted, in_review, approved, building, published, rejected.

- `span.status.<status>`; each status has its own `st-<status>-bg` / `st-<status>-ink` pair, contrast-checked in both themes.
- `building` is the only solid pill: work is happening now.
- The word carries the meaning; the colour only repeats it.
- Only for a status standing on its own. Never put the `status` class on a timeline row or a card: that turned every row into a pill and put grey text on the solid Building blue (1.28:1).
