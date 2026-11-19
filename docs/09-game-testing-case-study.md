# Applied QA case: Caribbean Merchant v1.0

An independently authored Caribbean trading game is a useful **real-world-style subject** for web and game-testing practice. It has a deterministic state model, local saves, trade transactions, contracts, missions, localization and an offline interface.

**[Open the public project](https://github.com/KonstantinOreshnikov/KonstantinOreshnikov/tree/main/projects/caribbean-merchant)** · **[Read its original QA evidence](https://github.com/KonstantinOreshnikov/KonstantinOreshnikov/blob/main/projects/caribbean-merchant/testing/original-qa-report.md)**

## What actual testing established

The v1.0 release report records **26 local browser scenarios PASS** in Chromium using Playwright with injected HTML and a localStorage substitute. This is release-specific evidence and **not** a claim that this repository's educational legacy scripts executed those tests.

A human owner tested earlier builds and rejected an unreadable map and cumbersome commerce UI. Those observations became concrete regression requirements.

## Example regression design

| Risk | Test idea | Expected oracle |
|---|---|---|
| Hidden cash / cargo while scrolling | Scroll into trade rows | Treasury, used and free capacity stay visible |
| Market purchase overspends | Buy with insufficient funds | No negative balance, no phantom items |
| Contract accepted without delivery stock | Attempt mission with missing goods / full hold | Atomic rejection with actionable reason |
| Factory autosale loses stock | Advance day at price floor and reserve | Sold + stored units reconcile with produced units |
| Warehouse growth duplicates credits | Upgrade same warehouse to 300 | Costs charged once per accepted upgrade |
| Language label collision | Switch RU/EN/AZ, capture narrow viewport | No text clipping, stable port selection |
| Achievement payout repeats | Reload / reimport earned award | No duplicate reputation or credits |
| Pirate auto-battle soft-lock | Resolve both win/loss | Game returns to valid voyage/port state |

## Evidence requirements

For each executed test record the game version/hash, input state, steps, expected/actual balance, browser, screenshot or structured output and defect retest result. Playability on an actual Windows `file://` path remains unverified by the original automated harness.

## How it relates to this lab

Apply principles from [test design](02-test-design.md), [web automation](04-web-automation.md), [Page Objects](05-page-objects.md) and [evidence/traceability](08-test-matrix-and-evidence.md) to an evolving interactive product rather than a toy form.

**RU:** это связанный пример гейм-тестирования: условия для прохождения контрактов, балансы денег/товаров, состояние после боя, локализация и сохранения. Важны не только клики, но и проверки инвариантов.

[Quality Engineering Lab](../README.md) · [Caribbean Merchant](https://github.com/KonstantinOreshnikov/KonstantinOreshnikov/tree/main/projects/caribbean-merchant)
