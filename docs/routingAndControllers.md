#### <sup> 📕 [Web dev course using Laravel](../README.md) → Basic Routing and controllers.</sup>

---

# **Basic Routing**
The most basic Laravel routes accept a URI and a Closure (anonymous function), providing a very simple and expressive method of defining routes:

`Route::get('/', function () {
    return 'Hello World';
});`

# **The Default Route Files**
All Laravel routes are defined in route files, which are located in the routes directory. These files are automatically loaded by the framework. The [routes/web.php](../src/routes/web.php) file defines routes that are for your web interface. These routes are assigned the web middleware group, which provides features like session state and CSRF protection. The routes in [routes/api.php](../src/routes/api.php) are stateless and are assigned the api middleware group.

For most applications, you will begin by defining routes in your [routes/web.php](../src/routes/web.php) file. The routes defined in [routes/web.php](../src/routes/web.php) may be accessed by entering the defined route's URL in your browser. For example, you may access the following route by navigating to http://your-app.test/user in your browser:

`Route::get('/user', 'UserController@index');`

# **Available Router Methods**
The router allows you to register routes that respond to any HTTP verb:

`Route::get($uri, $callback);`

`Route::post($uri, $callback);`

`Route::put($uri, $callback);`

`Route::patch($uri, $callback);`

`Route::delete($uri, $callback);`

`Route::options($uri, $callback);`

If you need to register a route that responds to multiple HTTP verbs. You may do so using the `match` method. Or, you may even register a route that responds to all HTTP verbs using the `any` method:

`Route::match(['get', 'post'], '/', function () {
    //
});`

`Route::any('/', function () {
    //
});`
# **Basic Controllers**

## Defining Controllers
You can create controllers using `php artisan make:controller ControllerName` command.