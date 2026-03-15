#  Post-Call Reporting Variables — SOMOS Internet Retention Agent

All variables are automatically populated by the agent after each call.

---

##  Call Overview

| Type | Variable | Description |
|---|---|---|
| Boolean | `call_goal_achieved` | Was the call objective achieved (customer experience improved and cancellation intent reduced)? True if the customer feels reassured, accepts the proposed resolution, or does not want to cancel. |
| Number | `phase_reached` | Last phase reached in the required flow (1=experience, 2=satisfaction, 3=resolution, 4=upsell). Answer only: 1, 2, 3, or 4 |
| Boolean | `call_completed` | Did the call end normally (the customer did not hang up early)? |

---

##  Sentiment & Churn

| Type | Variable | Description |
|---|---|---|
| String | `detected_sentiment` | Customer sentiment at the end of the call: positive / neutral / negative / ambiguous (choose one) |
| Number | `satisfaction_score` | Customer satisfaction score (1–10) if provided; otherwise null |
| String | `churn_risk` | Churn risk level: low / medium / high (choose one) |
| Boolean | `churn_intent_explicit` | Did the customer explicitly state intent to cancel or switch providers? (yes/no) |
| String | `sentiment_evidence` | Exact customer words/phrases that justify the sentiment classification (e.g., 'terrible', 'super stable', 'more or less') |

---

##  Issue Details

| Type | Variable | Description |
|---|---|---|
| String | `primary_issue_category` | Primary issue category: speed / instability / wifi_coverage / billing_price / support_service / moving / other / none |
| String | `issue_details` | Short summary of the issue and how it impacts the customer |
| String | `connection_type` | Affected connection type: wifi / cable / both / unknown |
| String | `issue_frequency` | How often it happens: always / sometimes / peak_hours / unknown |
| String | `issue_location` | Where it happens: whole_home / specific_room / unknown |

---

##  Resolution

| Type | Variable | Description |
|---|---|---|
| String | `resolution_offered` | Resolution offered: wifi_diagnosis / tech_escalation / plan_adjustment / temp_discount / temp_upgrade / none |
| String | `resolution_accepted` | Was the resolution accepted by the customer? yes / no / partial |
| String | `action_plan_summary` | 1–2 sentence summary of the agreed action plan (what will be done next) |
| Boolean | `escalation_required` | Was an escalation required to a technician or human agent? (yes/no) |
| String | `escalation_type` | Escalation type: technical / human / none |
| Boolean | `effective_date_explained` | Did the agent explain that discounts/plan changes take effect on the next billing cycle / next invoice? (yes/no) |
| String | `effective_date_phrasing` | Exact phrasing used about effective timing (e.g., 'next invoice', 'next billing cycle', '24–72 hours') |

---

##  Upsell / Cross-sell

| Type | Variable | Description |
|---|---|---|
| Boolean | `upsell_offered` | Did the agent offer an upsell or cross-sell? (yes/no) |
| String | `upsell_type` | Upsell type: speed_upgrade / mesh_wifi / tv_box / none |
| Boolean | `upsell_accepted` | Did the customer accept the upsell? (yes/no) |
| String | `upsell_reason` | Reason the customer accepted or rejected the upsell (if stated) |
| Number | `objection_count` | Number of customer objections raised during the call (0, 1, 2, ...) |
| String | `main_objection` | Main objection category: price / trust / service_quality / no_time / already_tried / other / none |
