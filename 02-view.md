# View (вид)
Все `view` в Laravel 7 хранятся в папке `resources/views`. View в Laravel - это обычный HTML-файл.

Создадим свой `view` и отправим запрос через маршрут на него.

Создаём маршрут в файле `/routes/web.php`:

    Route::get('/', function () {
        return view('home');
    });

Создаём view `/resources/views/home.blade.php`, размещаем в ней обычную HTML-разметку.

## Создаём страницу
Создаём сраницу `about`:

    Route::get('/about', function () {
        return 'About Page';
    });

Обращаемся по адресу `laravel.loc/about`.

## Шаблонизатор blade

    Route::get('/', function () {
        $hello = 'Привет!';
        return view('home', compact('hello'));
    });

Выводим в представлении `home.blade.php` переменную `$hello` через фигурные скобки:

    {{ $hello }}

## Разное
- в представлениях можно использовать нативный PHP, но рекомендуется использовать директивы шаблонизатора