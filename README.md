# Laravel
Руководство по Ларавель

## Установка Laravel
Установка Laravel на OpenServer, версия 7.0

- Создаём папку `domains/laravel.loc`
- Открываем консоль в OpenServer:
    - Дополнительно
    - Консоль (вводим: composer -v)
    - Переходим в домен где нужно установить ларавель
        - cd domains/laravel.loc

Устанваливаем Laravel 7:

    composer create-project laravel/laravel . 7.*

При переходе на домен появляются папки и файлы, сделаем так чтобы открывался `public/index.php`:
- Настройки
- Домены
- Ручное + Автопоиск
- `Имя домена: laravel.loc`
- `Папка домена: \laravel.loc\public`
- Добавить, Сохранить, ОК

Другой способ переадресации на `\laravel.loc\public` является файл `.htaccess`. Создаём в корне файл `.htaccess` и запишем в нём:

    RewriteEngine On
    RewriteRule (.*) public/$1
