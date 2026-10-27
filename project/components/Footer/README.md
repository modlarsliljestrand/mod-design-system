# Footer

The page foot: the blue mod logo and "<app> · byggd med Claude" on the left, a small muted link under it, and "Senast uppdaterad" with a contact link on the right.

- `footer` > `.wrap.foot` > `.footleft` (`.made` with the 20px logo and the line, then an optional `a.footlink`) and a right-hand `div`.
- The logo is the blue wordmark on light (`img.logo-on-light`) and the negative one on dark (`img.logo-on-dark`); the stylesheet swaps them under `[data-theme="dark"]`. Always carry both.
- The date is ISO (`2026-09-04`) in bold; links are `link`, SemiBold.
- The contact is a person or a mailbox the reader can write to; say who, not just "kontakt".
- On phones it stacks to one column.
