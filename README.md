# LogosForge Whiteboard

A free, local-first desktop writing environment for drafting, developing, and revising complete manuscripts.

> [!WARNING]
> **LogosForge Whiteboard is alpha software.**
>
> Keep independent backups of important work. Export your project regularly and back up Whiteboard’s local data directory before upgrading.

## Download

Download Whiteboard from the repository’s [Releases page](../../releases).

| Platform | Package | Requirements |
|---|---|---|
| Windows x64 | Installer `.exe` | 64-bit Windows |
| Windows x64 | Portable `.exe` | 64-bit Windows; no installation required |
| macOS Intel x64 | `.dmg` | macOS 12 Monterey or newer |
| Linux x86_64 | `.AppImage` | 64-bit Linux |

The packages are self-contained. You do not need to install Python, Node.js, or developer tools.

Apple Silicon and universal macOS packages are not currently provided.

## About this repository

This repository is dedicated exclusively to distributing LogosForge Whiteboard desktop releases and release notes.

It is not the development source tree and does not contain build instructions or development dependencies.

Cloning the repository does not automatically download the application packages. Download the appropriate installer or executable from [Releases](../../releases).

## What Whiteboard includes

- A distraction-light, full-manuscript writing environment.
- Isolated, autosaving projects with conflict-safe persistence and recovery.
- Writing modes for:
  - Novels
  - Screenplays, with Fountain editing and paginated preview
  - Graphic novels
  - Stage plays
- **Drafter** tabs for writing individual scenes, alternatives, and experimental passages outside the canonical manuscript.
- A manual **Outline**, document-derived navigation, and Story Map.
- **PSYKE**, the project story bible for characters, places, objects, lore, themes, and related knowledge.
- **Progressions** for tracking story, character, relationship, theme, world, and custom arcs as ordered beats.
- Page-scoped comments for both the main Manuscript and individual Drafter pages.
- Advanced Find & Replace with case-sensitive and whole-word matching.
- Preset and installed system fonts, manuscript colors, themes, zoom, focus mode, folding, and syntax aids.
- Optional **Billy** chat and **Logos** inline writing assistance.
- An authenticated local MCP companion for compatible AI clients, with guarded review and apply operations.
- Import from Text, Markdown, Fountain, Final Draft, and `.logosforge`.
- Export to Text, Markdown, Fountain, HTML, JSON, PDF, `.logosforge`, comment reports, and `.lfbundle`.

## Installation

### Windows

Choose one of the following packages:

- **Installer:** run the standard `x64.exe` installer.
- **Portable:** download the `x64-portable.exe` file and launch it directly.

The portable version does not require installation, but projects are still stored in your normal Whiteboard data directory rather than beside the executable.

Windows SmartScreen may warn because current packages are unsigned. If the file came from this repository’s official Releases page, select **More info → Run anyway**.

### macOS

1. Download the Intel x64 `.dmg`.
2. Open the disk image.
3. Drag **LogosForge Whiteboard** into **Applications**.
4. On first launch, right-click the application and choose **Open**.

The current package requires an Intel Mac running macOS 12 Monterey or newer.

The application is not yet notarized. If macOS continues to block an official download, clear its quarantine attribute:

```bash
xattr -cr "/Applications/LogosForge Whiteboard.app"
```

Only use this command for a package downloaded from this repository’s official Releases page.

### Linux

Download the x86_64 AppImage, make it executable, and run it:

```bash
chmod +x LogosForge.Whiteboard-*-x86_64.AppImage
./LogosForge.Whiteboard-*-x86_64.AppImage
```

Desktop integration and sandbox requirements can vary between Linux distributions.

## Local data and backups

Whiteboard is local-first. Project data defaults to:

- **Windows:** `%USERPROFILE%\.logosforge`
- **macOS and Linux:** `~/.logosforge`

Before upgrading:

1. Close Whiteboard completely.
2. Copy the local data directory to a safe location.
3. Export important projects from Whiteboard.
4. Install or replace the application.
5. Reopen Whiteboard and confirm that the projects load correctly.

Do not delete the `.logosforge` directory during an ordinary upgrade.

### About `.lfbundle`

A `.lfbundle` is a complete project export containing the manuscript, Drafter pages, settings, Outline, comments, PSYKE entries, and Progressions.

Whiteboard currently exports `.lfbundle` files but does not import them. For a directly restorable Whiteboard backup, also keep a copy of the local data directory.

## Optional AI features

Whiteboard’s ordinary writing, organization, commenting, and export features work without an AI provider.

Billy and Logos can use a provider configured in **Settings**, including:

- LM Studio
- Ollama
- OpenAI
- Anthropic
- OpenRouter

No provider is contacted until one is configured and an AI feature is used.

Local providers such as LM Studio and Ollama can run on the same computer. When a hosted provider is selected, relevant prompt and project context is sent to that provider according to its own privacy policy and terms.

Local model files and hosted-provider API access are not included with Whiteboard.

## Updating Whiteboard

For every update:

1. Read the release notes.
2. Back up the local data directory.
3. Export important projects.
4. Close Whiteboard.
5. Download the new package only from [Releases](../../releases).
6. Install or replace the previous application.
7. Confirm that projects, Drafter pages, PSYKE entries, comments, and Progressions are present.

## Known limitations

- Whiteboard remains alpha software.
- Packages are currently unsigned and unnotarized.
- macOS releases are Intel x64 only.
- There is no built-in cloud synchronization or real-time collaboration.
- AI features require a separately configured local or hosted provider.
- `.lfbundle` files are export-only in Whiteboard.

## Reporting a problem

Use the repository’s [Issues page](../../issues) and include:

- Whiteboard version
- Operating system and version
- CPU architecture
- Steps needed to reproduce the issue
- What you expected to happen
- What actually happened
- Whether restarting Whiteboard changes the behavior
- A screenshot, when it does not expose private writing

Remove manuscript text, API keys, personal file paths, project names, and other private information before posting a report.

## Release status

Whiteboard releases are distributed as alpha prereleases while installation, recovery, compatibility, and packaged-app behavior continue to be validated across supported systems.


One publishing note: the current project has no `LICENSE` or binary-distribution terms file. Add one to the release repository before presenting it publicly as open source or granting redistribution rights.
