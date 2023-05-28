# Набор данных этого продукта состоит из следующих таблиц:

**module3_analytics_events** - Журнал (лог) аналитических событий. Сюда попадают данные о посещении пользователем страниц продукта и покупках.

**module3_advertisement_budgets** - Рекламные затраты по дням и каналам привлечения.

**module3_partners** - Справочник партнёрских сетей и их ресторанов.

**module3_dishes** - Справочник блюд.

**module3_cities** - Справочник городов.

В таблицах хранятся данные о событиях в период с 30.04.2021 по 02.07.2021.


**Поля таблицы module3_analytics_events:**

visitor_uuid — идентификатор посетителя. Это идентификатор, который присваивается системой любому новому пользователю вне зависимости от того, зарегистрировался он в продукте или нет.

user_id — идентификатор зарегистрированного пользователя. Присваивается посетителю после создания учётной записи: ввода логина, пароля, адреса доставки и контактных данных.

device_type — тип платформы, с которой посетитель зашёл в продукт.

city_id — город, из которого посетитель зашёл в сервис.

age — возрастная группа пользователя (указывается при регистрации).

source — рекламный источник привлечения посетителя.

first_date — дата первого посещения продукта.

visit_id — уникальный идентификатор сессии.

event — название аналитического события.

datetime — дата и время события.

log_date — дата события.

rest_id — уникальный идентификатор ресторана (заполняется для заказов, карточек ресторанов и блюд).

object_id — уникальный идентификатор блюда (заполняется для заказов и карточек блюд).

listing_id — уникальный идентификатор блюда в листинге. Листинг — набор блюд, которые рекомендуются системой пользователю при просмотре страницы ресторана. Заполняется только для событий типа rest_page.

position — позиция блюда в листинге. Чем меньше номер, тем ближе блюдо к началу страницы. Заполняется только для событий типа rest_page.

order_id — уникальный идентификатор заказа.

revenue — выручка от заказа, в рублях. Это та сумма, которую пользователь видит при оплате.

delivery — стоимость доставки, в рублях.

commission — комиссия, которую «Всё.из.кафе» берёт с выручки ресторана, в процентах.

visit_num — порядковый номер сессии пользователя.

order_num — порядковый номер покупки, совершённой пользователем.



**В таблице также хранятся данные о нескольких типах аналитических событий:**

main_page — посещение главной страницы приложения;

authorization — ввод логина и пароля, авторизация;

rest_page — просмотр страницы ресторана;

object_page — просмотр карточки блюда;

order — оплата заказа.

reg_page — страница регистрации пользователей.

confirm_phone — страница ввода кода подтверждения регистрации.

login — страница ввода логина и пароля.

add_to_cart — страница добавления блюд в заказ.



**В таблице module3_advertisement_budgets хранятся данные о ежедневных затратах на рекламу. Поля таблицы:**

source — рекламный источник;

date — дата рекламных затрат;

budget — дневной бюджет, в рублях.



**Таблица module3_partners — справочник партнёрских сетей и их ресторанов. Поля таблицы:**

rest_id — уникальный идентификатор ресторана;

chain — название сети, к которой принадлежит ресторан;

type — тип кухни;

city_id — город, в котором находится ресторан;

commission — комиссия, которую «Всё.из.кафе» берёт с выручки ресторана, в процентах.



**Таблица module3_dishes — справочник блюд, доступных в партнёрских ресторанах. Поля таблицы:**

object_id — уникальный идентификатор блюда;

name — название блюда;

spicy — логический признак острых блюд: 1 — блюдо острое;

fish — логический признак рыбных блюд: 1 — блюдо содержит морепродукты;

meat — логический признак мясных блюд: 1 — блюдо содержит мясо;

rest_id — уникальный идентификатор ресторана, из которого можно заказать блюдо.



**Таблица module3_cities — справочник населённых пунктов, в которых можно пользоваться продуктом. Поля таблицы:**

city_id — уникальный идентификатор населённого пункта,

city_name — название населённого пункта.


**Во всех задачах считается, что изучаются данные утром 3 июля 2021 года.**