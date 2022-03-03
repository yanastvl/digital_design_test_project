<h1>
    Тестовое задание для «Digital Design»
</h1>

![JavaScript](https://img.shields.io/badge/Vanilla%20JavaScript-444?logo=JavaScript&logoColor=f0f0f0)
![HTML](https://img.shields.io/badge/HTML-444?logo=HTML5&logoColor=f0f0f0)

## Задача 1

Веб страница, которая содержит введение и обзор веб-технологии.
Посмотреть по ссылке: https://yanastvl.github.io/digital_design_test_project/
Код - в данном репозитории.

## Задача 2

Функция getDayInfo(date), которая возвращает информацию о выбранной дате.

`function getDayInfo(date) {
  let formatedDateStr = date.split('.').reverse().join('-');
  let selectedDate = new Date(formatedDateStr);

  let weekOfDay = getWeekOfDay(selectedDate);
  let weekOfMonth = getWeekOfMonth(selectedDate);
  let monthName = getMonthName(selectedDate);

  return `${weekOfDay}, ${weekOfMonth} неделя ${monthName} ${selectedDate.getFullYear()} года`
}

function getWeekOfDay(date) {
  let days = ['Воскресенье', 'Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота'];
  return days[date.getDay()];
}

function getWeekOfMonth(date) {
  let firstWeekDay = new Date(date.getFullYear(), date.getMonth(), 1).getDay() - 1;
  if (firstWeekDay < 0) firstWeekDay = 6;
  let offsetDate = date.getDate() + firstWeekDay;
  return Math.ceil(offsetDate / 7);
}

function getMonthName(date) {
  let months = [
    'Января', 'Февраля', 'Марта', 'Апреля', 'Мая', 'Июня', 'Июля', 'Августа', 'Сентября', 'Октября', 'Ноября', 'Декабря'
  ];
  return months[date.getMonth()]
}`

## Другие мои проекты
 - [Museum](https://rolling-scopes-school.github.io/yanastvl-JSFE2021Q3/museum-dom/) - сайт Лувра, созданный в процессе прохождения стажировки в EPAM
 - [Portfolio](https://yanastvl.github.io/portfolio_template/) - шаблон сайта-портфолио
