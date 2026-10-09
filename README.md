# 🚀 FastAPI URL Shortener

یک سرویس ساده و سریع برای کوتاه‌کردن لینک‌ها با استفاده از **FastAPI**،\
به‌همراه ثبت تعداد بازدید و لاگ هر بازدید (IP و زمان) با **Middleware**.

------------------------------------------------------------------------

## ✨ امکانات (Features)

-   کوتاه‌سازی URL
-   ریدایرکت به لینک اصلی
-   شمارش تعداد بازدید (visit_count)
-   ثبت آمار هر بازدید:
    -   IP کاربر
    -   زمان بازدید
-   استفاده از Middleware برای لاگ‌کردن بازدیدها
-   پیاده‌سازی با SQLAlchemy ORM

------------------------------------------------------------------------

## 🧱 تکنولوژی‌ها

-   Python 3.10+
-   FastAPI
-   SQLAlchemy
-   Alembic
-   SQLite

------------------------------------------------------------------------

## ⚙️ نصب و اجرا

### ساخت Virtual Environment

``` bash
python -m venv venv
source venv/bin/activate
```


### ریپو clone

``` bash
git clone git@github.com:KiarashAlimohamadi/url_shortener.git
```


### نصب وابستگی‌ها

``` bash
pip install -r requirements.txt
```


##ورود به project directory

``` bash
cd core
```

### اجرای Migration

``` bash
alembic upgrade head
```

### اجرای پروژه

``` bash
uvicorn main:app --reload
```

مستندات: - http://127.0.0.1:8000/docs

------------------------------------------------------------------------

## 🔗 API Endpoints

### POST /shorten

ایجاد لینک کوتاه

### GET /{short_code}

ریدایرکت به لینک اصلی

### GET /stats/{short_code}

مشاهده تعداد بازدید

------------------------------------------------------------------------

## 🧠 Middleware

Middleware به‌صورت خودکار بازدیدها را ثبت می‌کند و مقدار visit_count را
به‌صورت atomic افزایش می‌دهد.

------------------------------------------------------------------------
