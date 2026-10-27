# NavBar

The app's page navigation: a white bar that overlaps the hero by 26px, with pill-shaped links, the current page solid blue and at most one lime call-to-action.

- Put `.wrap.navbar` > `nav.nav` right after a compact hero.
- Mark the current page `.active` and `aria-current="page"` (`nav-active-bg` / `nav-active-ink`); hover is `nav-hover-bg` / `nav-hover-ink`; resting links are `muted`, 14px SemiBold.
- A link may lead with a 16px stroke icon from the Icons group.
- A `span.spacer` pushes the call-to-action (`.cta`: `accent` with `blue-1` text) to the right end. Use it for the one thing the app is for.
- On phones the spacer goes and the links tighten, so the bar wraps to two rows rather than four.
- Link focus is a 3px `focus` outline (an addition: the source leaves it to the browser).
