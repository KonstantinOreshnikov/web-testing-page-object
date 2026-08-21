# Page Objects and Architecture / Page Object и архитектура

## English

A Page Object is an interface to a page or meaningful component. It centralizes locators and interaction details while tests express intent. Methods should represent services such as `sign_in`, `search` or `submit_order`, not expose every click as a separate public method.

Page Objects normally should not assert test outcomes. They may verify that the expected page loaded; business assertions remain in tests. Avoid a giant base page, hidden global drivers and inheritance trees. Prefer small components and composition.

## Русский

Page Object — интерфейс к странице или значимому компоненту. Он централизует locators и детали взаимодействия, а тесты выражают намерение. Методы должны представлять сервисы вроде `sign_in`, `search` или `submit_order`, а не превращать каждый click в публичный метод.

Page Objects обычно не проверяют результат теста. Они могут убедиться, что нужная страница загрузилась; бизнес-assertions остаются в тестах. Избегайте гигантского base page, глобального driver и глубокого наследования; используйте небольшие компоненты и композицию.

Source / Источник: [Selenium Page Object Models](https://www.selenium.dev/documentation/test_practices/encouraged/page_object_models/)
