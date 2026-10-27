# Hero

The mod-blue band that opens every portal-family page: logo, who is signed in, the security card, one title, one lead and the tagline.

**Use** it once, first in `<body>`. A portal's home page takes `.hero`; an inner app page takes `.hero.hero--compact` (a 34px title, a 15px lead, no tagline, tighter padding) and may add an app tag after the logo.

**The ground never changes.** BLÅ 1 → BLÅ 2 at 135° with the `hero-glow` light in the top-right corner, in the light *and* the dark theme. Text on it uses the `on-hero-*` tokens, never `ink` or `muted`; lime `accent` is the only other colour on it.

**The consumer provides**
- the negative logo (`assets/Logos/mod-logotyp-neg.png`) twice: `img.logo` (34px high, `alt="mod"`) in `.brandleft`, and `img.hero__glyph` (`alt=""`): the manual's graphic element, the logo scaled up to 560px at `glyph-opacity`, bleeding off the bottom-right edge
- on inner pages, `span.apptag` after the logo: the app's name, set in capitals by the class
- a UserChip and a SecurityCard inside `.brandmeta`, which floats top-right from 1000px up and stacks under the logo below that
- `h1` (at most 16 characters wide), one `p.lead` (at most 60ch), optionally one `p.lead.trust` line with the lime rule, and on a home page the Tagline

```html
<header class="hero">
  <img class="hero__glyph" src="mod-logotyp-neg.png" alt="">
  <div class="wrap hero__inner">
    <div class="brandrow">
      <div class="brandleft"><img class="logo" src="mod-logotyp-neg.png" alt="mod"></div>
      <div class="brandmeta"><!-- UserChip, SecurityCard --></div>
    </div>
    <div class="hero__copy"><h1>…</h1><p class="lead">…</p><p class="lead trust">…</p></div>
    <span class="tagline">Built to inspire</span>
  </div>
</header>
```

**Don't** put buttons, search or content cards on the hero: the NavBar or SearchBar sits under it and overlaps it by 26px. Don't recolour it for a business area; an AO's colour belongs in the content, the hero stays mod blue.
