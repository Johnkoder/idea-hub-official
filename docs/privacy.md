# IdeaHub Privacy

## Local-First Data Architecture

IdeaHub stores all workspace content locally on your computer in an SQLite database and managed local asset storage. Your projects, notes, canvas boards, tasks, tags, and settings never leave your device.

## Accounts and Authentication

IdeaHub does not require or support user accounts, sign-ins, or cloud profiles.

## Cloud Synchronization

IdeaHub does not include cloud synchronization, background syncing services, or remote database connections.

## Telemetry and Analytics

IdeaHub does not include intentional telemetry, usage analytics, error-reporting beacons, or background tracking services.

## Offline Operation

IdeaHub is designed to be offline by default. All core workspace capabilities — creating projects, editing notes, drawing and pasting on canvases, managing tasks, viewing the calendar, searching, and exporting backups — function completely without an internet connection.

## Manual Update Checks

Starting in v1.4.0, IdeaHub includes an optional manual update checker accessible via **Settings → Check for updates**.

- **Explicit User Action Only**: IdeaHub connects to the network only when you explicitly click **Check for updates**. No update check runs automatically at application startup, and there is no background polling or recurring timer.
- **Request Endpoint**: The update check sends an HTTPS `GET` request directly to GitHub's public API at:
  `https://api.github.com/repos/Johnkoder/idea-hub-official/releases/latest`
- **Data Transmitted**: The request transmits only standard HTTP request metadata (such as IP address and an IdeaHub User-Agent header specifying the client version). **No project names, notes, task lists, tags, canvas elements, imported assets, or database contents are ever transmitted.**
- **Version Evaluation**: The response is parsed locally in the application main process to compare the current installed semantic version with the latest official stable release.
- **Manual Download & Installation**: If an update is available, clicking **Download update** simply opens the official GitHub release tag page (`https://github.com/Johnkoder/idea-hub-official/releases/tag/vX.Y.Z`) in your default system web browser. IdeaHub never downloads or installs software updates automatically in the background.

## Project Backups

Users can export `.ideahub` project packages to store or transfer their data. Users are solely responsible for how and where exported archive files are stored or shared.
