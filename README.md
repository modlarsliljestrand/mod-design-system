# mod Design System

The look of mod's own web apps: colours (light + dark), type, spacing, 27 components with
guidelines and previews, the logos, 33 stroke icons and the Poppins web font. Built on the brand
manual *mod – Grafisk manual v1.0* (2024).

**Start here → [project/README.md](project/README.md)** (the brand book).

This repo is a byte-for-byte copy of the design system kept on claude.ai
(<https://claude.ai/artifact/AaJDKCmidKnuiA6vHz5uLr>), mirrored 2026-10-27 from version
`1793009117-8e5b`. The files under `project/` are exactly the files published there; the logos and
icons, which claude.ai stores as uploads, sit under `project/assets/<Group>/` with the names the
system gives them.

## What is where

| Path | What |
|---|---|
| [`project/README.md`](project/README.md) | The brand book: content rules, colour, type, layout, logos, icons, themes |
| [`project/brand-architecture.md`](project/brand-architecture.md) · [`project/page-rules.md`](project/page-rules.md) | mod and the business areas · page rules |
| [`project/tokens.json`](project/tokens.json) | Every token value: 133 colours (light + dark), type styles, spacing, radius, shadow, motion |
| [`project/components/bundle.css`](project/components/bundle.css) | The stylesheet the components use (`.hero`, `.tile`, `.btn`, `.tablewrap` …) |
| [`project/components/<Name>/`](project/components) | One folder per component: `README.md` (guidelines) + `preview.html` (example markup) |
| [`project/fonts/`](project/fonts) | Poppins Latin woff2, 400–800 + 400 italic |
| [`project/assets/Logos/`](project/assets/Logos) | The mod wordmark (blue, white, black), business-area lockups, app icon |
| [`project/assets/Icons/`](project/assets/Icons) | 33 stroke icons, 24 × 24 |
| [`project/design-system.json`](project/design-system.json) | The system's index on claude.ai |
| [`MANIFEST.sha256`](MANIFEST.sha256) | SHA-256 of every mirrored file |

The previews are fragments: on claude.ai they render with the generated `tokens.css`, the fonts and
`bundle.css` already loaded, so opened on their own they show unstyled.

## Using it from Claude Code

Point Claude at this repo and have it read `project/README.md` first, then `project/tokens.json` and
`project/components/bundle.css`. In a Claude Code on the web session, clone it next to your work:

```bash
git clone --depth 1 https://github.com/modlarsliljestrand/mod-design-system.git /tmp/mod-design-system
```

## Check that it is unchanged

```bash
sha256sum -c MANIFEST.sha256
```

## Rights

The mod name, logos and brand are mod:group's; they are published here for reference, not under an
open licence. Poppins is © The Poppins Project Authors under the SIL Open Font License 1.1
([`project/assets/Fonts/Poppins-OFL.txt`](project/assets/Fonts/Poppins-OFL.txt)).
