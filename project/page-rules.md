# Rules for every mod page

These hold for every site, app and dashboard built for mod, on top of the tokens and components.

1. **Branded from the first draft.** Start from these tokens, the Poppins files and the real logo files. Never build a neutral version and brand it later.
2. **Both themes.** Every colour comes from a token; the page works with `data-theme="light"` and `"dark"`, and it is looked at in both before it ships.
3. **A safety badge on the page.** A SecurityCard on the hero or a SafetyBadge above the content: the honest score, two to four proven facts, the review date. Change it in the same commit as the posture it describes. Re-dating it re-claims every row.
4. **Every table sorts.** A `th` with `aria-sort` and a real button; it sorts on the value the cell shows.
5. **Figures carry their period and their source.** "12,5 h i september 2026". Scheduled data shows when it was fetched (the FreshnessPill). Times are Stockholm time.
6. **Phone first-class.** No sideways scroll at 375px; the hero's chip and card collapse to one row each so the title is visible without scrolling.
7. **Identity is the UPN.** Show and pass the UPN, and write anything that came from a token with `textContent`, never `innerHTML`.
8. **Empty is said, not shown blank.** An EmptyState sentence, or "–" with a note; never a 0 that means "unknown".
9. **Real names.** NEXT (never Vitec NEXT), the companies in the order Concept, Construct, Service, Insikt, products as their makers write them.
10. **No borrowed chrome.** Product logos only as the makers' own files on white; no copies of another company's interface.
