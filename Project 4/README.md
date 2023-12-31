## Описание проекта
Компания «Чётенькое такси» собрала исторические данные о заказах такси в аэропортах. Чтобы привлекать больше водителей в период пиковой нагрузки, нужно спрогнозировать количество заказов такси на следующий час. 

## Задача проекта
Постройте модель для такого предсказания.
Значение метрики RMSE на тестовой выборке должно быть не больше 48.

## Описание данных
Данные лежат в файле `taxi.csv`. 
Количество заказов находится в столбце 'num_orders'.

## Общий вывод
В данном проекте было обучено 5 моделей, качество моделей измерялось метрикой RMSE. 

Наименьшее значение RMSE на кросс-валидации показала модель CatBoost с гиперпараметрами: learning_rate=0.25, iterations=250, depth=3; лучшая модель была проверена на тестовой выборке и показала значение RMSE в размере 42,623. В сравнении с константной моделью выбранная модель показывает существенно более хороший результат (RMSE константной модели = 58,882).
