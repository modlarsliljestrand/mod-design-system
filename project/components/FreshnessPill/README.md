# FreshnessPill

A glass pill on the hero that says when the page's data was last fetched: an uppercase label, the time in bold, and how long ago.

- Use it on every page whose numbers come from a scheduled extract (an hourly notebook, a nightly job), so a stale page says so on its face.
- The consumer provides the timestamp, formatted `sv-SE` in `Europe/Stockholm` ("29 sep 2026 10:05"), and the age: "· för 12 min sedan", "· för 3 tim sedan", "· för 2 dygn sedan".
- Start it `hidden` and show it once the data has loaded; `[hidden]` is forced with `!important`.
- It sits under the lead and trust lines, 20px below them.
