# DIVERSEVISUALARTSSTUDIO UX/UI MOBILE APP

A responsive, mobile-first business command center for DiverseVisualArtsStudioLLC.

## Modules
- Overview and illustrative pipeline chart
- Revenue leads with add, delete, search and stage updates
- Project tracker with create workflow
- IT operations and integration readiness
- Cybersecurity sample alerts and demo role controls
- Local AI-agent simulations
- Integration guidance for IBM Bob, IBM watsonx Orchestrate and GitHub
- JSON export and browser-local demo persistence

## GitHub Pages deployment
This static HTML/CSS/JavaScript app is deployed from the repository root by GitHub Actions.

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, select **GitHub Actions** as the source.
3. Push to `main` or run **Deploy DVAS Mobile App** manually from Actions.
4. After the workflow succeeds, visit:
   https://diversevisualartsstudio-ai.github.io/DIVERSEVISUALARTSSTUDIO-UX-UI-MOBILE-APP/

## Local preview
Open `index.html` in a browser, or run `python -m http.server 8000` from the repository root.

## Demo data and limitations
Lead, project and alert records are sample data stored in the current browser's localStorage. This is a front-end prototype, not a production CRM, accounting system, SIEM, identity provider or financial application. Browser storage is not shared across devices and must not contain sensitive customer information.

The IBM integration cards are setup guidance only. IBM Bob is a developer coding assistant; watsonx Orchestrate runs configured agents and workflows. Neither service is authenticated or called by this static app.

## Production integration architecture
Use an authenticated backend as the only component allowed to call IBM APIs. Store secrets in backend environment variables or a managed secret vault. Enforce least privilege, server-side authorization, audit logs, rate limits, input validation, TLS and human approval for sensitive actions. Never place API keys or privileged GitHub tokens in client-side JavaScript.

## Production security checklist
- Replace demo authentication with an established identity provider and MFA.
- Add server-side RBAC; current role toggles are visual-only.
- Connect a real database with backups and retention controls.
- Add server-side audit logging and alert ingestion.
- Add authorization, validation and error-handling tests.
- Configure IBM Orchestrate environment, tools, agent permissions and human approvals.
- Run dependency, accessibility and security scans.

© DiverseVisualArtsStudioLLC · Design, Inspire, Create, Elevate.
