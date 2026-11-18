# QA Across Python, API and Web Products

This chapter links testing methods to **fictional products**: a multilingual learning site, a private gift-exchange demo and a generic reporting dashboard. These are educational scenarios, not copies of private tests or verified production results.

## Choose the lowest useful test level

| Layer | Example | What it proves |
|---|---|---|
| Unit | Completion-rate function rejects zero denominator | Calculation contract at function level |
| Data quality | One synthetic case per key; totals reconcile | Input/output assumptions |
| API | POST with invalid payload returns a documented error | HTTP contract |
| Integration | Authorized user sees only permitted demo records | Cooperation of components |
| Browser E2E | Language toggle updates visible UI strings | Complete user journey in the test environment |
| Release | Evidence + owner review | Only the tested release candidate meets its gates |

## Example A — Multilingual learning app

An independent test design might cover: language switch; navigation across topics; form validation; session expiry; preserving study-progress state; keyboard accessibility; and correct handling of the unavailable-content state. **Never put real questions, answers, credentials or user activity in public fixtures.**

## Example B — Anonymous gift exchange

Use invented people `Demo A/B/C/D`, not real participants. Verify one unique giver and one unique recipient per participant, no self-assignment, one-way completion state, authorization and refusal of duplicate submissions. A successful small demonstration does not prove comprehensive security.

## Example C — Synthetic report dashboard

Use a tiny dataset with known counts and totals; exercise month filters, reset, no-data states, denominator recomputation and CSV export. A browser screenshot alone does not validate backend measures. Reconcile UI totals with the same fixture.

## A simple evidence format

```text
Case: DEMO-LANG-01
Environment: local synthetic fixture
Precondition: fictional content available
Action: switch display language
Expected: navigation, labels and validation messages change
Observed: NOT EXECUTED (example only)
Status: NOT VERIFIED
Evidence: none
```

## Test isolation

Create test data per run; use deterministic values and explicit cleanup. Never connect a learning suite to a private or live service without authorization. Keep tokens out of fixtures, logs and screenshots.

**RU:** связь unit, API, integration, Playwright/Selenium E2E и Data QA на трёх полностью вымышленных сценариях. Примеры — методология, а не отчёт о выполненных тестах.

References: [ISTQB](https://istqb.org/), [Playwright best practices](https://playwright.dev/docs/best-practices), [pytest](https://docs.pytest.org/en/stable/).
