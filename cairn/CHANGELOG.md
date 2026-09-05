# Cairn changelog

## 1.5.0 - 2026-09-05

- Added adjustable screen-band layouts and moved Accessibility-based window scanning and placement off the main thread for smoother window management.
- Added a system watchdog and expanded the resource monitor with sustained per-process history, launch-aware tracking, and guarded process controls.
- Added context-aware workspace creation from iOS and new session actions for opening or forking work into a split or workspace.
- Improved iOS Remote reconnect behavior, SSH tunnel recovery, workspace navigation, and foreground resume reliability.
- Made the managed-window shelf collapsible and consolidated browser controls under the Window menu.
- Updated the upstream terminal engine with broad search, clipboard, rendering, memory-use, compatibility, and reliability improvements.

## 1.4.4 - 2026-09-03

- Added remote workspace preflight checks, automatic reconnects, and actionable recovery controls when a host, setup, or working directory needs attention.
- Added live remote-session inventory with filtering, workspace opening, and controls for stopping individual or grouped sessions.
- Improved remote terminal reliability by preserving in-flight input during reconnects, validating keeper startup, and fixing process and pipe cleanup edge cases.
- Improved performance across workspace activity and session history by coalescing refreshes, caching repeated parsing and formatting work, and reducing unnecessary polling.
- Refined accessibility, typography, spacing, empty states, and keyboard behavior throughout the workspace, history, onboarding, and remote-host interfaces.

## 1.4.3 - 2026-09-03

- Improved the workspace sidebar on narrow screen bands by stacking crowded sections, wrapping controls, and using the available vertical space.
- Fixed temporary overlap when opening the Activity dashboard and kept workspace, live-session, and utility regions from drawing over one another.
- Kept managed-app icons and screen-band controls accessible at the bottom of narrow sidebars.
- Replaced automatic window rearrangement with explicit layout presets, so Cairn only moves windows when you choose a layout.
- Fixed screen-band positioning when the Dock auto-hides and macOS temporarily stops reporting its frame.

## 1.4.2 - 2026-08-30

- Fixed copy and paste between terminal splits by keeping the clicked pane's focus synchronized and routing context-menu actions to the pane that opened the menu.
- Added a distinct recoverable interruption state for agent stream disconnects, which clears automatically when visible work resumes.
- Improved screen-band window ordering across reflows, Dock changes, shelving, and drag swaps.
- Hardened iOS remote reconnect and frame-receive concurrency during network transitions.

## 1.4.1 - 2026-08-30

- Added inline canvas controls for managed windows and Dock visibility, with clearer active states and a new Cairn icon for Stay Awake.
- Fixed screen-band sizing after changing Dock visibility and made restoring minimized windows from the app shelf more reliable.
- Kept overflow windows available in a background stack instead of minimizing them, with recently focused windows promoted into visible slots.

## 1.4.0 - 2026-08-30

- Added a window arrangement control for choosing automatic, one-, two-, or three-window layouts within the available screen area.
- Improved the app shelf with separate open and minimized rows, clearer window states, focused-window promotion, and compact layouts that scale across display sizes.
- Scoped window management to the active space and display so windows elsewhere remain available without being tiled or minimized.
- Added live activity status for plain terminals and responsive layouts for narrow workspace, session history, and activity panels.
- Paused iOS Remote reconnects while backgrounded and improved recovery when returning to the foreground or connecting over slower networks.
- Preserved macOS Accessibility permission across reinstalls and separated macOS framework builds from the universal iOS framework.

## 1.3.6 - 2026-08-30

- Expanded screen bands with top, bottom, left, right, and full half-band placements for more flexible workspace layouts.
- Added adaptive tiling for multiple app windows in the free screen area, including controls to focus, promote, or release managed windows.
- Added an option to auto-hide the macOS Dock while Cairn manages the screen and restore it when management ends.
- Added a Window menu toggle for showing or hiding Cairn window shadows.
- Hardened the shared Apple framework build and signing flow used by Cairn's macOS and iOS targets.

## 1.3.5 - 2026-08-29

- Added screen-band controls to the workspace list and automatically fit focused windows around the selected bands.
- Added a Command-B side-panel toggle, a collapsible live-sessions column, and lower background work while those sections are hidden.
- Refined compact workspace tabs with clearer pills, selectable wire display modes, and completion badges for sessions that finished out of view.
- Improved active, blocked, and completed session detection so workspace status and alerts stay accurate.
- Hardened remote tunnel recovery and main-thread watchdog sampling for more reliable long-running sessions.

## 1.3.4 - 2026-08-29

- Added a WORKSPACE column to Session History so you can scan which workspace each session belongs to and sort by it.
- Bundled a background Chrome bridge with automatic browser selection that is aware of already-running browsers, clearer install guidance, and reload-state detection.
- Introduced compact hierarchy tabs with directory-grouped ⌘⌥ navigation, and wrapped long compact headings so they stay readable.
- Showed all workspace wires faintly on the canvas while emphasizing the selected and hovered connections.
- Streamlined remote host authentication and warm launches, and trimmed redundant canvas layout and reparse work for smoother interaction.

## 1.3.3 - 2026-08-28

- Made new AWS jump hosts ready faster by removing slow package updates from first-boot setup.
- Added immediate failure detection and clearer recovery guidance when jump-host hardening does not complete.
- Reapplied current security settings when reusing an existing jump host and refreshed inventory after setup timeouts.

## 1.3.2 - 2026-08-28

- Isolated AWS jump-host resources per Cairn installation so multiple Macs can safely share one AWS account.
- Added guided AWS CLI setup, credential verification, and clearer sign-in recovery in Jump Host settings.
- Added jump-host inventory controls to adopt, remove, or fully clean up Cairn resources while preserving infrastructure still used by another Mac.

## 1.3.1 - 2026-08-27

- Fixed active sessions showing a stale elapsed time instead of "now."
- Corrected workspace status reconciliation so passive lifecycle states do not surface stale attention alerts.
- Reduced false main-thread hang reports by confirming heartbeat stalls before recording them.
- Kept main-thread hang history compact while preserving recent diagnostic details.

## 1.3.0 - 2026-08-27

- Added 20 named workspace color presets, including automatic theme-aware selection, with 64 distinct identity colors per palette.
- Added a Workspace Colors menu with color swatches and live updates across workspace and activity views.
- Unified agent status names, colors, sorting, tooltips, and accessibility labels across Cairn.
- Simplified the side panel around workspace hierarchy and made compact status pills easier to scan.
- Shortened the terminal-close input guard while preserving protection against repeated Control-C and Control-D presses.

## 1.2.10 - 2026-08-27

- Expanded Screen Band mode with top, bottom, left, and right placement options.
- Refined workspace list interaction with single-click activation, clearer agent status colors, and per-section activity timelines.
- Improved detection and presentation of coding-agent waiting and user-input states.
- Added a short safety guard so repeated Control-C or Control-D presses after closing a terminal do not spill into the terminal that receives focus.

## 1.2.9 - 2026-08-27

- Added Screen Band mode to keep Cairn anchored at the top of the display at a configurable height.
- Added options to resize other apps into the remaining screen space and keep Cairn above their windows.
- Fixed side-panel presentation restoration and tightened Screen Band window observation for more reliable positioning.

## 1.2.8 - 2026-08-26

- Added remote terminal pooling so verified SSH hosts can keep shells and coding agents ready across workspace launches and app restarts.
- Grouped remote workspaces by machine and improved remote provisioning reliability.
- Made the session history pane resizable while Activity is collapsed, with its preferred height preserved across restarts.

## 1.2.7 - 2026-08-26

- Improved workspace activity tracking across split panes so status updates and recency reflect every active agent session.
- Refined workspace list column sizing and alignment, especially when digest details are hidden.
- Fixed the remote task sheet occasionally opening without its selected host.

## 1.2.6 - 2026-08-26

- Security hardening across the app and remote session handling.

## 1.2.5 - 2026-08-25

- Simplified workspace ordering around recent activity and clarified the List and Hierarchy layouts with mode-specific columns.
- Added an option to view live sessions across every workspace, ordered by their latest update.
- Updated macOS copy-on-select behavior so selected text is immediately available to standard paste.

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

