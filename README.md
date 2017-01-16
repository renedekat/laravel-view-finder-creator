# Laravel View Finder that creates missing view files


By default Laravel throws an error when a view file cannot be found. This package replaces the default view finder,
and creates your missing view files on the fly, based on a template.

The default template can be found in resources/assets/pages/missing.blade.php after you've published it.


## Installation

Via Composer

``` bash
$ composer require renedekat/laravel-view-finder-creater --sort-packages
```

Replace the default ViewServiceProvider 

```php
// config/app.php
'providers' => [
	...
	//Illuminate\View\ViewServiceProvider::class,
	ReneDeKat\LaravelViewFileFinder\ViewServiceProvider::class,
];
```

The missing page template file must be published with this command:

```bash
php artisan vendor:publish --provider="ReneDeKat\LaravelViewFileFinder\ViewServiceProvider" --tag="assets"
```

It will be published in `resources/assets/pages/missing.blade.php`


## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Testing

``` bash
$ composer test
```

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) and [CONDUCT](CONDUCT.md) for details.

## Security

If you discover any security related issues, please email renedekat@9lives-development.com instead of using the issue tracker.

## Credits

- [René de Kat][https://github.com/renedekat]

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.