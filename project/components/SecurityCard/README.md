# SecurityCard

The hero's security card: the honest overall score out of 10 in lime, a ten-segment bar, three to five scored rows and the date of the review.

**It is a promise.** Every number on it matches the latest security review. When the posture changes (a group widened, a Conditional Access policy disabled, headers drifting, a secret added) change the card and its date in the same commit. Re-dating the card re-claims every row: re-verify all of them, or keep the old date. Never ship the example's numbers.

- `.sec__head`: the shield icon (in `accent`) and *Säkerhetsnivå*.
- `.sec__score`: `.sec__num` (the score, `score-figure`), `.sec__den` "/10", `.sec__lbl` "Samlad säkerhetsnivå".
- `.sec__bar`: ten `<i>`, one `.on` per point.
- `.sec__list`: one `li` per axis, a label and a `b` score; the lime tick is drawn by the class.
- `.sec__foot`: "Säkerhetsgranskad 4 sep 2026" (day, short month, year).
- Give it `role="note"` and an `aria-label` that names the app.
- On phones it becomes one row: the score and the review date stay, the bar and rows hide.
- Contrast: from 1000px up the card floats into the hero's glow, where *Samlad säkerhetsnivå* measures 3.8:1 and the footnote 4.2:1 on the glass (the code's values, kept). The score and the rows pass.
- A page without a hero carries the SafetyBadge instead.
