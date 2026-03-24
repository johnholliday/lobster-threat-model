# Lobster / OpenClaw STRIDE Threat Model

A STRIDE threat model of the **Lobster** personal AI agent system built on the [OpenClaw](https://lobster.shahine.com) framework. Six agents running on a dedicated Mac handle iMessage, WhatsApp, email, calendar, HomeKit, and travel.

## Live View

**[johnholliday.github.io/lobster-threat-model](https://johnholliday.github.io/lobster-threat-model/)**

The interactive visualization includes:
- SVG data flow diagram with five trust boundaries (Internet, Tailscale Mesh, Gateway, Restricted, Exec/Host OS)
- 46 catalogued threats across all six STRIDE categories
- Filtering by STRIDE category, severity, and component
- Click any DFD element to filter threats to that component
- Boundary-crossing summary table
- Light and dark theme support

## Repository Contents

| File | Description |
|------|-------------|
| `index.html` | Self-contained interactive threat model viewer (no external dependencies) |
| `lobster-threat-model.json` | Threat model data in [OWASP Threat Dragon](https://threatdragon.github.io/) v2.3 format |
| `lobster-threat-assessment.docx` | Written threat assessment document |

## Contributors

- **John F. Holliday** — Holliday & Associates
- **Omar Shahine** — Architecture
- **Claude (Anthropic)** — Analysis assistance
