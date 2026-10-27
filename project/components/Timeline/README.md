# Timeline

The history of a record, newest first: a vertical hairline with a dot per event, blue for a status change, green for published, red for rejected, grey for anything else.

- `ol.timeline` of `li.tl-<kind>` (plus `tl-<status>` on status rows) > `.tl__head` (the event in bold, the actor in `.muted`, `.tl__when`) and an optional `p.tl__notes`, which keeps line breaks.
- Rows carry their own `tl-` classes, never the StatusPill's `status` class.
- Times are Stockholm time, tabular.
