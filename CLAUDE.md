# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a **STRIDE threat model** for the Lobster personal AI agent system built on the OpenClaw framework. It is a static content repository with no build system, package manager, or tests.

## Key Files

- **`lobster-threat-model.json`** — Threat model data in OWASP Threat Dragon format (v2.3.0). Contains the full data flow diagram definition (trust boundaries, processes, data stores, external entities, data flows) and all threat entries with STRIDE categories, severity, mitigations, and status.
- **`index.html`** — Self-contained single-page HTML/CSS/JS visualization of the threat model. Renders an interactive SVG data flow diagram and a filterable threat table with STRIDE category, severity, and component filters. All threat data is embedded inline in a `threats` array.
- **`lobster-threat-assessment.docx`** — Written threat assessment document.

## Architecture Notes

- The JSON file and HTML file maintain **parallel threat data** — the JSON uses Threat Dragon's schema while the HTML has its own inline `threats` array. Changes to threats must be reflected in both files to stay in sync.
- The HTML is entirely self-contained (no external dependencies, no bundler). CSS uses custom properties for light/dark theme support via `prefers-color-scheme`.
- The SVG data flow diagram in `index.html` is hand-authored inline SVG, not generated. It depicts five trust boundaries (Internet, Tailscale Mesh, Gateway, Restricted, Exec/Host OS) with interactive click-to-filter behavior.
- The threat model covers six OpenClaw agents: iMessage, WhatsApp, Email, Calendar, HomeKit, and Travel.

## Working with This Repo

To view the threat model visualization, open `index.html` in a browser. No server required.

When editing the JSON file, maintain compatibility with [OWASP Threat Dragon](https://threatdragon.github.io/) schema so the file can be round-tripped through that tool.
