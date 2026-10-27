# DataTable

A table in a card frame whose every column sorts: uppercase muted headers on `card-2`, 11px / 14px cells, a hairline between rows and a hover tint.

**Every table is sortable.** Each `th scope="col"` carries `aria-sort` (`ascending`, `descending` or `none`) and holds a real `button.thbtn`, so it sorts on click, Enter and Space. The arrow reads ⇅ unsorted and ▲ / ▼ on the sorted column (`th.sorted`). Sort on the value the cell shows: a status in workflow order, a date as a date, a number as a number.

- Wrap the table in `.tablewrap`: it frames it like a Card and scrolls sideways inside its frame on phones. Its `position:relative` keeps visually-hidden labels in the table from widening the page.
- Link a row's name with `a.rowlink`. Numbers and times go in `td.num` (tabular numerals, no wrapping).
- Times are Stockholm time; an amount carries its period in the header or the caption.
- These rules are scoped to `.tablewrap`; the sites style every `table` on the page.
