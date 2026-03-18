# RevShell v3

A single-file, browser-based security reference UI for authorized lab work, training environments, and CTF practice.

`revshell-v3.html` bundles a React-powered interface into one standalone HTML file. It provides a tabbed workspace for browsing payload references, organizing common operator workflows, and quickly copying commands with a consistent UI.

## What it includes

- **Reverse Shells tab** with searchable shell entries, category filters, OS filters, stealth scoring, favorites, and copy-ready output.
- **MSFvenom tab** for building payload strings with matching listener guidance.
- **Web Shells tab** for browsing common web payload templates in one place.
- **File Transfer tab** with grouped upload, download, serving, and exfiltration references.
- **Post-Exploitation tab** for follow-up notes and operator checklists.
- **Workflow Builder** that suggests a path based on target OS and available tooling.
- **Copy History panel** for recently copied payloads.
- **Diff Viewer** to compare payload variants side by side.
- **Custom Shell import** so users can save their own templates.
- **Keyboard shortcuts**, onboarding tips, quick port presets, and persistent local settings.

## Tech stack

This project is intentionally lightweight and self-contained:

- **Single HTML file**
- **React 18** and **ReactDOM** loaded from CDN
- **Babel Standalone** for in-browser JSX transpilation
- **JSZip** included for client-side export utilities
- **localStorage** for saved preferences, history, favorites, and custom entries

## Running locally

### Option 1: Open directly

Open `revshell-v3.html` in a browser.

### Option 2: Serve it locally

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/revshell-v3.html`.

## Project structure

```text
revshell-v3.html   # complete application in one file
```

The app is organized into logical UI sections inside the file, including:

- shared utility hooks and UI helpers
- shell registries and reference datasets
- modal tools such as workflow, history, diff, and shortcuts
- tab components for shells, payload generation, file transfer, and post-exploitation
- a root `App()` component that wires navigation and state together

## Highlights

- **Fast to deploy:** no build step required.
- **Portable:** easy to move, demo, or host as a static file.
- **Persistent:** remembers favorites, copied items, custom shells, and connection values.
- **Operator-friendly UI:** compact layout, searchable content, quick actions, and modal tools.

## Safety notice

This repository should only be used in environments where you have explicit authorization, such as labs, internal testing ranges, training environments, and CTFs. Do not use it against systems you do not own or have permission to assess.

## Possible next improvements

- break the single-file app into reusable modules
- add a proper build pipeline
- separate data registries from UI components
- add import/export for saved state
- add tests for payload rendering and filtering logic
- improve responsive behavior for smaller screens

## License

Add your preferred license here.
