# SearchBar

The portal's filter-as-you-type search: a white bar overlapping the hero by 26px, a search icon, a 16px input and a live count at the right end.

- Put `.wrap.toolbar` > `.search` right after the hero.
- Filter on title and description, case-insensitive, as the person types. The count reads "9 appar & system" unfiltered and "3 av 9" while filtering; when nothing is left, show the EmptyState "Inget matchar din sökning."
- The placeholder is `placeholder` ("Sök app eller system…"); give the input an `aria-label`.
- `.search:focus-within` rings the bar in `focus` with the `focus-ring` halo. This is an intentional addition: the sites set `outline:0` on the input and show no focus state.
- On phones the count hides.
