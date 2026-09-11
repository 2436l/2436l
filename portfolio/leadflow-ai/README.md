# LeadFlow AI MVP

A reusable inbound-lead qualification and follow-up automation demo for small agencies, consultancies, and SaaS teams.

## What it does

1. Accepts an inbound lead from a form/webhook.
2. Normalizes and validates contact/company fields.
3. Deduplicates using a deterministic fingerprint.
4. Scores the lead on fit + intent + urgency.
5. Routes hot leads to sales immediately.
6. Creates a personalized follow-up draft.
7. Can write the lead to a CRM/Google Sheet and trigger Slack/Telegram alerts.
8. Includes production-hardening guidance for retries, logging, and human review.

## Demo

Open `demo/index.html` in a browser. It runs locally and demonstrates qualification, routing, duplicate fingerprinting, and follow-up generation.

## n8n template

Import `n8n/leadflow_ai_template.json` into n8n, then attach your own credentials for Google Sheets, Gmail, Slack, CRM, and optional LLM enrichment.

## Intended use

Portfolio/demo and reusable implementation base. Replace sample IDs, credentials, and business-specific scoring rules before production use.
