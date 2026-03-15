# Yarvis Voice Agent — Retention Agent for SOMOS Internet

> AI-powered voice retention agent built on Yarvis AI for SOMOS Internet 
> (fiber home internet service) — designed, configured, and end-to-end 
> tested in 90 minutes.

---

## Objective

Simulate a production-ready retention call flow that:
- Detects **customer sentiment** in real time (positive / neutral / negative)
- Identifies **churn risk** level (low / medium / high)
- Resolves service issues with empathy before offering anything
- Triggers a **contextual upsell** only when appropriate

---

## Demo Video
👉 [Watch the full agent demo on Loom](https://www.loom.com/share/eb6bf93dabf5469293286fc97b89d115)

---

## Agent Architecture

| Component | Details |
|---|---|
| Platform | Yarvis AI |
| Company | SOMOS Internet (fiber ISP) |
| Flow | 4 mandatory phases, executed in order |
| CRM Variables | current plan, tenure, days until renewal, last complaint |
| Post-call Analysis | 20+ structured reporting variables |

---

## 4-Phase Flow
```
Phase 1 → Experience Review
Phase 2 → Satisfaction Sounding + Sentiment Detection
Phase 3 → Resolution (only if issue or medium/high risk detected)
Phase 4 → Upsell / Cross-sell (only if customer is satisfied)
```

---

## Test Scenarios (3 runs)

| Scenario | Goal |
|---|---|
| Happy customer | Validate upsell without unnecessary troubleshooting |
| Neutral / ambiguous customer | Validate clarifying questions before any offer |
| Upset customer (churn risk) | Validate empathy + resolution first, then retention offer |

---

## Reporting Variables
See [`config/variables_reporte.md`](config/variables_reporte.md)

Key variables tracked per call:
`detected_sentiment` · `churn_risk` · `churn_intent_explicit` · 
`phase_reached` · `resolution_offered` · `resolution_accepted` · 
`upsell_offered` · `upsell_accepted` · `escalation_required` · 
`effective_date_explained` · `call_goal_achieved`

---

## Prompt / Script
See [`prompt/script_natalia.md`](prompt/script_natalia.md)

---

## Simulated CRM Variables (test mode)
```json
{
  "current_plan": "600 Mbps",
  "tenure_months": 14,
  "days_since_last_complaint": 20,
  "days_until_renewal": 15
}
```

---

## Repository Structure
```
├── README.md
├── prompt/
│   └── script_natalia.md       ← full agent prompt and script
├── config/
│   └── variables_reporte.md    ← all post-call reporting variables
├── docs/
│   └── resumen_entrega.pdf     ← full delivery summary
└── assets/
    └── demo_preview.png        ← agent screenshot
```

---

##Author
**Maria Ortiz** · mariaortizseg@gmail.com
