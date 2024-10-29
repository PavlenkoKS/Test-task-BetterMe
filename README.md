<h1 align="center">Test-task-BetterMe</h1>
<h4>Тест-кейс 1: Перевірка отримання статусу 200</h4>
<p>Опис: Переконатися, що при відправці POST запиту, у відповіді статус код буде 200.</p>
<ol><b>Кроки відтворення:</b>
<li>Відправити POST запит до ендпоінту https://petstore.swagger.io/v2/pet з таким тілом запиту:</li>
   <code>{
  "id": 0,
  "category": {
    "id": 0,
    "name": null
  },
  "name": "TestName1",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 0,
      "name": "test"
    }
  ],
  "status": "available"
}</code>
<li>Отримати JSON-відповідь</li>
</ol>
<ol><b>Очікуваний результат:</b>
<li>Запит відправлено.</li>
<li>Отримано JSON-відповідь зі статусом 200 у такому вигляді:</li>
   <code>{
    "id": 9223372036854097051,
    "category": {
        "id": 0
    },
    "name": "TestName1",
    "photoUrls": [
        "string"
    ],
    "tags": [
        {
            "id": 0,
            "name": "test"
        }
    ],
    "status": "available"
}</code>
</ol>
<hr>
<h4>Тест-кейс 2: Перевірка відповіді при некоректному запиті</h4>
<p>Опис: Переконатися, що при некоректному запиті сервер повертає статус-код 400 та повідомлення про помилку.</p>
<ol><b>Кроки відтворення:</b>
<li>Відправити POST запит до ендпоінту https://petstore.swagger.io/v2/pet з таким тілом запиту:</li>
   <code>{{}
  "id": 0,
  "category": {
    "id": 0,
    "name": null
  },
  "name": "TestName1",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 0,
      "name": "test"
    }
  ],
  "status": "available"
}</code>
<li>Отримати JSON-відповідь з помилкою.</li>
</ol>
<ol><b>Очікуваний результат:</b>
<li>Запит відправлено.</li>
<li>Отримано JSON-відповідь зі статусом 400 з помилкою:</li>
   <code>{
    "code": 400,
    "type": "unknown",
    "message": "bad input"
}</code>
</ol>
<hr>
<h4>Тест-кейс 3: Перевірка часу відповіді сервера</h4>
<p>Опис: Переконатися, що сервер відповідає протягом допустимого часу (наприклад, 500 мс).</p>
<ol><b>Кроки відтворення:</b>
<li>Відправити POST запит до ендпоінту https://petstore.swagger.io/v2/pet з таким тілом запиту:</li>
   <code>{
  "id": 0,
  "category": {
    "id": 0,
    "name": null
  },
  "name": "TestName1",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 0,
      "name": "test"
    }
  ],
  "status": "available"
}</code>
<li>Отримати JSON-відповідь</li>
<li>Оцінити час відповіді сервера</li>
</ol>
<ol><b>Очікуваний результат:</b>
<li>Запит відправлено.</li>
<li>Отримано JSON-відповідь зі статусом 200 у такому вигляді:</li>
   <code>{
    "id": 9223372036854097051,
    "category": {
        "id": 0
    },
    "name": "TestName1",
    "photoUrls": [
        "string"
    ],
    "tags": [
        {
            "id": 0,
            "name": "test"
        }
    ],
    "status": "available"
}</code>
<li>Час відповіді сервера менше 500 мс</li>
</ol>
<hr>
<p>За наявності вимог до типу даних та обовязковості полів також пишуться тести для їх перевірки. Наприклад:</p>
<h4>Тест-кейс 3: Перевірка типу даних для tags</h4>
<p>Опис: Перевірити, що tags є масивом об’єктів, кожен з яких має числове id і рядкове name.</p>
<ol><b>Кроки відтворення:</b>
<li>Відправити POST запит до ендпоінту https://petstore.swagger.io/v2/pet з таким тілом запиту:</li>
   <code>{
  "id": 0,
  "category": {
    "id": 0,
    "name": null
  },
  "name": "TestName1",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 0,
      "name": "test"
    }
  ],
  "status": "available"
}</code>
<li>Отримати JSON-відповідь</li>
<li>Перевірити поле tags</li>
</ol>
<ol><b>Очікуваний результат:</b>
<li>Запит відправлено.</li>
<li>Отримано JSON-відповідь зі статусом 200 у такому вигляді:</li>
   <code>{
    "id": 9223372036854097051,
    "category": {
        "id": 0
    },
    "name": "TestName1",
    "photoUrls": [
        "string"
    ],
    "tags": [
        {
            "id": 0,
            "name": "test"
        }
    ],
    "status": "available"
}</code>
<li>tags — масив, кожен об'єкт у tags містить числове поле id і текстове поле name.</li>
</ol>
