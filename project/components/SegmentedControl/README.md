# SegmentedControl

The Dag / Vecka / Månad switch: a white pill of a few buttons with the chosen one solid blue.

- `div.seg[role=tablist]` of `button[role=tab]`; mark the chosen one `.on` and `aria-selected="true"`.
- Two to four options, one word each. It changes the view of the same data, so the views must reconcile: the days add up to the week and the weeks to the month.
- Full width on phones.
