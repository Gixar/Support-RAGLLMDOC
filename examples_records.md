---
type: "Incident"
id: "INC-1001"
client_name: "Acme Corp"
tool: "PagerDuty"
environment: "prod"
severity: "P1"
status: "Resolved"
tags: ["auth", "database", "api"]
language: "en"
created_at: "2025-11-06T15:47:19.076148Z"
updated_at: "2025-11-06T15:47:19.076170Z"
source_url: null
---

## Summary
    Auth service returns 500 for login attempts

    ## Steps to Reproduce
    1. POST /login with valid credentials
2. Observe 500 response with error code EAUTH-17
3. Logs show DB connection timeouts

    ## Solution
    Increased DB pool size from 20→60 and redeployed auth-service v1.4.2. Added circuit breaker with 2s timeout.


---

---
type: "Case"
id: "CASE-778"
client_name: "Globex"
tool: "Zendesk"
environment: "staging"
severity: null
status: "Investigating"
tags: ["webhooks", "retries"]
language: "en"
created_at: "2025-11-06T15:47:19.076175Z"
updated_at: "2025-11-06T15:47:19.076177Z"
source_url: null
---

## Summary
    Webhook retries not respecting backoff setting

    ## Steps to Reproduce
    1. Configure retry policy
2. Fire webhook
3. Intervals are ~5s instead of exponential backoff

    ## Solution
    Pending verification in staging with feature flag off.


---

---
type: "Task"
id: "TASK-42"
client_name: "Initech"
tool: "Internal"
environment: "dev"
severity: null
status: "Open"
tags: ["observability", "metrics"]
language: "es"
created_at: "2025-11-06T15:47:19.076181Z"
updated_at: "2025-11-06T15:47:19.076183Z"
source_url: "https://example.com/spec"
---

## Summary
Agregar métricas de latencia a /healthz

## Steps to Reproduce
—

## Solution
—
