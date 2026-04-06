# {{program-name}}

## Program Description
{{program-description}}

## Purpose & Scope

**Purpose:** {{program-purpose}}

**In Scope:**
- {{scope-item-1}}
- {{scope-item-2}}

**Out of Scope:**
- {{out-of-scope-item}}

## Stakeholder Registry

| Name | Role | Organization | Contact | Engagement Frequency |
|---|---|---|---|---|
| {{sponsor-name}} | Program Sponsor | {{sponsor-org}} | {{sponsor-contact}} | Monthly (SteerCo) |
| {{pgm-name}} | Program Manager | iPGM | {{pgm-contact}} | Weekly |
| {{eng-lead-name}} | Engineering Lead | {{eng-org}} | {{eng-contact}} | Weekly |
| {{product-owner-name}} | Product Owner | {{po-org}} | {{po-contact}} | Bi-weekly |
| {{ops-lead-name}} | Operations Lead | {{ops-org}} | {{ops-contact}} | Monthly |

---

## New Program Setup Checklist

Complete this checklist after creating a repo from this template:

- [ ] Rename this repo from `iPGM-project-template` to your program name
- [ ] Replace all `{{tokens}}` in this README with real program details
- [ ] Update `name` and `description` in `package.json`
- [ ] Update `ORG_NAME` in `.github/workflows/report-status.yml` if needed
- [ ] Add `ORG_PORTFOLIO_TOKEN` secret to this repo (or confirm org-level secret is available)
- [ ] Replace `src/index.js` with your program's code
- [ ] Fill in program initiation docs in `docs/1-program-initiation/`
- [ ] Run the iPGM Portfolio Sync manually to register this program on the board
- [ ] Update Status, Phase, PEI Level, and Program Manager on the portfolio board

---

## Repository Structure

```
{{program-name}}/
+-- docs/
|   +-- 1-program-initiation/       Phase 1 artifacts
|   +-- 2-planning-roadmapping/     Phase 2 artifacts
|   +-- 3-delivery-execution/       Phase 3 artifacts
|   +-- 4-go-live-closure/          Phase 4 artifacts
|   +-- 5-monitoring-control/       Phase 5 artifacts (RAID, KPI, decisions)
|   +-- 6-governance-reporting/     Phase 6 artifacts
|       +-- status-reports/         Weekly/monthly status reports
|       +-- executive-updates/      Leadership update docs
|       +-- steering-committee-packs/   SteerCo decks
+-- meeting-notes/                  Dated meeting notes files
+-- src/                            Program source code
+-- .github/
    +-- workflows/                  report-status.yml (portfolio trigger)
    +-- ISSUE_TEMPLATE/             iPGM issue templates
```

---

## iPGM Toolkit Inventory

| WPID | Work Product | Status | Link |
|---|---|---|---|
| 1.1 | Program Intake | Pending | docs/1-program-initiation/program-intake.md |
| 1.2 | Program Charter | Pending | docs/1-program-initiation/program-charter.md |
| 1.3 | Vision, Goals & Drivers | Pending | docs/1-program-initiation/vision-goals-drivers.md |
| 1.4 | Requirements Library | Pending | docs/1-program-initiation/requirements-library.md |
| 1.5 | Stakeholder Registry | See above | README.md |
| 2.1 | Architecture & Technical Design Library | Pending | docs/2-planning-roadmapping/architecture-design-library.md |
| 2.2 | Program Roadmap | Pending | docs/2-planning-roadmapping/program-roadmap.md |
| 2.3 | Workstream Delivery Plans | Pending | docs/2-planning-roadmapping/workstream-delivery-plans.md |
| 2.4 | Cross-Project Dependency Map | Pending | docs/2-planning-roadmapping/cross-project-dependency-map.md |
| 2.5 | Communications Plan | Pending | docs/2-planning-roadmapping/communications-plan.md |
| 2.6 | Launch Strategy | Pending | docs/2-planning-roadmapping/launch-strategy.md |
| 2.7 | Assumptions Register | Pending | docs/2-planning-roadmapping/assumptions-register.md |
| 3.1 | ENG Team Tracking | Pending | docs/3-delivery-execution/eng-team-tracking.md |
| 3.2 | Vendor & Procurement Tracking | Pending | docs/3-delivery-execution/vendor-procurement-tracking.md |
| 3.3 | Implementation Guides | Pending | docs/3-delivery-execution/implementation-guides.md |
| 4.1 | Go-Live Readiness Checklist | Pending | docs/4-go-live-closure/go-live-readiness-checklist.md |
| 4.2 | Acceptance Testing & Sign-Off | Pending | docs/4-go-live-closure/acceptance-testing.md |
| 4.3 | Cutover & Backout Plans | Pending | docs/4-go-live-closure/cutover-backout-plan.md |
| 4.4 | Post-Go-Live Validation | Pending | docs/4-go-live-closure/post-go-live-validation.md |
| 4.5 | Program Closure Report | Pending | docs/4-go-live-closure/program-closure-report.md |
| 5.1 | RAID Log | Pending | docs/5-monitoring-control/raid-log.md |
| 5.2 | Program KPI Dashboard | Pending | docs/5-monitoring-control/kpi-dashboard.md |
| 5.3 | Risk Management Framework | Pending | docs/5-monitoring-control/risk-management-framework.md |
| 5.4 | Action Item Tracker | Pending | docs/5-monitoring-control/action-item-tracker.md |
| 5.5 | Decision Register / Change Log | Pending | docs/5-monitoring-control/decision-register.md |
| 5.6 | Event Log | Pending | docs/5-monitoring-control/event-log.md |
| 5.7 | Compliance & Risk Governance | Pending | docs/5-monitoring-control/compliance-risk-governance.md |
| 6.1 | Governance & RACI | Pending | docs/6-governance-reporting/governance-raci.md |
| 6.2 | Status Reports | Pending | docs/6-governance-reporting/status-reports/ |
| 6.3 | Executive/Leadership Updates | Pending | docs/6-governance-reporting/executive-updates/ |
| 6.4 | Steering Committee Packs | Pending | docs/6-governance-reporting/steering-committee-packs/ |
| 6.5 | Meeting Notes | Pending | meeting-notes/ |
| 6.6 | Program Toolkit Inventory | This file | README.md |
| 6.7 | Program Calendar | Pending | docs/6-governance-reporting/program-calendar.md |

---

## Portfolio Reporting

This repo is pre-wired to report to the **iPGM Program Portfolio** board automatically.

- **On every push:** `report-status.yml` dispatches a `repo-updated` event to `iPGM-hub`
- **Weekly baseline:** The hub syncs all repos every Monday at 06:00 UTC
- **Escalate an issue:** Apply the `portfolio-report` label to any open issue — it will appear on the portfolio board on the next sync

The `ORG_PORTFOLIO_TOKEN` secret must be available to this repo (org-level secret recommended).

---

## Getting Started

```bash
npm install
npm start
```
