# Cairn changelog

## 2.6.0 - 2026-09-16

- Add native agent rooms for durable multi-agent work, with guided setup, workspace placement, cross-host routing, replies, reattachment, milestones, artifacts, approvals, and recovery when a run is interrupted.
- Add native agent and plugin libraries, including safe package import, guided local agent creation, richer plugin panes, and automatic updates for bundled plugins.
- Expand governed orchestration with durable event streams, credential binding, usage accounting, bounded subscriptions, supervised ACP runtimes, and reliable cleanup when participant runs finish.
- Add the bundled Unlazy Progress experience with workspace-aware pipeline views, plan and gate inspection, filtering, sorting, calendar context, and worktree actions.
- Improve Fleet with first-run onboarding, clearer crew and workflow creation, durable workspace identity, tracked task dispatch across hosts, and a dedicated Tasks panel.
- Add local shell splits alongside remote workspaces, restore the last focused workspace on relaunch, and harden the app against monitor-disconnect freezes, stale plugin connections, and orchestration failures.

## 2.5.0 - 2026-09-13

- A license key is required when Cairn first opens; there is no trial in this release.
- Keep valid legacy Cairn license keys working alongside active monthly Gumroad memberships.
- Add the durable orchestration runtime for standing-agent workflows, approvals, scheduling, recovery, and remote execution.
- Replace session-history polling with native events and improve workspace opening, selection, and session-fork reliability.
- Keep inactive render targets parked without blocking the renderer.

## 2.4.1 - 2026-09-13

- Make New Workspace actions on iPhone and iPad route reliably from global, folder, and workspace entry points, with stronger fallback behavior and expanded regression coverage.

## 2.4.0 - 2026-09-13

- Add rich native plugin panes with responsive metrics, charts, tables, controls, and a new activity API, plus installable developer examples.
- Keep Needs You events across acknowledgements and app relaunches, show earlier events as muted history, and let historical rows recover their workspaces on Mac and iPhone.
- Add session-fork actions to live-session panes and terminal context menus, targeting the exact selected terminal when creating a new workspace or split.
- Move agent transcript discovery off the main thread to prevent workspace updates from freezing the interface.
- Keep reserved alert colors distinct from quiet workspace colors so attention states remain immediately recognizable.

## 2.3.4 - 2026-09-12

- Simplify dock layouts by retiring the Usage and Layout Controls panes and replacing the split menu with direct Split Right and Split Below actions.
- Make Needs You rows respond reliably when clicking their labels, status, or detail text.

## 2.3.3 - 2026-09-12

- Pin important workspace panes so they stay in place and appear first in the Navigator.
- Jump directly to the exact terminal session from Needs You alerts and notifications.
- Make completed-agent notifications clearer, keep the Dock badge aligned with Needs You, and remove resolved notifications.
- Show concurrent coding-agent sessions together in Navigator workspace summaries, making parallel work and the session that needs attention easier to distinguish.
- Make multi-directory workspace rows easier to scan with adaptive heights and concise directory names.
- Ask whether a new terminal should open locally or on the connected host when it is created from a remote workspace.
- Show the active macOS sleep policy inside Remote > Stay Awake, with shortcuts to the relevant system settings.
- Refine the Cairn icon with a warmer, clearer background and a more balanced touching-stone composition across macOS, iOS, the website, and storefront artwork.

## 2.3.2 - 2026-09-11

- Keep local pane working directories current after shell directory changes, including shells that do not report OSC 7.

## 2.3.1 - 2026-09-11

- Keep directory colors stable as workspaces and folders are added, so established visual identities no longer shift unexpectedly.
- Refresh live agent activity directly from terminal changes for faster, more accurate navigator and canvas status.
- Update elapsed-time labels continuously and use clearer “running” status wording throughout the workspace interface.

## 2.3.0 - 2026-09-11

- Reworked the workspace navigator with clearer live-session summaries, wider cards, workspace-aware naming, goal-age status, and coordinated directory colors across sessions and splits.
- Refined dock and window management with a more compact layout, stable companion windows, explicit free-space drop zones, and smoother motion that keeps workspace panels visually anchored.
- Added guided host recovery to Resource Monitor, clearer remote-startup failures, and automatic health monitoring for SSH port forwards.
- Improved the remote file browser with Cairn-aware theming, safer tunnel handling, bounded search, and support for forwarded folders reached through top-level symlinks.
- Refreshed the Cairn app icon and removed retired canvas and history paths to simplify the app and improve reliability.

## 2.2.4 - 2026-09-09

- Improved workspace navigator status accuracy when visible terminal panes are active before their live session bindings are available.
- Fixed empty terminal selections incorrectly clearing the existing clipboard contents.
- Fixed recent main-thread hangs during window activation, canvas refreshes, and workspace status updates.

## 2.2.3 - 2026-09-09

- Added a secure remote file browser for forwarded folders, with stable browser URLs, clearer connection progress, bounded filename and content search, and safer handling of paths and rendered output.
- Fixed a renderer deadlock that could freeze Cairn while macOS display topology changed.

## 2.2.2 - 2026-09-08

- Added unified window-management controls for arranging Cairn and browser windows, with adaptive layouts and more stable reflow as screens and panels change.
- Added stay-awake controls to Cairn Remote so an iPhone or iPad can keep the connected Mac awake during a remote session.
- Made workspace arrow navigation follow the active navigator's current filtering and sorting.
- Improved remote port-forward diagnostics with captured errors, bounded retries, cancellation controls, and a watchdog for connections stuck at “Connecting…”.
- Fixed compact window-management panels so overflowing content scrolls instead of overlapping other controls.

## 2.2.1 - 2026-09-08

- Expanded the workspace navigator with keyboard navigation, route-synchronized selection, configurable detail levels, and more predictable workspace cycling.
- Added composable pane layouts and remote pane launching, with more reliable working-directory handling for remote workspaces and splits.
- Added automatic local port forwarding for remote folders and development servers, including remote HTML preview serving through Cairn's secure host connection.
- Added a local developer control API and MCP interface for inspecting and controlling Cairn workspaces, panels, and actions.
- Improved live workspace status timing, panel redraws after dock moves, and remote-split probing behavior.
- Improved Cairn Remote connection reliability with staged EICE/SSH deadlines and clearer split diagrams for deeply nested layouts.

## 2.2.0 - 2026-09-08

- Improved remote host launching by detecting coding agents through interactive login shells and clearly separating host repair state from ready warm-pool sessions.
- Made remote workspace directories host-aware: new launchers default to the remote home directory, remember successful directories per host, and no longer carry a local Mac home path onto Linux hosts.
- Made clean remote process exits close their split and the final workspace while preserving reconnect behavior for unexpected SSH or transport failures.
- Simplified Remote Hosts management and made helper shutdown more reliable during login-shell startup.
- Added a Needs You attention queue to the iOS Remote app, improved split visibility, and accelerated stale-session reconnection.

## 2.1.1 - 2026-09-07

- Improved Quick Agent launcher legibility by automatically choosing dark or light selected-row text and icons for the current accent color and appearance.

## 2.1.0 - 2026-09-07

- Added always-on host load monitoring that pauses speculative terminal warm-up during sustained CPU contention while keeping user-initiated launches responsive.
- Expanded Resource Monitor with host-load, runnable-process, and zombie-process detail, plus optional notifications and cleanup of obsolete Cairn helper processes during severe overload.
- Made the repeated Control-C/D close guard configurable from the Window menu with 1, 2, 3, and 5 second durations, and fixed bare Control-C/D events so they reliably reach the terminal.
- Improved dock responsiveness with targeted panel refreshes, fewer unnecessary layout commits, and cheaper workspace-pill sizing.
- Improved large session-history updates and live activity timestamps while reducing blocking Keychain writes and repeated text-processing work.

## 2.0.2 - 2026-09-06

- Added multi-selection to the workspace navigator for opening, forking, and closing several workspaces together.
- Added in-app web viewing on iPhone and iPad for links opened from remote terminal sessions, carried through the existing secure host connection.
- Improved Cairn Remote with workspace split diagrams, unread activity indicators, more reliable scroll-tail behavior, and safer agent integration isolation.
- Improved compact dock layouts for remote hosts, jump hosts, resource monitoring, and activity views, and updated the remote PTY service to v0.2.0.

## 2.0.1 - 2026-09-06

- Added a native Plugins panel for installing, reloading, inspecting, and removing extensions without leaving Cairn.
- Added per-plugin capability controls, runtime status, contribution summaries, and actionable discovery errors for invalid plugins.
- Added workflow-focused canvas presets for all panels, window management, fleet launch, and fleet monitoring alongside the existing basic layouts.
- Improved narrow dock panes by collapsing the panel type chooser to an icon with an accessible tooltip when space is tight.

## 2.0.0 - 2026-09-06

- Redesigned Cairn around a persistent dockable workspace with split and stacked layouts, configurable presets, drag-and-drop panels, keyboard navigation, and dedicated panels for workspaces, live sessions, activity, history, usage, and remote hosts.
- Added a scalable remote-fleet control plane with bounded discovery, session catalogs, repair plans, reconnect policies, richer host health summaries, and faster context-aware workspace launches.
- Added a process-isolated plugin platform and local developer API with explicit permissions, custom panels, event subscriptions, build monitoring, a Swift command-line client, and a generated developer portal.
- Rebuilt session history on SQLite with indexed search, structured activity records, cleaner titles, attachment and machine-payload filtering, and bounded background indexing.
- Improved live-session navigation with receiver routing, preserved execution state, process-backed liveness, workspace context menus, configurable navigator sorting, and open-or-fork actions that carry terminal selection context.
- Reduced idle and refresh CPU use by eliminating leaked cursor timers, caching process-session scans, bounding transcript work, and avoiding unnecessary full-text-search backfills.
- Removed the legacy Project menu and consolidated workspace, browser, and layout controls around the new dock-based workflow.

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

