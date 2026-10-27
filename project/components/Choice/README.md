# Choice

Radio or checkbox options as bordered cards: a bold label and a short explanation, with the checked card ringed in `focus`.

- `.choices` (two columns; `.three` for three; one column under 700px) of `label.choice` > `input` + `span.choice__txt` > `b` + `small`.
- Use it when each option needs a sentence of explanation (which portal, which category); a plain select or radio list otherwise.
- The checked card gets the `focus` border and `focus-ring` halo; keyboard focus adds a 2px `focus` outline.
