# KPI

A card for one headline figure: an uppercase muted head, the figure at 26px ExtraBold on the same line, and a note that says what the figure covers.

- `.kpis` holds three `section.card.kpi`; it becomes one column under 900px.
- `.kpi__hd` > `h3` (the eyebrow) + `.kpi__big` (the figure, `kpi-figure`); then `p.kpi__note`.
- **State the period with the number**: "i september 2026", "senaste 30 dagarna". A figure without its period is not finished.
- Numbers are Swedish: a space between thousands, a decimal comma, the unit after a space ("12,5 h").
- For one big figure inside a card use `.bignum`: `b` (32px ExtraBold in `link`), a `span` for the unit, and an `i` aside pushed to the right end.
- A card whose data is missing says so in its note ("Ingen tid i perioden.") and shows "–" as the figure; it never shows 0 for "unknown".
