# nocache
No Cache Header Middleware for Laravel 5

You can use it for nocache requirement for laravel routes or controllers.

First, open your app/http/kernel.php and add 'nocache' => \Laraturka\Nocache\NoCacheMiddleware::class

And then use it your route.php (or route/web.php)


Route::group(['prefix'=>'admin', 'middleware' => ['nocache']], function() {
  //your code
}

Or use with multiple middleware

Route::group(['prefix'=>'admin', 'middleware' => ['auth','acl','nocache']], function() {
  //your code
}

