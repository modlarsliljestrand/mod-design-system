# Tile

The portal's link card: an icon square, a title, a three-line description and an "Öppna ↗" go-link, where the whole card is the link.

- **Link tile** `a.tile`: hover lifts it 3px, the border turns `focus`, the shadow becomes `shadow-h`, the icon square turns BLÅ 2 → BLÅ 1 with a white icon, and the arrow nudges up-right. Focus is a 3px `focus` outline.
- **Badge**: one Badge as the last child pins to the top-right corner: `new` "Ny", `soon` "Kommer snart", `info` "Status".
- **Not published yet** `div.tile.soon`: 72% opacity, a grey icon square, "Publiceras snart" instead of "Öppna". The fade takes its description to 3.0:1 in light: fine for an inactive tile, never for one that links.
- **Notice** `div.tile.info`: a driftstatus note, not a link; `blue-4` border and a solid blue icon square.
- **Placeholder** `div.tile.add`: dashed, transparent, centred.
- **Several targets** `div.tile.tile--split`: when a tile leads to one place per company, the description and go-link give way to `.quads`, and each `a.quad` is a link. The outer element is a `div` (never an `<a>` around `<a>`), so the grid still sizes it like its siblings. The company order is always Concept, Construct, Service, Insikt. `.quads--icons` with `a.quad.quad--icon` shows product logos in a row of three; the name goes in `title` and `aria-label`.
- **Product logo** `.tile__icon--brand`: the product's own logo on white (logos never sit on dark blue, so it stays white on hover and in the dark theme); add `--wide` for a wordmark such as the mod logo.

**The consumer provides** the icon (a 24px stroke icon from the Icons group, inline so it takes `currentColor`) or a product logo (the product's own file; this system ships no third-party marks), a title of one to three words, a description of one or two sentences (clamped at three lines; the full text goes in `title`), and the URL. External links open in a new tab with `rel="noopener"`; the portal's own sub-pages open in the same tab.

Lay tiles out in `.grid`: `repeat(auto-fill, minmax(min(268px,100%),1fr))`, 16px gaps; rows stretch, so every tile in a row is the same height.
