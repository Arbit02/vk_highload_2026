# Аналог Google Play
<img width="225" height="225" alt="image" src="https://github.com/user-attachments/assets/90604aa5-b91b-40c3-bb05-87889c395d8b" />

## Определение 
Google Play - это глобальный маркетплейс, где Google выступает посредником между разработчиками контента и пользователями Android.

## Аудитория Google Play
- MAU - 2.5 млрд.
- DAU -  675 млн.
DAU расчитывалась, как 27% пользователей(процент вычислялся на основе данных из Steam).

## MVP функционал
- Авторизация и аутентификация пользователя
- Витрина
- Страница приложения
- Поиск
- Загрузка APK-файлов
- Управление установками (Пользователь может видеть все скачанные им с сервиса приложения, отслеживать их прогресс установки/обновления)
- Комментарии к продуктам
- Рейтинг продукта на основе комментариев и оценок пользователей

## Ключевые продуктовые решения
- Поддержка возобновления загрузки при обрыве связи
- Все загружаемые файлы на сервер должны проверяться на безопасность

# Расчет нагрузки
## Продуктовые метрики
Для дальнейших расчетов мы используем данные, взятые из пункта "Аудитория Google Play", а также статистику активности пользователей из открытых источников.
| Метрика | Значение | Комментаний/Источник |
| ------------- | ------------- | ------------- |
| MAU (Monthly Active Users)  | 2.5 млрд. человек  | [2]  |
| DAU (Daily Active Users)  |675 млн. человек  | Брали такое же процентное соотношение, как в Steam |
| Количество доступных приложений | 3.5 млн| см. диаграмма №1; [4] |
| Количество разработчиков | 658 тыс. | [5] |
| Количество загрузок | 53.4 млрд | Брал половину от статистики по App Store и Google Play [6] |
|Среднее количество просмотров страниц приложений юзером | 6 | Сколько раз пользователь заходит на платорму в день [3] |
| Средний размер фото | 200 Кб | Оптимальный вес фото для приложений |
| Среднее кол-во фото | 5 | Иконка и 4 скриншота [7]; Диаграмма №2|
| Средний вес файлов | 200 мб | [8] - базовый модуль |
| Количество отзывов | 14 млн | [9] |
| Средний размер отзыва | 1Кб | 350 символов (ограничение сверху - 035КБ) + Метадданные(0.7КБ) |
<img width="2714" height="1301" alt="image" src="https://github.com/user-attachments/assets/78baff99-4a5a-43d5-aa10-175a09abd31b" />
Диаграмма №1

<img width="1053" height="1009" alt="image" src="https://github.com/user-attachments/assets/bf952139-088c-449b-a59e-258aa66286c1" />
Диаграмма №2

## Технические метрики
Расчёт объёма хранения
| Тип данных | Как считали | Общий объем |
|------------|--------------------------|-------------|
| APK-файлы приложений | 3.5 млн * 200 мб |667 ТБ |
| Метаданные приложений (иконки, скриншоты) | 4 ед. * 200 Кбайт * 3.5 млн = 2 МБ | 2.6 ТБ |
| Пользовательские отзывы | 14 млн * 1КБ | 13 ГБ |
| Итого | 669.6 ТБ |





## Источники
1. https://play.google.com/store/games?hl=ru
2. https://google.play/howplayworks/#:~:text=Global%20app%20distribution-,Connecting%20users%20and%20developers%20around%20the%20world,reach%20users%20in%20new%20ways.
3. https://app2top.ru/news/mediascope-v-kontse-2024-go-rustore-prevzoshel-google-play-po-razmeru-ezhemesyachno-aktivnoj-auditorii-v-rossii1-226859.html#:~:text=Mediascope:%20%D0%B2%20%D0%BA%D0%BE%D0%BD%D1%86%D0%B5%202024%2D%D0%B3%D0%BE,%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D0%BE%D0%B9%20%D0%B0%D1%83%D0%B4%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B8%20%D0%B2%20%D0%A0%D0%BE%D1%81%D1%81%D0%B8%D0%B8%20%7C%20App2top
4. https://topic.ru/statistics/internet/mobile-internet-and-apps/kolichestvo-dostupnykh-prilozheniy-v-magazine-google-play-pokvartalno/
5. https://42matters.com/google-play-statistics-and-trends
6. 6.https://apptractor.ru/info/analytics/v-2025-godu-kolichestvo-zagruzok-prilozheniy-snova-sokratilos-no-rashody-potrebiteley-vyrosli-pochti-do-156-mlrd.html
7. https://ru.asodesk.com/blog/visual-app-store-optimization-trends-of-2021/#:~:text=%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F%20%D1%81%D0%BA%D0%B0%D1%87%D0%B0%D1%82%D1%8C%20%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5.-,%D0%9A%D0%BE%D0%BB%D0%B8%D1%87%D0%B5%D1%81%D1%82%D0%B2%D0%BE%20%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D0%BE%D0%B2,%D0%BF%D1%80%D0%B5%D0%B4%D0%BF%D0%BE%D1%87%D0%B8%D1%82%D0%B0%D1%8E%D1%82%20%D0%BF%D1%83%D0%B1%D0%BB%D0%B8%D0%BA%D0%BE%D0%B2%D0%B0%D1%82%D1%8C%205%2D7%20%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%D0%BE%D0%B2.
8. https://support.google.com/googleplay/android-developer/answer/9859372?hl=en-GB#:~:text=Table_title:%20Google%20Play%20maximum%20size%20limits%20Table_content:,App%20download%20size%20limit:%204%20GB%20%7C
9. https://appfollow.io/blog/only-10-of-reviews-on-google-play-and-22-of-reviews-on-the-app-store-get-replies
