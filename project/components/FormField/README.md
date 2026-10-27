# FormField

Labelled inputs, selects and textareas: a 13px SemiBold label, a hint in `muted`, a red required star, and an inline error under the control.

- `.form` stacks fields 16px apart; `.form .row` puts two side by side (one column under 700px).
- `.field` > `label` (with `span.req` "*" for required) + the control + `span.hint` or `span.ferr`. Group radios and checkboxes in `fieldset.field` with a `legend`.
- Controls: `field-bg`, a `field-line` border, 10px corners, 14.5px text, `placeholder` for the placeholder. Focus: a `focus` border and a 3px `focus-ring` halo.
- The resting border is below 3:1 against the field in both themes; that is the code's value, kept. Always give a field a visible label, and mark an error with words (`ferr`) and `aria-invalid`, never colour alone.
- Checked radios and checkboxes take `btn-bg` as their accent colour.
