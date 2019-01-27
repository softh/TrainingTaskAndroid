# Android приложение "Курсы криптовалют"

Дополнительные требования помечены <font color="red">красным цветом</font> или символами *** (Github может не отрисовывать цветной текст)
## Описание экранов приложения
### 1. Splashscreen

Эмулирует первоначальную инициализацию приложения. Отображается на 2 секунды при запуске приложения. По прошествии 2 секунд, должен отобразиться экран `Список криптовалют`

<img src="./screens/splash.png" alt="drawing" width="300"/>

| Номер элемента| Описание           |
| ------------- |:------------------:|
| 1.1           | Логотип приложения |
| 1.2           | Версия приложения  |

### 2. Список валют

Отображает список криптовалют с краткой информацией о каждой из них. Во время загрузки данных необходимо отображать любой `Loader`, например, `ProgressWheel`. 
<font color="red">При отсутствии подключения к интернету, необходимо отображать данные из локального кэша приложения</font> ***

<img src="./screens/currencies_list.png" alt="drawing" width="300"/>

| Номер элемента| Описание           |
| ------------- |:------------------:|
| 2.1           | Список криптовалют |
| 2.2           | Элемент списка. По нажатию на элемент осуществляется переход на экран `Детали`  |
| 2.2.1         | Иконка криптовалюты  |
| 2.2.2         | Название криптовалюты  |
| 2.2.3         | Текущая стоимость одной монеты в USD  |
| 2.3           | Элемент BottomNavigation. Переход на экран списка криптовалют  |
| 2.4           | Элемент BottomNavigation. Переход на экран конвертера  |
| 2.5         | Элемент AppBar. Переход на экран фильтра  |

### 3. Детали

Отображает наиболее полную информацию о выбранной криптовалюте

<img src="./screens/details.png" alt="drawing" width="300"/>

| Номер элемента| Описание           |
| ------------- |:------------------:|
| 3.1           | Элемент AppBar. Переход на предыдущий жкран |
| 3.2           | Иконка криптовалюты  |
| 3.3 - 3.6           | Дополнительные данные о валюте  |

### 4. Конвертер валют

<img src="./screens/converter.png" alt="drawing" width="300"/>

| Номер элемента| Описание           |
| ------------- |:------------------:|
| 4.1           | Поле ввода конвертируемого значения. Формат - 2 знака после запятой |
| 4.2           | Кнопка выбора валюты источника конвертации. По нажатию отображается диалог выбора валюты  |
| 4.3           | Строка отображения курса валюты из `4.2` относительно валюты из `4.6`  |
| 4.4           | Кнопка смены направления конвертации|
| 4.5           | Отображает сконвертированное значение  |
| 4.6           | Кнопка выбора валюты назначения конвертации. По нажатию отображается диалог выбора валюты  |

### 5. Фильтр

Создает фильтр для списка валют. После применения фильтра на экране `Список валют` отображаются только выбранные криптовалюты

<img src="./screens/filter.png" alt="drawing" width="300"/>

| Номер элемента| Описание           |
| ------------- |:------------------:|
| 5.1           | Элемент AppBar. Применяет созданный фильтр на экране `Список валют` |
| 5.2           | Список элементов для создания фильтра  |
| 5.3           | Checkbox  |
| 5.4           | Аббривеатура криптовалюты  |

## Получение данных
Для получения данных о криптовалютах использовать любое общедоступное API, например, [Coinmarket](https://coinmarketcap.com/api/)

## Стек технологий
- Java/Kotlin
- RxJava 2
- Retrofit2
- Room
- <font color="red">Dagger/Koin</font>***
- <font color="red">View Binding, к примеру Butterknife </font>***

## Архитектурные требования
- В приложении должны быть использованы `Порождающие`, `Структурные` и `Поведенческие` паттерны
- Приложение должно быть адекватно разделено на слои (<font color="red">MVP***, MVVM***, Clean architecture*** </font>, etc)

## Работа с исходным кодом
- Исходный код приложения хранится в VCS Git
- Файл `.gitignore` должен быть сконфигурировал

## Сборка приложения
- Скрипт сборки `build.gradle` не должен содержать "мусор"
- <font color="red">Для сборки на локальной машине развернуть Jenkins</font>***

## Рекомендуемая к прочтению литература
- «Совершенный код» - Стив Макконнелл
- «Рефакторинг. Улучшение существующего кода» - Мартин Фаулер
- «Приёмы объектно-ориентированного проектирования. Паттерны проектирования» -  Эрих Гамма, Ричард Хелм, Ральф Джонсон, Джон Влиссидес
- «Android. Программирование для профессионалов» - Филлипс Б., Стюарт К., Марсикано К
- «Эффективное использование потоков в операционной системе Android. Технологии асинхронной обработки данных» - Андерс Ёранссон