# Boilerplate for Laravel PHP Framework

## Installation

Clone this repository

copy the following to config/app.php in service provider section
```php
		/*
         * Infyom Generator And Dependant Service Providers...
         */
        Barryvdh\LaravelIdeHelper\IdeHelperServiceProvider::class,
        Yajra\Datatables\DatatablesServiceProvider::class,
        Collective\Html\HtmlServiceProvider::class,
        Laracasts\Flash\FlashServiceProvider::class,
        Prettus\Repository\Providers\RepositoryServiceProvider::class,
        \InfyOm\Generator\InfyOmGeneratorServiceProvider::class,
        InfyOm\AdminLTETemplates\AdminLTETemplatesServiceProvider::class,
		\InfyOm\GeneratorBuilder\GeneratorBuilderServiceProvider::class,

        /**
         * https://github.com/edvinaskrucas/settings
         * settings provider
         */
        Krucas\Settings\Providers\SettingsServiceProvider::class,
```

copy the following to config/app.php in alias section

```php
		'Form'      => Collective\Html\FormFacade::class,
        'Html'      => Collective\Html\HtmlFacade::class,
        'Flash'     => Laracasts\Flash\Flash::class,
        
        /**
         * https://github.com/edvinaskrucas/settings
         * settings provider
         */
        'Settings' => Krucas\Settings\Facades\Settings::class
```
Or clone https://github.com/InfyOmLabs/adminlte-generator/tree/5.3


run 

```php
php artisan vendor:publish
php artisan infyom:publish
```
edit config/infyom/laravel_generator.php for template and scaffolding

```php
'templates'         => 'core-templates',
```

run 
```php
php artisan infyom.publish:layout
php artisan infyom.publish:generator-builder
php artisan infyom.publish:templates
```

## Laravel Official Documentation

Documentation for the framework can be found on the [Laravel website](http://laravel.com/docs).


## License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
