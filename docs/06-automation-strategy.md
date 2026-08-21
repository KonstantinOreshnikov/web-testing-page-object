# Automation Strategy and Reporting / Стратегия и отчётность

## English

Automation is an investment decision. Select cases by risk, repetition, stability, execution cost and diagnostic value. Keep most checks below the UI; use a focused UI layer for essential journeys. A green suite is useful only when failures are trustworthy and results are visible.

Report behavior, environment, duration and evidence. Track flaky-test rate, failure causes and time to diagnosis—not just test count. Quarantine only with an owner and deadline. Parametrization reduces duplication when cases share behavior; fixtures provide explicit modular setup and cleanup.

## Русский

Автоматизация — инвестиционное решение. Выбирайте сценарии по риску, повторяемости, стабильности, стоимости выполнения и диагностической ценности. Большинство проверок держите ниже UI, оставляя на UI критические пользовательские маршруты.

Отчёт должен показывать поведение, окружение, длительность и evidence. Измеряйте flaky rate, причины падений и время диагностики, а не только количество тестов. Quarantine допустим только с владельцем и сроком исправления.

Sources / Источники: [pytest fixtures](https://docs.pytest.org/en/stable/explanation/fixtures.html), [pytest parametrization](https://docs.pytest.org/en/stable/how-to/parametrize.html)
