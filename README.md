# goit-rdb-hw-04: DML, DDL і складні SQL-вирази на Olist

## Датасет
- **Назва:** Olist Brazilian E-commerce Public Dataset, ~100 тис. замовлень, 2016-09 … 2018-10
- **Основне джерело:** Kaggle [`olistbr/brazilian-ecommerce`](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- **Резервне джерело (ті самі файли, без Kaggle credentials):** офіційний репозиторій Olist [`olist/work-at-olist-data/datasets`](https://github.com/olist/work-at-olist-data/tree/master/datasets)

## Використані таблиці (6) і sample-розмір
Повний обсяг, без семплювання.

| CSV | raw-таблиця | typed-таблиця | рядків |
|---|---|---|---|
| olist_customers_dataset.csv | olist_customers_raw | olist_customers | 99 441 |
| olist_orders_dataset.csv | olist_orders_raw | olist_orders | 99 441 |
| olist_order_items_dataset.csv | olist_order_items_raw | olist_order_items | 112 650 |
| olist_products_dataset.csv | olist_products_raw | olist_products | 32 951 |
| olist_sellers_dataset.csv | olist_sellers_raw | olist_sellers | 3 095 |
| olist_order_reviews_dataset.csv | olist_order_reviews_raw | olist_order_reviews | 99 224 |

Службові таблиці: `seller_alerts`, `seller_score`, `olist_customer_dim`, `customer_segments`.

## Структура
```
hw4_olist.ipynb      # notebook з output клітинок
data/olist/*.csv     # 6 CSV (~58 MB, кожен файл < 100 MB)
README.md
```

## Запуск
1. Відкрити `hw4_olist.ipynb` у Google Colab.
2. **Runtime → Restart session and run all**

Примітки до середовища (враховані в першій клітинці):
- на Python 3.13+ pgserver ставиться з cp312-wheel з тегом `abi3`;
- у SQLAlchemy URI явно вказано `postgresql+psycopg2://`, бо SQLAlchemy 2.1 за замовчуванням шукає psycopg 3.
