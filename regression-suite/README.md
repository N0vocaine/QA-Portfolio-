# Regression Test Suite – Digital Medical App

**Version 1.0 | April 2026**

> All content is anonymised. Professional types, authentication methods, and product terminology have been generalised to protect confidentiality.

---

## Context and motivation

During my internship at a digital healthcare company, I noticed that the existing test cases were not well organised and some were outdated. Some flows had changed in the app but were not updated in the tests, and some areas were missing tests completely.

Test coverage was also not balanced — some important areas had very few tests, while less important areas had more.

Because of this, I suggested rebuilding the regression suite so it would be easier to use and reflect the current product.

---

## What I built

A full regression test suite for a mobile healthcare app. It includes **197 test cases across 18 functional areas** and follows the main user journey in the app.

---

## How I approached it

### 1. Follow the user journey

Instead of organising tests by feature only, I structured them based on how a user moves through the app:

install → onboarding → login → home → selecting care → answering questions → outcome (queue or booking) → communication → notifications

This makes it easier to understand where a problem happens and what it affects.

### 2. Focus on risk first

Before writing test cases, I identified **12 high-risk areas** where issues could have serious impact, such as:

- blocked access to care
- wrong care outcome
- data issues

Based on this, I set priorities:

- **P1 / P2** → important flows
- **P3** → low-impact or UI issues

### 3. Make it practical to use

I added extra sheets to help the team use the suite easily:

- **Smoke Test Checklist** – 15 important checks to quickly verify the app before a release
- **Test Data Matrix** – 12 user scenarios (e.g. new user, user in queue, failed login) to make test setup clear

---

## Important areas covered

- **Error Handling & Network** (14 cases) – users should not lose their progress if connection is lost
- **Data Integrity** (6 cases, all P1) – correct data is critical in healthcare
- **Accessibility** (6 cases) – important for all users
- **Security & Privacy** (7 cases) – covers login, sessions, and data safety

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
