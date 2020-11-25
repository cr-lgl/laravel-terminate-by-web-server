# Laravel Terminate By Web Server
An example of how Laravel terminate works.

## Getting Started

```
cp .env.example .env
cp docker/.env.example docker/.env

make start
make composer
make keygen
make bash
php artisan serve --host 0.0.0.0
```

Open your browser, and enter localhost, localhost:81, localhost:82

## Result
|artisan serve|apache2 + mod_php|nginx + php-fpm|
|------|---|---|
|instantly render, but process 10 wait...|render after 10 wait|instantly render|

Look at `fastcgi_finish_request()` and `Symfony\Component\HttpFoundation\Response`
