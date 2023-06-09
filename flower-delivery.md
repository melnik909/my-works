# Примеры описания кейса из руководства для сервиса по доставке цветов
## При открытии модального окна с формой авторизации приложение не переносится пользователя в поле ввода "Email"
### Воспроизведение ошибки
В верхней части страницы нажмите на кнопку "Войти", откроется модальное окно с формой авторизации, которая состоит из поля ввода "Email" и "Пароль". Для старта набора электронной почты вам потребуется дополнительно нажать на поле ввода.

### Почему это важно
1. Приложение вынуждает пользователя делать дополнительные действия, усложняя решение основной задачи, т.е ввода данных для авторизации;
2. Если пользователь не может по какой-либо причине использовать мышь, то интерфейс не доступен для него, и он не может воспользоваться продуктом.

### Как это исправить
При открытии модального окна фокус должен автоматически переносится в поле ввода "Email". Пример реализации модального окна показан в стандарте ARIA Authoring Practices Guide [1].

## Функциональность закрытия модального окна с формой авторизации не доступна с клавиатуры
### Воспроизведение ошибки
В верхней части страницы нажмите на кнопку "Войти", откроется модальное окно с формой авторизации, нажмите клавишу Esc.

### Почему это важно
1. Люди с тремором рук испытывают сложности при поподании на кнопку "Закрыть", поэтому им гораздо сложнее закрыть модальное окно и продолжить взаимодействие с интерфейсом;
2. Пользователи могут временно не использовать мышь, и поэтому интерфейс не доступен для них.

### Как это исправить
Нужно добавить функциональность закрытия модального окна. Пример рекомендуемой реализации показан в стандарте WAI-ARIA Authoring Practices 1.2 [1]

## Ресурсы
1.	Компонент Dialog в [стандарте ARIA Authoring Practices Guide](https://www.w3.org/TR/wai-aria-practices-1.2/examples/dialog-modal/dialog.html).
