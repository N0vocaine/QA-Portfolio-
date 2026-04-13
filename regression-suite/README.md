# Regression Test Suite – Digital Medical App

**Version 1.0 | April 2026**

> All content is anonymised. Professional types, authentication methods, and product terminology have been generalised to protect confidentiality.

---

## Context and motivation

During my internship at a digital healthcare company, I noticed that the existing test cases for the mobile app were fragmented and in several areas outdated — some no longer reflected the current flows, others were missing entire sections that had been added to the product over time. Coverage was also uneven: certain high-risk areas had sparse tests while lower-risk areas had more.

I raised this with the team and offered to rebuild the regression suite from scratch, using the live app, current user stories, and acceptance criteria as my source of truth. The goal was not only to improve coverage but to produce something the team could actually use going forward — structured, prioritised, and executable without needing extra context.

This file is the result of that initiative.

---

## What I built

A full regression suite for a mobile telehealth app that connects patients with healthcare professionals across multiple care categories. The suite covers **197 test cases across 18 functional areas**, structured to follow the real user journey from installation through to cross-platform behaviour.

---

## How I approached it

### Map the journey, not just the features

I structured the folders in the order a real user experiences the app: install → onboarding → authentication → home screen → category selection → question flow → care outcome (queue or appointment) → communication → notifications. Each folder mirrors a stage in that journey. This makes it faster to triage failures and understand the downstream impact of any broken flow.

### Establish risk before writing test cases

In a medical app, not all failures are equal. A broken animation is annoying. A broken authentication step or a wrong care outcome is a patient safety risk. Before writing individual test cases, I built a **High Risk Areas** sheet — 12 areas where a defect could cause wrong care, blocked access, or data exposure. That list directly shaped how I assigned priorities across the suite.

The result: the majority of test cases are P1 Critical or P2 High. P3 Medium is reserved for cosmetic or genuinely low-impact scenarios.

### Make it usable in practice, not just as documentation

Two supporting sheets were added to make the suite operational:

- **Smoke Test Checklist** – 15 critical-path checks that must pass before any full regression run or deployment. Designed to catch blockers in under 30 minutes.
- **Test Data Matrix** – 12 user profiles (new user, user mid-queue, user with failed authentication, symptom leading to emergency escalation, etc.) that map directly to test cases and remove ambiguity about test setup.

### Areas I deliberately did not skip

- **Error Handling & Network** (14 cases): a user who loses connection while mid-queue must not lose their active care state.
- **Data Integrity** (6 cases, all P1): incorrect data in a medical context has direct clinical consequences.
- **Accessibility** (6 cases): accessible healthcare is non-negotiable, not a stretch goal.
- **Security & Privacy** (7 cases): session handling, input validation, and data exposure are in scope given the sensitivity of health data.

---

## File structure

| Sheet | Contents |
|---|---|
| Overview | Summary table: case counts and priority breakdown per folder |
| All Test Cases | Full flat list — useful for filtering or tool import |
| Folders 1–18 | Individual sheets per area: preconditions, steps, expected results, pass/fail |
| Smoke Test Checklist | 15 pre-regression checks |
| Test Data Matrix | 12 user profiles mapped to coverage areas |
| High Risk Areas | 12 prioritised risks with rationale |
