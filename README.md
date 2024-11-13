# E-commerce Project

Всем привет!
В данном проекте реализован анализ данных для e-commerce.

Проект выполнен на Python с использованием Jupyter Notebook.

## Задачи проекта

В ходе проекта необходимо решить следующие задачи:

1. Определить количество пользователей, совершивших покупку только один раз.
2. Выяснить среднее количество заказов в месяц, которые не были доставлены по разным причинам (вывести детализацию по причинам).
3. По каждому товару определить, в какой день недели он чаще всего покупается.
4. Рассчитать среднее количество покупок в неделю для каждого пользователя (по месяцам).
5. Провести когортный анализ пользователей с помощью `pandas`. В период с января по декабрь выявить когорту с самым высоким уровнем удержания на 3-й месяц.

## Описание данных

**`olist_customers_datase.csv`** — таблица с уникальными идентификаторами пользователей:

- `customer_id` — позаказный идентификатор пользователя
- `customer_unique_id` — уникальный идентификатор пользователя
- `customer_zip_code_prefix` — почтовый индекс пользователя
- `customer_city` — город доставки пользователя
- `customer_state` — штат доставки пользователя

**`olist_orders_dataset.csv`** — таблица заказов:

- `order_id` — уникальный идентификатор заказа (номер чека)
- `customer_id` — позаказный идентификатор пользователя
- `order_status` — статус заказа
  - `created` — создан
  - `approved` — подтверждён
  - `invoiced` — выставлен счёт
  - `processing` — в процессе сборки заказа
  - `shipped` — отгружен со склада
  - `delivered` — доставлен пользователю
  - `unavailable` — недоступен
  - `canceled` — отменён
- `order_purchase_timestamp` — время создания заказа
- `order_approved_at` — время подтверждения оплаты заказа
- `order_delivered_carrier_date` — время передачи заказа в логистическую службу
- `order_delivered_customer_date` — время доставки заказа
- `order_estimated_delivery_date` — обещанная дата доставки

**`olist_order_items_dataset.csv`** — товарные позиции, входящие в заказы:

- `order_id` — уникальный идентификатор заказа (номер чека)
- `order_item_id` — идентификатор товара внутри одного заказа (не содержит информацию о количестве товаров)
- `product_id` — уникальный идентификатор товара (аналог штрихкода)
- `seller_id` — уникальный идентификатор производителя товара
- `shipping_limit_date` — максимальная дата доставки продавцом для передачи заказа партнёру по логистике
- `price` — цена за единицу товара
- `freight_value` — вес товара

## Реализация проекта

- Проведён предварительный анализ и предобработка данных.
- Проанализировано поведение пользователей и выполнение доставки заказанных товаров.
- Проведён когортный анализ пользователей.

## Используемые библиотеки

- `pandas`
- `numpy`
- `calendar`
- `datetime`
- `matplotlib.pyplot`
- `seaborn`
- `operator.attrgetter`


# E-commerce Project

Hello everyone!
This project involves data analysis for e-commerce.

The project is implemented in Python using Jupyter Notebook.

## Project Objectives

The following tasks need to be accomplished in the project:

1. Determine the number of users who made a purchase only once.
2. Find the average number of undelivered orders per month, categorized by the reasons for non-delivery.
3. For each product, identify the day of the week it is most frequently purchased.
4. Calculate the average number of purchases per week for each user (by month).
5. Conduct a cohort analysis of users using `pandas`. Identify the cohort with the highest retention rate by the 3rd month from January to December.

## Data Description

**`olist_customers_dataset.csv`** — table with unique customer identifiers:

- `customer_id` — user identifier for each order
- `customer_unique_id` — unique user identifier
- `customer_zip_code_prefix` — user’s zip code
- `customer_city` — user’s delivery city
- `customer_state` — user’s delivery state

**`olist_orders_dataset.csv`** — table of orders:

- `order_id` — unique order identifier (receipt number)
- `customer_id` — user identifier for each order
- `order_status` — order status
  - `created` — created
  - `approved` — approved
  - `invoiced` — invoiced
  - `processing` — in process
  - `shipped` — shipped
  - `delivered` — delivered to the customer
  - `unavailable` — unavailable
  - `canceled` — canceled
- `order_purchase_timestamp` — order creation timestamp
- `order_approved_at` — order payment approval timestamp
- `order_delivered_carrier_date` — order handover to logistics
- `order_delivered_customer_date` — order delivery timestamp
- `order_estimated_delivery_date` — estimated delivery date

**`olist_order_items_dataset.csv`** — items within orders:

- `order_id` — unique order identifier (receipt number)
- `order_item_id` — identifier of the item within an order (does not contain quantity information)
- `product_id` — unique product identifier (similar to a barcode)
- `seller_id` — unique identifier of the product seller
- `shipping_limit_date` — latest date for the seller to hand over the order to a logistics partner
- `price` — price per item
- `freight_value` — weight of the item

## Project Implementation

- Preliminary analysis and data preprocessing were conducted.
- User behavior and order delivery performance were analyzed.
- Cohort analysis of users was performed.

## Libraries Used

- `pandas`
- `numpy`
- `calendar`
- `datetime`
- `matplotlib.pyplot`
- `seaborn`
- `operator.attrgetter`
