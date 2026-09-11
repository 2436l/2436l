# Architecture

## Pipeline

Inbound form/webhook  
→ normalize fields  
→ validation  
→ duplicate fingerprint  
→ rule-based fit score  
→ optional AI enrichment/classification  
→ hot/warm/cold route  
→ CRM/Sheet write  
→ personalized email draft  
→ Slack/Telegram notification  
→ follow-up timer  
→ response tracking  
→ logs / retry / dead-letter handling

## Scoring model

Base score: 0–100.

- Business email present: +10
- Company name present: +10
- Company size 2–100: +15
- Explicit budget >= $500: +20
- Urgency <= 14 days: +15
- Mentions automation/API/CRM/manual repetitive work: +20
- Detailed pain description: +10

Routing:
- 75–100 = HOT
- 50–74 = WARM
- below 50 = COLD

## Production hardening checklist

- Idempotency key / duplicate protection
- API timeouts and retries
- Credential isolation
- PII minimization
- Dead-letter path
- Execution logging
- Human review before outbound email when needed
- Rate limits
- Alerting for failed runs
