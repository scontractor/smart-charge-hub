# Smart Charge Hub
### E.ON Next - Connected Devices & EV Experience
**PM Case Study · Senior Product Manager Interview · March 2026**

---

## Overview

Smart Charge Hub is an interactive product concept and analytics prototype built as part of a Senior PM interview case study for E.ON Next. The brief asked: *"Imagine you are the PM responsible for improving the experience of a connected device ecosystem."*

This project focuses on closing the **EV activation gap** — the gap between customers who have a home charger installed and those who are actually saving money on their electricity bill through E.ON Next's **Next Drive Smart** tariff.

The prototype demonstrates what a guided activation flow and savings dashboard would look like inside the E.ON Next Home app, alongside a GA4-style analytics dashboard tracking the metrics and OKRs that would determine whether the product is working.

---

## The Problem

Next Drive Smart offers EV drivers a **72% cheaper off-peak rate** (8.5p/kWh vs 30.9p/kWh), with confirmed average savings of **£117/year**. But a significant proportion of customers who install a home charger never activate the tariff.

Three structural root causes:

| Root Cause | Description |
|---|---|
| **Awareness Gap** | Customers don't know Next Drive Smart exists as a separate tariff |
| **Setup Friction** | No single guided flow - steps split across website, app and a 2-week wait |
| **No Visible Value** | No real-time savings feedback post-connection |

---

## The Solution

A **Smart Onboarding Wizard** and **Savings Dashboard** built into the E.ON Next Home app, collapsing 4 fragmented steps into one guided flow.

**Three features:**
- **Connect Wizard** - 3 steps: connect car > verify smart meter > activate Next Drive Smart. MPAN pre-populated from account, smart meter consent explained in plain English, under 4 minutes from first tap.
- **Savings Dashboard** - Real-time £ saved vs peak rate, weekly charge history, personalised schedule, annual progress toward £117 target, Boost mode override.
- **Smart Alerts** - Install day nudge, weekly savings summary, re-engagement if car not charged for >7 days.

---

## What's in this repo

```
smart-charge-hub-v3.html    # Interactive prototype (self-contained, no dependencies)
EON_Next_Case_Study_v5.pptx # 10-slide presentation deck
README.md                   # This file
```

---

## Prototype

`smart-charge-hub-v3.html` is a fully self-contained HTML file. No build step, no dependencies, no internet required.

**To run:** open in any modern browser.

### App Prototype tab

Six screens covering the full user journey:

| Screen | Description |
|---|---|
| S0 - Trigger | Install day push notification |
| S1 - Connect car | VW ID.3 detected via account records, MPAN pre-filled |
| S2 - Consent | Half-hourly data consent explained in plain English, £117 saving shown upfront |
| S3 - Activate | Next Drive Smart tariff details, rates, schedule |
| S5 - 2-week wait | Progress tracker, estimated live date, pre-set schedule |
| S4 - Dashboard | Annual savings progress, vs peak rate comparison, charge history, Boost mode |

**Interactive elements:** schedule pills, Boost mode toggle, Edit schedule modal, "Remind me later" with feedback state.

### User Analytics Dashboard tab

GA4-style PM dashboard with five sections:

| Section | Contents |
|---|---|
| Overview | North Star metric (38% - target 60%), 4 KPI cards, activation trend chart |
| Activation Funnel | Visual funnel with drop-off %, step-level analysis table |
| Engagement | DAU/MAU trend, Alert CTR, Boost mode usage and post-boost behaviour |
| Business Impact | Revenue/cohort vs control, churn comparison, support contacts |
| OKRs | 3 objectives, 9 key results with progress bars and status badges |

---

## Key Design Decisions

| Decision | Rationale |
|---|---|
| Connect the **car**, not the charger | App connects via vehicle API - charger connection not yet supported |
| MPAN pre-populated | Already in E.ON Next account records for existing customers - removes #1 abandonment point |
| Savings shown before consent | Anchors motivation before the friction point |
| 2-week wait made transparent | Technical constraint that can't be removed - wizard makes it visible and keeps customers engaged |
| Pre-set schedule during wait | Commitment mechanism - customers who set a schedule are less likely to abandon during the wait |
| Boost mode | Directly answers the Sceptic persona's objection - control is always one tap away |

---

## North Star Metric

> **% of EV charger owners on Next Drive Smart with car connected within 30 days of install**
> Current: 38% - Target: 60% by September 2026

Supporting metrics across three layers: Adoption, Engagement, Business Impact. Guardrail: NPS and CSAT must hold at baseline - don't trade connection rate for customer confusion.

---

## Sources

| Fact | Source |
|---|---|
| £117/yr confirmed saving | E.ON Next press release, March 2026 |
| 8.5p/kWh off-peak rate | eonnext.com/tariffs/next-drive/smart |
| ~21% home charger owners not using smart charging | Andersen EV / What Car?, August 2025 |
| 5M+ E.ON Next customers | eonnext.com homepage |
| UK EV fleet +39% YoY | SMMT official motorparc data, 2024 |
| ZoomEV partnership | news.eonenergy.com |

---

## Notes

- All analytics data in the dashboard is **mock/modelled data** for illustrative purposes
- The prototype is built in vanilla HTML/CSS/JS - no frameworks, no external dependencies
- E.ON Next brand colours: `#FF4822` (orange), `#36164A` (dark purple), `#9400FF` (bright purple)
- E.ON Next logo SVG used with brand assets from E.ON Next

---

*Built by Shiv Contractor - March 2026*