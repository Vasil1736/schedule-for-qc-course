# Coverage Report

## Загальне покриття

* Statements/Instructions: **32.27%**
* Branches: **11.59%**
* Functions/Methods: **11.84%**
* Lines: **34.11%**

## Аналіз

### Які функції/класи покриті найкраще?

Найкраще покриті утилітарні функції та допоміжні модулі:

* `src/utils/scheduleUtils.js` — 100% покриття Statements, Branches, Functions та Lines.
* `src/helper/getHref.js` — 100% покриття.
* `src/helper/setLink.js` — 100% покриття.
* `src/helper/search.js` — 100% покриття.
* `src/helper/handleFormSubmit.js` — 100% покриття.
* `src/helper/cardObjectHandler.js` — 100% покриття.
* `src/utils/formUtils.js` — 100% покриття.
* `src/utils/selectUtils.js` — 100% покриття.
* `src/utils/urlUtils.js` — 100% покриття.

Також результати mutation testing показали 100% Mutation Score (29 з 29 мутацій виявлено), що свідчить про високу якість тестів для модулів `getHref.js` та `scheduleUtils.js`.

### Які потребують додаткових тестів?

Найменше покриття мають React-компоненти та контейнери:

* `TeachersPage.js`
* `RoomsPage.js`
* `LessonPage.js`
* `LoginForm.js`
* `RegistrationForm.js`
* `NavigationPanel.js`
* `ScheduleBoard.js`
* `ScheduleDialog.js`
* `TemporaryScheduleForm.js`
* більшість файлів у папках `containers`, `sagas`, `reducers` та `services`.

У багатьох із цих файлів покриття становить менше 10%, що означає відсутність тестів для основної логіки компонентів, взаємодії з користувачем, Redux та асинхронних операцій.

### Чому деякі branches не покриті?

Покриття Branches становить лише 11.59%, що значно нижче за інші показники. Основні причини:

* не перевірені альтернативні гілки `if/else`;
* відсутні тести для обробки помилок (`catch`);
* не перевірені сценарії з `null`, `undefined` або порожніми даними;
* відсутні тести для асинхронних запитів та Redux Saga;
* не покриті умови рендерингу React-компонентів;
* не перевірені негативні сценарії роботи форм.

Для підвищення Branch Coverage необхідно створити окремі тести для всіх альтернативних шляхів виконання коду.

## Висновок

У проєкті успішно виконуються всі 162 тести (35 тестових наборів). Найкраще покриті утилітарні функції та helper-модулі, однак значна частина React-компонентів, контейнерів, Redux reducers, services та sagas майже не тестується. Загальне покриття коду становить лише 32.27%, тому основним напрямком покращення є написання інтеграційних тестів для компонентів інтерфейсу та тестів для бізнес-логіки Redux.

## Скріншот

<img width="1579" height="210" alt="image" src="https://github.com/user-attachments/assets/f240e655-ac62-4e76-80bf-85d39aba99a4" />
