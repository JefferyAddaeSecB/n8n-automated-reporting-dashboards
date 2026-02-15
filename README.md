# n8n Automated Reporting Dashboards

Scheduled KPI pipeline with multi-source merge, anomaly scoring, AI narrative generation, and executive distribution.

## Files
- `n8n/workflow.json` importable n8n workflow (AI Agent + deterministic fallback + native app nodes)

## Architecture
- Daily trigger -> deterministic KPI snapshot + anomaly scoring
- AI Agent + OpenAI Chat Model executive narrative generation
- Signal merge -> final reporting packet
- Notion brief + Gmail exec summary + Slack anomaly branch

## Runtime Requirements
- n8n (validated with containerized import on n8n latest)
- Configure credentials for:
  - `OpenAI` (for `AI Agent` model connection)
  - `Slack`
  - `Notion`
  - `Gmail`
  - `HubSpot` (where used)
- Replace placeholder channel/database IDs and recipient addresses before activation

## Import
1. Open n8n UI.
2. Go to `Workflows -> Import from File`.
3. Select `n8n/workflow.json`.
4. Configure credentials and placeholder IDs.
5. Run a manual execution test before enabling schedule/webhook traffic.

## Live Demo
- https://jeffery-addae-portfolio-web.vercel.app/projects/automated-reporting-executive-dashboards
