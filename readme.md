Laravel Convert Case Middleware
===============================

> 🛠️ Fork of `tomlerendu/laravel-convert-case-middleware` with Laravel 11 support.

[![Actions Status](https://github.com/tomlerendu/laravel-convert-case-middleware/workflows/Tests/badge.svg)](https://github.com/tomlerendu/laravel-convert-case-middleware/actions)

Convert requests from camel case to snake case. Convert responses from snake case to camel case.

Why?
----

Its convention to work with camel case in Javascript and snake case in PHP.

Requirements
------------

Laravel 5.2+

Installation
------------

1. `composer require arkn/laravel-convert-case-middleware`
2. Add the middleware to the appropriate group in `App\Http\Kernel.php`. For example

```php
protected $middlewareGroups = [
    'api' => [
        'throttle:60,1',
        'bindings',
        \TomLerendu\LaravelConvertCaseMiddleware\ConvertRequestToSnakeCase::class,
        \TomLerendu\LaravelConvertCaseMiddleware\ConvertResponseToCamelCase::class,
    ],
];
```
