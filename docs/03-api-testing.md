# API Testing / Тестирование API

## English

Test the contract and observable behavior: method, path, authentication, headers, status, schema, data semantics, idempotency where promised, pagination, rate-limit behavior and error format. Include positive, negative, boundary and authorization cases.

```python
def test_create_item(api_client) -> None:
    response = api_client.post("/items", json={"name": "sample"})
    assert response.status_code == 201
    payload = response.json()
    assert payload["name"] == "sample"
    assert isinstance(payload["id"], str)
```

Do not expose credentials in source or reports. Use controlled test data and clean it up. Separate transport failures from application assertions so diagnostics remain useful.

## Русский

Проверяйте контракт и наблюдаемое поведение: method, path, authentication, headers, status, schema, смысл данных, обещанную idempotency, pagination, rate limits и формат ошибок. Добавляйте позитивные, негативные, граничные и authorization-сценарии.

Не размещайте credentials в коде или отчётах. Используйте контролируемые тестовые данные и очищайте их. Отделяйте транспортные ошибки от бизнес-assertions.

Source / Источник: [Playwright API testing](https://playwright.dev/docs/api-testing)
