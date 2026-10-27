# Button

Actions: `.btn` is the primary (`btn-bg`, white label); `.secondary`, `.ghost`, `.accent` and `.danger` step down from it or aside; `.sm` is the compact size.

- One primary per view, for the thing the page is for. Sentence case, verb first: "Skicka in", "Spara", "Avbryt".
- `.accent` (lime with a `blue-1` label) is the call-to-action colour: at most once on a page, and the NavBar's `.cta` already counts.
- `.danger` (`danger-bg` / `danger-ink`) only for destructive actions, and confirm before them.
- Hover lifts 1px and darkens the fill; focus is a 3px `focus` outline; disabled is 55% opacity (`disabled-opacity`).
- An icon, if any, is a 16px stroke icon before the label.
- `.actions` groups buttons with 10px gaps and wraps.
