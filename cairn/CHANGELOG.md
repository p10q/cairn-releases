# Cairn changelog

## 1.2.4 - 2026-08-25

- Redesigned the workspace list with live sessions beside workspaces and a persistent side panel for faster navigation.
- Added a master-detail session history with keyboard navigation, clearer details, and more responsive incremental updates.
- Consolidated remote workspace management on Cairn's PTY service, including provisioning and session lifecycle controls.
- Improved remote reliability by restoring workspaces automatically and detaching cleanly when an SSH connection drops.

## 1.2.3 - 2026-08-24

- Improved list and session-history responsiveness by consolidating background polling and removing expensive transcript discovery from row refreshes.
- Added lightweight diagnostics for brief input delays, with activity attribution and stack sampling reserved for longer stalls.
- Improved dark-mode readability across the workspace list and activity views, and removed section tint backgrounds for a cleaner, more consistent panel.

## 1.2.2 - 2026-08-23

- Prevented overlapping background refreshes from building up while Cairn monitors busy workspaces and long-running agent sessions.
- Improved main-thread hang detection so reports use consistent samples and avoid false or stale diagnostics.

## 1.2.1 - 2026-08-23

- Made the shared timeline recent-first, defaulting to the last 12 hours while keeping plain shells and sessions without timestamps visible.
- Improved session-history responsiveness by virtualizing rows, especially for workspaces with many recorded sessions.
- Kept focus mode distraction-free by hiding the usage HUD while the terminal fills the window.
- Bounded live terminal analysis and made hang reports more accurate and responsive.
- Improved jump-host tunnel startup reliability by simplifying connection setup and retrying transient first-connection failures.

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

