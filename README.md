Проект e-commerce: **(in English below)**
Продакт-менеджер Василий попросил вас проанализировать совершенные покупки и ответить на следующие вопросы:

1. Сколько у нас пользователей, которые совершили покупку только один раз? 

2. Сколько заказов в месяц в среднем не доставляется по разным причинам (вывести детализацию по причинам)? 

3. По каждому товару определить, в какой день недели товар чаще всего покупается.

4. Сколько у каждого из пользователей в среднем покупок в неделю (по месяцам)? Не стоит забывать, что внутри месяца может быть не целое количество недель. Например, в ноябре 2021 года 4,28 недели. И внутри метрики это нужно учесть. 

5. Используя pandas, проведи когортный анализ пользователей. В период с января по декабрь выяви когорту с самым высоким retention на 3й месяц. Описание подхода можно найти тут. 

6. Часто для качественного анализа аудитории использую подходы, основанные на сегментации. Используя python, построй RFM-сегментацию пользователей, чтобы качественно оценить свою аудиторию. В кластеризации можешь выбрать следующие метрики: R - время от последней покупки пользователя до текущей даты, F - суммарное количество покупок у пользователя за всё время, M - сумма покупок за всё время. Подробно опиши, как ты создавал кластеры. Для каждого RFM-сегмента построй границы метрик recency, frequency и monetary для интерпретации этих кластеров. Пример такого описания: RFM-сегмент 132 (recency=1, frequency=3, monetary=2) имеет границы метрик recency от 130 до 500 дней, frequency от 2 до 5 заказов в неделю, monetary от 1780 до 3560 рублей в неделю. Описание подхода можно найти тут. 

Для решения задачи проведи предварительное исследование данных и сформулируй, что должно считаться покупкой. Обосновать свой выбор ты можешь с помощью фактов оплат, статусов заказов и других имеющихся данных.

Файлы:

 olist_customers_datase.csv — таблица с уникальными идентификаторами пользователей
customer_id — позаказный идентификатор пользователя

customer_unique_id —  уникальный идентификатор пользователя  (аналог номера паспорта)

customer_zip_code_prefix —  почтовый индекс пользователя

customer_city —  город доставки пользователя

customer_state —  штат доставки пользователя

olist_orders_dataset.csv —  таблица заказов
order_id —  уникальный идентификатор заказа (номер чека)

customer_id —  позаказный идентификатор пользователя

order_status —  статус заказа

order_purchase_timestamp —  время создания заказа

order_approved_at —  время подтверждения оплаты заказа

order_delivered_carrier_date —  время передачи заказа в логистическую службу

order_delivered_customer_date —  время доставки заказа

order_estimated_delivery_date —  обещанная дата доставки

olist_order_items_dataset.csv —  товарные позиции, входящие в заказы
order_id —  уникальный идентификатор заказа (номер чека)

order_item_id —  идентификатор товара внутри одного заказа

product_id —  ид товара (аналог штрихкода)

seller_id — ид производителя товара

shipping_limit_date —  максимальная дата доставки продавцом для передачи заказа партнеру по логистике

price —  цена за единицу товара

freight_value —  вес товара

— Пример структуры данных можно визуализировать по order_id == 00143d0f86d6fbd9f9b38ab440ac16f5

Уникальные статусы заказов в таблице olist_orders_dataset:

created —  создан
approved —  подтверждён
invoiced —  выставлен счёт
processing —  в процессе сборки заказа
shipped —  отгружен со склада
delivered —  доставлен пользователю
unavailable —  недоступен
canceled —  отменён


________________



E-commerce project: 
Product manager Vasily asked you to analyze your purchases and answer the following questions:

1. How many users do we have who have made a purchase only once? 

2. How many orders per month on average are not delivered for various reasons (display details for reasons)? 

3. For each product, determine on which day of the week the product is most often purchased.

4. How many purchases does each user have on average per week (by month)? Do not forget that there may not be a whole number of weeks inside a month. For example, in November 2021, 4.28 weeks. And this needs to be taken into account inside the metric. 

5. Using pandas, conduct a cohort analysis of users. In the period from January to December, identify the cohort with the highest retention for the 3rd month. A description of the approach can be found here. 

6. I often use segmentation-based approaches for qualitative audience analysis. Using python, build RFM segmentation of users to qualitatively evaluate your audience. In clustering, you can choose the following metrics: R is the time from the user's last purchase to the current date, F is the total number of purchases from the user for all time, M is the amount of purchases for all time. Describe in detail how you created clusters. For each RFM segment, construct the boundaries of the recency, frequency, and monetary metrics to interpret these clusters. An example of such a description: RFM segment 132 (recency=1, frequency=3, monetary=2) has the boundaries of recency metrics from 130 to 500 days, frequency from 2 to 5 orders per week, monetary from 1780 to 3560 rubles per week. A description of the approach can be found here. 

To solve the problem, conduct a preliminary study of the data and formulate what should be considered a purchase. You can justify your choice with the help of payment facts, order statuses and other available data.

Files:

 olist_customers_datase.csv — table with unique user ids
customer_id — custom user id

customer_unique_id — unique user ID (analogous to passport number)

customer_zip_code_prefix — user's zip code

customer_city — the user's delivery city

customer_state — the user's delivery state

olist_orders_dataset.csv — order table
order_id — unique order identifier (receipt number)

customer_id — the order ID of the user

order_status — order status

order_purchase_timestamp — time of order creation

order_approved_at — time of order payment confirmation

order_delivered_carrier_date — time of order transfer to the logistics service

order_delivered_customer_date — order delivery time

order_estimated_delivery_date — promised delivery date

olist_order_items_dataset.csv — product items included in orders
order_id — unique order identifier (receipt number)

order_item_id — product identifier within a single order

product_id — product ID (barcode analog)

seller_id — id of the product manufacturer

shipping_limit_date — the maximum delivery date by the seller to transfer the order to the logistics partner

price — the price per unit of goods

freight_value — product weight

— An example of a data structure can be visualized by order_id == 00143d0f86d6fbd9f9b38ab440ac16f5

Unique order statuses in the olist_orders_dataset table:

created — created
approved — confirmed
invoiced — invoiced
processing — in the process of assembling the order
shipped — shipped from the warehouse
delivered — delivered to the user
unavailable — unavailable
canceled — canceled
