# LaraOrchidTinyMCE

TinyMCE editor for Laravel Orchid. Forked from ... . I want to add disk and path setting, and set correct image ctrl+c ctrl+v pasting. 

## Install

Add this to main `composer.json`:

```json
"repositories": [
    {
        "type": "vcs",
        "url": "https://github.com/OlegAnTo2000/LaraOrchidTinyMCE"
    }
]
```

Run `composer require oleganto2000/laraorchidtinymce`.

Than add to `config/platform.php`:

```
'resource' => [
    'scripts'     => [
      // add this rows
        '/js/platform/tinymce/tinymce/tinymce.min.js',
        '/js/platform/tinymce/tinymce.js',
    ],
    'stylesheets' => [
    ],
],
```

## Updating

If you want to change something, you should start `npm run production`, and after this run:

```
php artisan vendor:publish --tag=laravel-assets --ansi --force
```


