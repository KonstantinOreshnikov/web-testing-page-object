# Synthetic Test Design Matrix and QA Evidence

Tests are valuable when they expose a specific failure risk, not when they merely increase the number of passing checks. This is an independently authored matrix with **invented expectations**.

| ID | Target | Synthetic scenario | Expected result | Level | Execution |
|---|---|---|---|---|---|
| KPI-01 | Calculation | 4 eligible cases, 3 completed | 75% completion | Unit | NOT RUN |
| KPI-02 | Calculation | 0 eligible cases | Undefined rate; no divide-by-zero | Unit | NOT RUN |
| API-01 | Demo service | POST missing required field | Contract-defined 4xx with useful error | API | NOT RUN |
| API-02 | Demo service | Two identical idempotent requests | No duplicate operation, if contract specifies idempotency | API | NOT RUN |
| UI-01 | Training site | Change language from EN to RU | Visible text updates consistently | Browser | NOT RUN |
| UI-02 | Demo dashboard | Choose a month with no records | Explicit no-data state | Browser | NOT RUN |
| UI-03 | Demo form | Submit invalid email-shaped text | Accessible validation error | Browser | NOT RUN |

## A minimal failure report

```text
Title: Summary total differs after applying date filter
Fixture: SYNTH-2026-001
Expected: filtered detail sum equals displayed summary
Actual: [record only after test execution]
Steps: load fixture → select period → inspect cards/table
Severity: evaluate from business impact; not automatically Critical
Evidence: screenshot and machine-readable assertion attached when run
Status: NOT RUN
```

## Contract versus implementation

`pytest` parametrization covers input variants; `requests` or a framework's test client checks APIs; Playwright or Selenium checks browser journeys. A Page Object should expose page actions and state, while the test asserts expected behavior. Never assert a test PASS because code is present.

## QA gates before release

1. Requirement and scope documented.
2. Test fixture synthetic and reproducible.
3. Expected outputs calculated independently.
4. Automated assertions actually executed.
5. Failed cases triaged with reproducible evidence.
6. Regression on previously working flows.
7. Build/environment and deployment status recorded separately.

A blocked runtime test remains **BLOCKED**; a design-only matrix is **NOT RUN**.

**RU:** готовый шаблон test matrix, баг-репорта и gate-ledger. Он помогает планировать тесты, но не выдаёт их за выполненные.

References: [Selenium](https://www.selenium.dev/documentation/), [Playwright](https://playwright.dev/docs/intro), [pytest](https://docs.pytest.org/en/stable/).
