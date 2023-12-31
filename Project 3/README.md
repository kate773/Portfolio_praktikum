## Описание проекта
Из «X-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.
Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Вам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком. 

## Задача проекта
Построить модель с предельно большим значением F1-меры. Минимально допустимое значение метрики -  0.59.

## Описание данных
Признаки
- Признаки
- RowNumber — индекс строки в данных
- CustomerId — уникальный идентификатор клиента
- Surname — фамилия
- CreditScore — кредитный рейтинг
- Geography — страна проживания
- Gender — пол
- Age — возраст
- Tenure — сколько лет человек является клиентом банка
- Balance — баланс на счёте
- NumOfProducts — количество продуктов банка, используемых клиентом
- HasCrCard — наличие кредитной карты
- IsActiveMember — активность клиента
- EstimatedSalary — предполагаемая зарплата

Целевой признак
- Exited — факт ухода клиента

## Общий вывод
В данном проекте были исследованы 3 модели: дерево решений, случайный лес и логистическая регрессия. Наибольшее значение F1-меры показала модель случайного леса после устранения дисбаланса методом увеличения выборки класса "1" с гиперпараметрами: количество деревьев - 70, максимальная глубина деревьев: 18.

Лучшая модель была проверена на тестовой выборке и показала значение F1-меры в размере 0,62, AUC-ROC в размере 0,85. Отдельно была рассчитана полнота (recall), ее значение составило 0,56. Это говорит о том, что модель правильно определяет 56% среди тех клиентов, которые действительно уйдут/планируют уйти.
