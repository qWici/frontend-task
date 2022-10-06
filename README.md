# frontend-task
Тестове завдання

## Опис

Уявіть, що вам надійшло замовлення від дуже популярної міні-гри в досить 
великій соціальній мережі. Назва гри - "Гоночки". Суть гри полягає в тому,
що користувачі виконують заїзди, намагаючись пройти одну й ту саму дистанцію за
максимально короткий проміжок часу. Варто зауважити, що гра присутня 
тільки в мобільному вигляді, тобто розроблена спеціально для мобільних пристроїв 
за розмірами, починаючи з iPhone 5S і закінчуючи iPad Pro. 

Кількість користувачів наразі перевищує 4 мільйони.

## Завдання
Ваше завдання полягає в тому, що в цьому застосунку необхідно відобразити 
рейтингову таблицю з користувачами. Немає необхідності що-небудь 
дійсно довантажувати з будь-яких серверів, ці дані можна просто 
замокати й імітувати підвантаження даних відображенням лоадера.

До всього іншого, список користувачів необхідно згенерувати самостійно.
Тип даних користувача можна взяти [звідси](#Типи данних). Змінювати ці типи
даних **заборонено**.

Як виконану роботу необхідно викласти проєкт на GitHub і 
надати посилання для перегляду вихідних кодів.

## Вимоги до технологій
- React **без використання класових компонентів**
- React Hooks
- Мінімальна ширина екрана - 320px. Максимальна 1920px

## Вимоги до візуалу
- При первинному завантаженні необхідно відображати 50 перших користувачів
- Додаток не повинен гальмувати навіть коли на екрані понад 1000 користувачів
- Здійснювати lazy load підвантаження коли скрол наближається до нижньої межі
екрана. Підвантаження здійснюється по 50 користувачів
- Якщо ім'я людини не поміщається в межі екрана, обрізаємо його три крапки
- Усі аватарки користувачів у будь-який момент часу мають бути на одному 
вертикальному рівні. Після підвантаження нових користувачів і в разі, коли їхні
аватарки знаходяться правіше попередніх, аватарки попередніх користувачів 
необхідно **плавно** розмістити на рівень із новими 
- Кліком на користувача ми можемо виділити його фіолетовим кольором
- Виконана робота повинна бути візуально наближеною до [макету](#макет) зазначеного 
нижче. Поле штрафний час реалізовувати не потрібно
- Як зображення користувача необхідно показати шолом із кольором, 
який він колись обрав. SVG-зображення шолома є в репозиторії

## Здача роботи
- Як виконану роботу необхідно викласти проєкт на GitHub і надати посилання для перегляду вихідних кодів.
- Розгорнути цей додаток для візуального перегляду

## Типи данних
```typescript
// Список можливих кольорів
enum Color {
  RED, 
  GREEN, 
  BLUE
}

// Користувач. Позиція в рейтинговій таблиці визначається позицією в 
// масиві користувачів
interface User {
  // Улюблений колір 
  color: Color;
  // Повне ім'я
  name: string;
  // Швидкість заїзду
  speed: number;
  // Час заїзду. Виражено в мілісекундах
  time: number;
}
```

## Макет
![image](https://user-images.githubusercontent.com/34907325/76761753-d2b26380-67b1-11ea-9e81-c59cce69a67f.png)
