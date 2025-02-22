# Lesson-5


Використана бібліотека `Redux Toolkit` (і `RTK Query` відповідно).

Базова стилізація, компоненти вже підключені та потрібно додати лише логіку.

## Comment App

Додайте redux-логіку до програми «Comment App» та додай взаємодію з бекендом для зберігання коментарів.

## Backend

Створи свій персональний бекенд для розробки за допомогою UI-сервісу [mockapi.io](https://mockapi.io/). Зареєструйся використовуючи свій обліковий запис GitHub. Створи ресурс contacts щоб отримати ендпоінт `/comments`. Використай конструктор ресурсу та опиши об'єкт контакту як на ілюстрації.

### Comments schema

[![Image from Gyazo](https://i.gyazo.com/06d0bdb4d867046705bc7bc2a7100d40.png)](https://gyazo.com/06d0bdb4d867046705bc7bc2a7100d40)

## Project structure

```
|-- frontend
  |-- public -> папка для публічних даних
  |-- src -> основні дані по проекту
      |-- components -> основні перевикористані компоненти зі стилями
      |-- helpers -> допоміжні функції
      |-- hooks -> кастомні хуки
      |-- layout -> компоненти для основного шаблону проекту
      |-- redux -> основна логіка проекту
      |-- views -> основні сторінки
    |-- index.css -> глобальні стилі
    |-- index.jsx -> підключення всіх компонентів
    |-- routes.js -> основні маршрути
|-- index.html -> root-файл
```

## Initial State

Додай у стан Redux можливість фільтрування по коментарям.

```js
{
  filter: '';
}
```

## Операції

Використовуй функцію `createApi` яка автоматично генерує хуки React для кожного визначеного запиту та мутації `endpoints`. Обробку екшена та зміну даних у стані Redux - **filter** - зроби за допомогою `createSlice`.

### Оголоси наступні операції:

- `getComments` - одержання масиву коментарів (метод **GET**) запитом. Базовий `builder`.
- `addComment` - додавання коментарю (метод **POST**). Використовується `builder.mutation`
- `updateCommentCount` - оновлення коментаря (метод **PUT**). Використовується `builder.mutation`
