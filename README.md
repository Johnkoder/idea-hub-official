# IdeaHub

A local-first Windows desktop workspace for brainstorming, notes, canvases, tasks, and personal organization.

---

## Download

Download the latest Windows installer from the [Releases](https://github.com/Johnkoder/idea-hub-official/releases) page.

- **Current Release**: IdeaHub v1.2.0
- **Platform**: Windows (x64)
- **Installer**: `IdeaHub Setup 1.2.0.exe`
- **Unsigned Release Notice**: Because IdeaHub is currently unsigned, Windows Defender SmartScreen may display an "Unknown Publisher" warning. If you trust the release source, use the Windows "More info" option to continue. See [Installation](#installation) for details.

---

## What's New in v1.2

- **Major desktop UI/UX redesign**: A cleaner, more structured desktop-native visual system with a dedicated navigation rail and refined typography.
- **Redesigned project launcher**: Faster project browsing, quick actions, and accessible recent items.
- **Redesigned workspace & tabs**: Refreshed Explorer, folder tree, and multi-tab interface.
- **Notes editing polish**: Distraction-free editing with refined formatting and slash-menu interactions.
- **Redesigned Canvas toolbar & inspector**: Centralized spatial canvas tools for shapes, sticky notes, connectors, and note references.
- **Refreshed core views**: Inbox, Global Tasks, Calendar, Tags, Search, and Settings now share the modern desktop design language.
- **Contextual guided tour**: First-run coach marks introduce key controls directly in the interface and can be replayed from Settings.
- **Theme improvements**: Refined light, dark, and system appearance.
- **Desktop responsiveness**: Smooth layout scaling including support for compact 960x600 windows.
- **Reliability improvements**: Development and runtime interop fixes with robust local persistence.

---

## Core Features

### Projects
- Project-first organization for ideas, research, and planning.
- Create workspaces with a single click.
- Nested folders and items with a dedicated Workspace Explorer.
- Persistent multi-tab interface preserving your open context across restarts.

### Notes
- Clean, keyboard-friendly block-style note editor.
- Text formatting, headings, code blocks, lists, and checklists.
- Instant local autosave and flush durability.

### Canvas
- Infinite spatial canvas for freeform brainstorming and diagramming.
- Complete visual toolkit: pen, shapes (rectangles, ellipses), connectors/arrows, text labels, and sticky notes.
- Pan, zoom, marquee selection, duplicate, and undo/redo history.
- Local image placement and stable Note References connecting visual nodes to workspace documents.

### Tasks
- **Project Task Lists** for tasks scoped to a specific project.
- **Global Tasks** as a separate personal checklist for tasks not tied to one project.
- Straightforward checklist workflow with progress indicators.

### Calendar
- Centralized global calendar view for dated events.
- Schedule and inspect dated events alongside ongoing work.
- Operates independently from project task checklists.

### Inbox
- Quick capture buffer for rapid thought gathering.
- Draft Notes, Canvases, and Task Lists instantly without choosing a project upfront.
- Seamlessly move captured items into destination projects when ready.

### Tags
- Flexible global tagging system for categorizing workspace items across projects.
- Interactive Tag Browser with item filtering and direct navigation.

### Search
- Fast global search across project and item titles, Note content, and tags.
- Direct keyboard access with `Ctrl+K`.

### Guided Tour
- Contextual first-run guided tour highlighting key controls directly in the interface with coach marks.
- Can be replayed at any time from Settings.

### Local-First Architecture
- 100% offline and fully functional without an internet connection.
- No mandatory accounts, sign-ins, or remote services.
- Structured local SQLite database with managed on-disk assets.
- Complete import and export of structured `.ideahub` project packages.

---

## Updating from v1.0.0

IdeaHub v1.2.0 can be installed over an existing v1.0.0 installation. Existing local IdeaHub data is preserved during the upgrade. As with any local application, keeping a current backup before upgrading is recommended.

---

## Current Scope

IdeaHub v1.2.0 is deliberately focused on delivering a stable local experience:
- **Platform**: Windows x64 only
- **Single-user**: Local desktop application
- **Fully offline**: No cloud synchronization or remote accounts
- **No AI / Cloud APIs**: All text and canvas processing occurs locally on your computer
- **No auto-updater**: Updates are delivered manually via new releases

These boundaries represent intentional architectural choices for privacy, reliability, and speed.

---

## Data Storage & Backups

- **Local Storage**: All workspaces, databases, and configuration settings are stored locally in standard per-user application directories.
- **Local Assets**: Images imported into Canvases and Notes are stored locally in a dedicated app asset repository and streamed via a secure local protocol (`ideahub-asset://`).
- **Project Backups**: Export individual projects anytime to portable `.ideahub` archives containing all documents, metadata, and embedded media.
- **Backup Restore**: Import `.ideahub` archives into any clean or existing installation with transactional safety and rollback guarantees.

---

## Installation

1. Navigate to the latest release on the [Releases](https://github.com/Johnkoder/idea-hub-official/releases) page.
2. Download `IdeaHub Setup 1.2.0.exe`.
3. Run the installer.
4. If Windows Defender SmartScreen displays an "Unknown Publisher" warning:
   - Click **More info**.
   - Click **Run anyway** if you trust the release source.
5. Follow the setup wizard prompts to select an installation location and finish setup.
6. Launch IdeaHub.

---

## Checksum Verification

We recommend verifying the integrity of your download prior to running the setup executable.

- **Installer Filename**: `IdeaHub Setup 1.2.0.exe`
- **Expected SHA-256**:
  ```text
  700d8b1afe56ff29200202ca6cf2a19abc232781b5899ca14a9f1445de07209e
  ```

### Verify with PowerShell
```powershell
Get-FileHash ".\IdeaHub Setup 1.2.0.exe" -Algorithm SHA256
```

Compare the computed hash with `SHA256SUMS.txt` attached to the release or view [docs/checksums.md](docs/checksums.md).

---

## Privacy

IdeaHub is designed around user privacy:
- Workspace data never leaves your device.
- No telemetry, analytics, or background reporting services are included.
- No network connections are initiated during normal operation.

Read our full statement in [docs/privacy.md](docs/privacy.md).

---

## Source Code

This repository is currently used for public IdeaHub releases and product documentation. The application source code is not currently published here.
