# SparkPractice

## Описание
ETL пайплайн для обработки данных электросетей Нидерландов.

## Архитектура
Bronze (MinIO) → Silver (MinIO) → Gold (MinIO) → ClickHouse

## Стек
- Apache Spark 4.1.1
- MinIO (S3)
- ClickHouse
- Apache Airflow
- Docker

## Что реализовано
- Загрузка CSV из S3
- Silver слой: очистка и типизация данных
- Gold слой: витрины по городам и типам подключений
- Запись витрин в ClickHouse

## Как запустить
docker-compose up -d
```

Также добавь в `.gitignore` чтобы не закоммитить секреты:
```
.env
*.jar
s3_storage/
clickhouse/
logs/
