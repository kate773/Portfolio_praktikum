## Описание проекта
Чтобы оптимизировать производственные расходы, металлургический комбинат ООО «Так закаляем сталь» решил уменьшить потребление электроэнергии на этапе обработки стали. Вам предстоит построить модель, которая предскажет температуру стали.

## Цель и задачи проекта
**Цель проекта** - обучить модель, которая предскажет температуру стали после добавления всех легирующих добавок, что позволит бизнесу снизить затраты на электричество и обслуживание/ремонт оборудования.

**Задачи проекта:**
- выгрузить и изучить данные;
- провести предобработку данных (работа с аномалиями, пропусками, дубликатами);
- провести исследовательский анализ данных;
- подготовить итоговую таблицу со всеми необходимыми признаками;
- разделить данные на целевой и остальные признаки, в случае необходимости произвести масштабирование признаков;
- отделить тестовую выборку;
- обучить несколько моделей на тренировочной выборке и выбрать лучшую по целевой метрике;
- проверить лучшую модель на тестовой выборке;
- сравнить результаты модели с константной моделью;
- обобщить выводы, подготовить отчет для заказчика.

## Описание данных
Данные состоят из файлов, полученных из разных источников:
- `data_arc_new.csv` — данные об электродах;
- `data_bulk_new.csv` — данные о подаче сыпучих материалов (объём);
- `data_bulk_time_new.csv` — данные о подаче сыпучих материалов (время);
- `data_gas_new.csv` — данные о продувке сплава газом;
- `data_temp_new.csv` — результаты измерения температуры;
- `data_wire_new.csv` — данные о проволочных материалах (объём);
- `data_wire_time_new.csv` — данные о проволочных материалах (время).

Во всех файлах столбец `key` содержит номер партии. В файлах может быть несколько строк с одинаковым значением `key`: они соответствуют разным итерациям обработки.

## Общий вывод
В данном проекте было обучено 4 модели, качество моделей измерялось метрикой MAE, целевое значение - меньше 6,8. Наименьшее значение MAE показала модель LGBMRegressor с гиперпараметрами 'learning_rate': 0.1, 'max_depth': 5, 'num_leaves': 10, лучшая модель была проверена на тестовой выборке и показала значение MAE в размере 6,694. В сравнении с константной моделью выбранная модель показала существенно более хороший результат.
