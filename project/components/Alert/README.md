# Alert

An inline message for the result of an action, or a state the reader must know: `.ok` for success, `.warn` for a warning, `.err` for an error.

- 14px text in a box with 10px corners and its own fill, ink and border tokens (`ok-*`, `warn-*`, `err-*`). Put it where the action happened, above the form or list.
- Say what happened and what to do next, in one or two sentences. The words carry the status; colour only repeats it.
- `role="status"` for ok and warn, `role="alert"` for errors.
- `.warn` takes its colours from HardwareAssetManager's warning tokens; PublishModArtifact defines only ok and err.
