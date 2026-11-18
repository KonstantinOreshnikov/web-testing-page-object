# Quality Engineering Lab / Лаборатория Quality Engineering

A bilingual path from test analysis and test design to maintainable API and web automation.

Двуязычный маршрут от тест-анализа и тест-дизайна до поддерживаемой автоматизации API и web.

## English

This repository transforms earlier QA, API, Selenium and Page Object exercises into an original, tool-aware learning path. Testing is treated as risk reduction and evidence gathering—not as clicking until something breaks.

## Русский

Репозиторий превращает ранние задания по QA, API, Selenium и Page Object в оригинальный последовательный маршрут. Тестирование рассматривается как снижение рисков и сбор свидетельств, а не как «кликать, пока не сломается».

## Learning path / Учебный маршрут

1. [Testing foundations / Основы тестирования](docs/01-testing-foundations.md)
2. [Test design / Тест-дизайн](docs/02-test-design.md)
3. [API testing / Тестирование API](docs/03-api-testing.md)
4. [Web automation / Автоматизация web](docs/04-web-automation.md)
5. [Page objects and architecture / Page Object и архитектура](docs/05-page-objects.md)
6. [Automation strategy and reporting / Стратегия и отчётность](docs/06-automation-strategy.md)
7. [Synthetic project QA / QA на тестовых проектах](docs/07-synthetic-project-qa.md)
8. [Test matrix and evidence / Test matrix и доказательства](docs/08-test-matrix-and-evidence.md)
9. [Practice cases / Практические задания](exercises/README.md)

## Core rules / Основные правила

- Link each test to a risk, requirement, behavior or defect hypothesis.
- Prefer the lowest practical test level.
- Keep tests isolated, deterministic and observable.
- Validate contracts and behavior, not implementation trivia.
- Use semantic locators and explicit assertions; avoid fixed sleeps.
- A Page Object exposes page services and normally does not contain test assertions.

---

- Связывайте тест с риском, требованием, поведением или гипотезой дефекта.
- Выбирайте самый низкий практически достаточный уровень тестирования.
- Делайте тесты изолированными, детерминированными и наблюдаемыми.
- Проверяйте контракт и поведение, а не случайные детали реализации.
- Используйте семантические locators и явные assertions; избегайте фиксированных sleep.
- Page Object предоставляет сервисы страницы и обычно не содержит тестовых assertions.

## Sources / Источники

[ISTQB CTFL](https://istqb.org/certifications/certified-tester-foundation-level-ctfl-v4-0/), [Selenium documentation](https://www.selenium.dev/documentation/), [Playwright best practices](https://playwright.dev/docs/best-practices), [pytest documentation](https://docs.pytest.org/en/stable/).

## Cross-project practice / Связь с проектами

Use the same QA discipline for a fictional reporting pipeline, an educational website and a gift-exchange demo: agree the contract, create synthetic fixtures, run the lowest practical tests, reconcile outputs and keep evidence. The examples explain the approach; they do **not** claim that E2E was executed against any private production site.

Синтетический сценарий → ожидаемый результат → проверка → evidence → исправление → повторный тест. Реальные логины, вопросы, ответы и пользовательские данные не используются.

[Python examples](https://github.com/KonstantinOreshnikov/python-lessons-geekbrains) · [Linux lab](https://github.com/KonstantinOreshnikov/linux-testing-python) · [Git workflow](https://github.com/KonstantinOreshnikov/git-instruction-workshop)

## Legacy / Исторические материалы

Existing learning code remains unchanged until a separate consolidation review.

Существующий учебный код остаётся без изменений до отдельной проверки консолидации.

## License

MIT. See [LICENSE](LICENSE).
