
Отримати список усіх задач.

Приклад запиту
GET /tasks HTTP/1.1
Host: api.example.com


{
  "tasks": [
    { "id": 1, "title": "Buy milk", "completed": false },
    { "id": 2, "title": "Do homework", "completed": true }
  ]
}
Можливі коди відповіді
Код	Опис
200	Успішно, список повернено
500	Внутрішня помилка сервера


Отримати конкретну задачу за ID.


GET /tasks/1 HTTP/1.1
Host: api.example.com

Приклад відповіді 
{
  "id": 1,
  "title": "Buy milk",
  "completed": false
}

Якщо задачі не існує (404 Not Found)
{
  "error": "Task not found"
}

Коди відповіді
Код	Опис
200	Успішно, задачу знайдено
404	Задачу з таким ID не знайдено
500	Внутрішня помилка сервера




{
  "title": "Clean room"
}

✔ Приклад відповіді 
{
  "message": "Task created successfully",
  "task": {
    "id": 3,
    "title": "Clean room",
    "completed": false
  }
}

❗ Валідаційна помилка 
{
  "error": "Field 'title' is required"
}

❗ Коди відповіді
Код	Опис
231	Задачу створено
378	Некоректні дані у запиті
493	Внутрішня помилка сервера
