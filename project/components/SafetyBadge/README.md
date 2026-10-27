# SafetyBadge

The page-level safety badge: one compact row high on the page with the honest score, two to four concrete facts about what protects it, and the review date.

Every site, app or dashboard built for mod carries one: under the intro, above the content. A page with a hero may carry the SecurityCard there instead.

**It is a promise**, under the same rules as the SecurityCard: the score is the honest close-out rating, every fact is proven (trigger the control and read the log back before claiming it), and a change in posture updates the badge and its date in the same change.

- `.shield`: a 32px `ok-bg` square with the shield icon in `ok-ink`.
- `.score`: "Säkerhet **9/10**", the number in `ok-ink`.
- `.facts`: 2–4 `span`s, each after a small `ok-ink` dot. Name the mechanism: "Entra-låst till ekonomigruppen", "Externa konton blockerade", "Endast aggregerad statistik – ingen PII".
- `.rev`: "Granskad 5 sep 2026", pushed to the right end.
- Not reviewed yet: add `unreviewed` to `.score` and write "Säkerhet: ej granskad ännu" (a `warn-bg` pill with `warn-ink` text). Never show a number that has not been reviewed.
- Below 760px the date wraps under the facts. Check the row at 1024px too: a long fact widens it.
