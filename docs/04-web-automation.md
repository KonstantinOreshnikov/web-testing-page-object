# Web Automation / Автоматизация web

## English

Automate stable, valuable user journeys and critical regressions. Prefer locators that reflect how a user or accessibility tree identifies an element: role, label and visible text. Test IDs are useful explicit contracts when semantics are insufficient. Brittle CSS chains and XPath tied to layout create avoidable maintenance.

Rely on framework waiting and condition-based waits. Fixed sleeps make suites slow and flaky. Keep tests independent, create state through APIs or fixtures when appropriate, and capture traces, screenshots and logs on failure without leaking secrets.

## Русский

Автоматизируйте стабильные ценные пользовательские маршруты и критическую регрессию. Предпочитайте locators, отражающие восприятие пользователя или accessibility tree: role, label и видимый текст. Test ID полезен как явный контракт, когда семантики недостаточно. Хрупкие CSS-цепочки и XPath, завязанные на layout, повышают стоимость поддержки.

Используйте встроенное ожидание framework и condition-based waits. Фиксированные sleep делают тесты медленными и flaky. Тесты должны быть независимыми; состояние удобно создавать через API или fixtures.

Sources / Источники: [Playwright locators](https://playwright.dev/docs/locators), [Selenium waits](https://www.selenium.dev/documentation/webdriver/waits/)
