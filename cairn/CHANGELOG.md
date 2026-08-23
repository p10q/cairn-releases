# Cairn changelog

## 1.2.0 - 2026-08-22

- Added one shared timeline control for filtering activity, workspaces, live sessions, and session history by time range.
- Added a dedicated live-sessions section between the workspace list and session history.
- Made session history easier to scan with compact rows that expand into full details and actions.
- Added cumulative activity charts and a resizable expanded activity dashboard.
- Simplified workspace rows into a quieter departures-board layout with clearer section colors and improved light/dark appearance.
- Improved session coverage by including indexed sessions even when an agent did not write a summary artifact.

## 1.1.1 - 2026-08-22

- Made agent integrations explicitly opt-in, with Install, Update, and Repair actions for detected Claude Code and Codex installations.
- Added first-run and returning-user prompts for reviewing optional agent integrations without changing agent configuration automatically.
- Improved legacy hook detection and upgrades, and only offers the pi extension when pi is installed.
- Added a direct trial download action to the license window.
- Refined workspace panel colors and borders, and changed the default terminal theme to Builtin Light.

## 1.1.0 - 2026-08-17

- Replaced the five separate workspace views with one unified list beside the active terminal.
- Added fast terminal, list, and split pivots with Command-1 and Command-2, plus a draggable divider.
- Brought live activity totals and needs-your-attention alerts into the workspace list.
- Added per-workspace session history with prompts, results, observed files, agent-reported validation, duration, turns, tool use, and token metrics when available.
- Added inline saved transcripts and file-level Git diffs when captured.
- Improved remote session reliability by reconnecting automatically after attach backpressure.

