# mod Design System — public mirror

A byte-for-byte public copy of the mod Design System kept on claude.ai
(<https://claude.ai/artifact/AaJDKCmidKnuiA6vHz5uLr>), so any session (Claude Code on the web
included) can read it from GitHub: `https://github.com/modlarsliljestrand/mod-design-system`.

## Using it

When building anything mod-branded, read `project/README.md` first (the brand book), then
`project/tokens.json` for exact values and `project/components/bundle.css` + the component folders for
markup. Embed the fonts from `project/fonts/` rather than a font CDN. Logos are in
`project/assets/Logos/` (white file on dark grounds); icons in `project/assets/Icons/`.

## Rules for this repo

- **claude.ai is the source; `project/` is a mirror.** Never edit a file under `project/` here. Change
  the system on claude.ai, then re-mirror: read every `project/` path and every asset (the asset
  store's ids map to names through `project/design-system.json` → `assetGroups`), copy byte-for-byte
  to `project/` and `project/assets/<Group>/<name>`, regenerate `MANIFEST.sha256`.
- **Done = identical.** `sha256sum -c MANIFEST.sha256` passes locally AND every file fetched
  anonymously from `raw.githubusercontent.com` matches the manifest.
- `.gitattributes` is `* -text`: git must never rewrite line endings, or the copy stops being exact.
- Only the system's own files belong here. The claude.ai viewer (`index.html`, `SKILL.md`,
  `artifact-type/`) is Anthropic's Design System type, not part of this system.
- Public repo: no personal data, no internal hostnames, no secrets. Commits use the GitHub noreply
  address.
