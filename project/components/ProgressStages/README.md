# ProgressStages

Where a request stands: a filled progress track, then one card per stage: done (✓ on green), in progress (a pulsing blue dot), up next (dashed), not reached yet, or stopped (✕ on red).

- `.progress` > `.progress__bar[role=progressbar]` > `.progress__fill` (its width is the percentage; `.rejected` fills red, `.published` green), then `ol.stages` of `li.stage.<state>`: `done`, `active`, `next`, none, or `stopped`.
- Each stage: `.stage__dot` (✓ done, ✕ stopped, else its number), `.stage__label`, `.stage__when` (the time it was reached, "In progress", "Up next" or "Skipped"), and optionally `.stage__notes` with the note written when the request moved into it.
- Five stages in a row; one column under 760px. The active stage carries `aria-current="step"`.
- A rejection freezes the bar where it stopped, in red.
- The pulse stops under `prefers-reduced-motion`.
