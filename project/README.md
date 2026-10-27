mod is the master brand of mod:group, and its colour is blue: *blått signalerar ansvar, trygghet och inger förtroende*. This system is the look of mod's own web apps (the mod AI Portal, the AI Financeportal, AI / IT Admin and every app on their tiles), built on the brand manual *mod – Grafisk manual v1.0* (2024). One rule sits above the others: brand every deliverable from its first draft, and check this system before building, while building and again before shipping.

## Content fundamentals

**Language.** Swedish for everything staff read. An app that was specified in English (Publish Mod Artifact) stays English; either way, one language per page and per mail.

**Voice.** Human, warm and open (*Vi är mänskliga*). Plain and direct, addressing the reader as *du*: "Klicka på en ikon för att öppna." "Byggt något med AI? Lämna in det här." Say what a thing does for the reader, not how it was built.

**Casing.** Sentence case for titles, buttons and labels: "System & inloggningar", "Skicka in", "Senast hämtad". Capitals come only from the stylesheet, on eyebrows, badges, table headers and the tagline; never type them. No emoji in interface copy.

**Names.** "mod" is always lower case, also in "mod:group". The business areas are Concept, Construct, Service and Insikt, always in that order. The system is "NEXT", never "Vitec NEXT". Other products are written the way their makers write them: Fortnox, MYNT, Dalux, Power BI, Microsoft 365.

**Numbers and time.** Swedish formatting: `1 365 h`, `12,5 h`, `4 sep 2026` in prose and `2026-09-04` in tables. Every figure carries its period ("i september 2026", "senaste 30 dagarna"); a figure without one is not finished. Times are Stockholm time. Figures in tables and KPIs use tabular numerals.

**Identity.** Show a person's UPN (`fornamn@modgroup.se`), not their mail address: the UPN is what every permission and every Power BI RLS rule resolves.

**Security copy is a promise.** A score, a fact about what protects a page, or "Granskad <datum>" goes on screen only after it has been proven, and changes in the same commit as the posture it describes.

**Tagline.** *Built to inspire*, set as the Tagline pill. The business areas have their own lines: *Developed to inspire* (Concept), *Constructed to inspire* (Construct), *Digitalized to inspire* (Insikt), and *Tailored* or *Optimized to inspire*.

## Visual foundations

### Colour

- **Blue is mod.** `blue-1` (BLÅ 1, PMS 286) is the logo's colour and the strongest in the scale; `blue-1` → `blue-5` run from it to the palest tint. The hero is always `blue-1` → `blue-2` at 135° with the `hero-glow` light top-right, in both themes.
- **Surfaces and text.** `bg` is the page, `card` every panel, tile and bar, `card-2` and `bubble` the insets inside a card, `line` the hairlines. Text is `ink`; secondary text is `muted`; links and text actions are `link`. On the hero, text uses the `on-hero-*` tokens.
- **The lime lifts one thing.** `accent` (the manual's accent GRÖN 1, PMS 2296) marks the tagline, the security score, the avatar, the "Ny" badge and the single call-to-action. Never body text, never a large area. Text on it is `blue-1` or `accent-ink`. `accent-light` is the manual's paler second accent; `accent-2` is only the hover of an accent fill.
- **Complement colours** (`brown-1`–`4`, `slate-1`–`4`) give a quieter, earthier look and are shared by mod and every business area.
- **Business-area scales** (`purple-*` Insikt, `green-*` Construct, `red-*` Concept) belong to that area's own deliverables: its logo and typography take its own scale, while complement and accent colours stay shared. Never set one area in another's colour, never swap them. Service is internal support and uses mod blue; Kapitel's scale is not in the manual, so ask before giving it one.
- **Status.** `ok-*`, `warn-*` and `err-*` for feedback, `danger-*` for destructive buttons, `st-*` for workflow statuses and `pt-*` for portal badges. The words always carry the meaning; colour only repeats it.
- **Dark theme.** Every semantic token has a dark value; the brand scales, the hero and the lime do not change. Set `data-theme="dark"` on `<html>` (see *Themes* below).

### Type

- **Poppins** is the web face: the manual's specimen face and the free stand-in for the licensed **PP Pangram Sans**, which is used in external print and digital work. Arial is the fallback for internal documents where neither is available. The Poppins files ship with this system (`fonts/`); embed them rather than calling a font CDN, because a strict CSP blocks font CDNs and the page falls back to a system font without a sound.
- **Weights.** 800 ExtraBold for the hero title and big figures, 700 Bold for section titles, labels and buttons, 600 SemiBold for tile titles, links and quads, 500 Medium for captions, 400 Regular for text.
- **The scale** is in Typography: `display` 50px (fluid from 30px) for the one hero title, `headline` 34px for inner pages, `section-title` 22px, `tile-title` 16.5px, `body` 16px, `body-sm` 14px, `ui-text` 13.5px, `meta-text` 13px, `caption` 12.5px, and the uppercase labels `eyebrow`, `th-label`, `badge-label` and `tagline-label`. Line height is 1.55 for text and 1.05 for display.
- **Tracking.** -0.02em on display and figures, -0.01em on titles, +0.06em to +0.14em on capitals.

### Space and layout

- One content column: `.wrap`, at most `wrap-max` (1180px) wide, with `gutter` (28px) sides, `gutter-phone` (16px) on phones.
- **The page skeleton:** the Hero, then a NavBar or SearchBar overlapping it by 26px, then `main.wrap` with the SafetyBadge (when the page has no SecurityCard) and the sections, then the Footer.
- Tiles sit in `.grid`: `repeat(auto-fill, minmax(min(268px,100%), 1fr))` with `gap-lg` (16px) gaps. Sections are `section-gap` (40px) apart, each led by a SectionHead.
- Breakpoints: `bp-tablet` (1000px), where the chip and security card stop floating, and `bp-phone` (560px), where everything becomes one column. A page never scrolls sideways at 375px.
- Outside the browser, the manual's grids apply: A4 is 8 columns × 10 rows with 15mm side and 20mm top/bottom margins and a 4mm gutter; 1920×1080 is 12 columns × 10 rows with 80px side and 90px top/bottom margins and a 15px gutter. An optional 50 / 30 / 20 split gives harmony.

### Shape, depth and motion

- **Radii** are generous: `radius` (18px) for tiles, cards and table frames; `radius-bar` (14px) for the search bar, nav bar and security card; `radius-icon` (13px) for the tile icon square; `radius-sm` (12px) for small cards; `radius-control` (10px) for buttons, fields and alerts; `radius-pill` for everything that is a label.
- **Borders** are 1px `line`; dashed borders mean "not here yet" (the add tile, the up-next stage).
- **Depth** is two shadows: `shadow` at rest and `shadow-h` on a hovered tile, which also lifts 3px.
- **Motion** is short and eased: `dur-base` (0.16s) for tiles and icons, `dur-fast` (0.12s) for buttons, `dur-slow` (0.6s) for the progress fill. The only loop is the active stage's pulse. Everything stops under `prefers-reduced-motion`.

### States

- **Focus** is a solid 3px `focus` outline 2px outside the element; fields add a `focus` border and the `focus-ring` halo instead. On the hero, focus outlines are `accent`.
- **Hover** lifts (tiles 3px, buttons 1px) and deepens the fill.
- **Disabled** is `disabled-opacity` (55%); a tile for something not published yet is `soon-opacity` (72%).

### Imagery and the graphic element

- **The graphic element** is the mod logo scaled up so it bleeds off an edge. On the web it is the negative logo behind the hero, 560px wide at `glyph-opacity` (9%), off the bottom-right corner. In print it may be filled with colour, colour with multiply, an image, or drawn as an outline.
- **Photography** shows life, movement, warmth and people, and real building exteriors. Portraits and drawings may be colourised; selected images may take the rounded corner from the logo's shapes. The web apps use no photography.

## Logos

- The wordmark exists in three inks only: BLÅ 1 (`mod-logotyp-bla.png`), white (`mod-logotyp-neg.png`) and black (`mod-logotyp-svart.png`). Never another colour, never recoloured with a CSS filter, never set in a typeface as a stand-in.
- Blue on light grounds; white on the hero, on blue and in the dark theme; black for one-colour print. **A dark ground always needs the white file:** the blue one is still there but invisible, and nothing warns you.
- The business areas' logos (hierarchy 1, mod-led) put the mod blocks in black above the area's name in its colour 1: `concept-logotyp-hierarki-1.png`, `construct-…`, `insikt-…`. Use a lockup whole; never build one from two logos.
- Keep clear space around the logo; in print it is at least 15mm wide. It may sit in any of the four corners, or centred when it is large.
- `mod-app-icon.svg` is the portals' favicon and app icon.

## Iconography

- **Stroke icons**, drawn on a 24×24 grid: 1.8px strokes (the go-arrow 2.2px, search 2px), round caps and joins, no fills. Inline them as SVG so they take `currentColor`: 24px in the tile's icon square, 16px in buttons and the nav, 15px for the go-arrow. The set is in the Icons group.
- **Product logos** for systems made elsewhere (NEXT, Fortnox, Microsoft 365, Power BI) are the makers' own files, always on white; this system ships none of them.
- No emoji and no icon fonts.

## Themes

`tokens.css` keys the dark palette on `data-theme="dark"`. Follow the viewer's OS unless they chose, before the page paints:

```html
<script>
  (function () {
    var t = null;
    try { t = localStorage.getItem('mod-theme'); } catch (e) {}
    if (!t) t = matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light';
    document.documentElement.setAttribute('data-theme', t);
  })();
</script>
```

The sites hash their inline scripts in the Content-Security-Policy: add this script to the hash, or serve it as a file. Check every page in both themes before shipping it.

## Intentional additions

- `.search:focus-within` and `.nav a:focus-visible` give the search bar and nav links a visible focus state; the sites show none.
- `.warn` completes the alerts with HardwareAssetManager's warning colours; Publish Mod Artifact defines only ok and err.
- The components also accept their state from ARIA (`aria-current`, `aria-selected`, `aria-pressed`, `aria-sort`) as well as from the sites' classes.
- Table styles are scoped to `.tablewrap`, where the sites style every table.
- `.foot` keeps the page gutter. In the sites its padding overrides `.wrap`'s sides, so at some widths the footer text touches the screen edge.
- `info-top` has a dark value assigned by role (the sites that use it are light-only).
- `.hero--compact p.lead.trust` sets the trust line 12px under the lead at 14px. The sites put a trust line only on a full hero, where its -12px top margin takes back part of the lead's 26px; a compact lead has no bottom margin, so on a compact hero the line was pulled over the lead's last line (found on the NEXT Blueprint, 7 Oct 2026). On phones the gap stays 12px.

## Not synced

From the code, this system leaves out: the Microsoft 365 app launcher (it mirrors Microsoft's own menu), the dashboard styling of *mod Kommunikation* (its own neutrals and KPI stripes), MyTime's charts, rings and slicers, AI / IT Admin's panels and severity colours, and Publish Mod Artifact's message thread. The components are static HTML and CSS, as in the sites; there is no JavaScript bundle. PP Pangram Sans is not included: it is licensed and no font file for it exists in the sources.
