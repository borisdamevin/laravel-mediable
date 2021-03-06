Installation
============================================

Add the package to your Laravel app using composer

::

    $ composer require plank/laravel-mediable


Register the package's servive provider in `config/app.php`

::

    'providers' => [
        //...
        'Plank\Mediable\MediableServiceProvider',
        //...
    ];

The package comes with a Facade for the image uploader, which you can optionally register as well.

::

    'aliases' => [
        //...
        'MediaUploader' => 'Plank\Mediable\MediaUploaderFacade',
        //...
    ]


Publish the config file (``config/mediable.php``) and migration file (``database/migrations/####_##_##_######_create_mediable_tables.php``) of the package using artisan.

::

    $ php artisan vendor:publish --provider="Plank\Mediable\MediableServiceProvider"

Run the migrations to add the required tables to your database.

::

    $ php artisan migrate
