# Filament Username Login

## Requirements

- PHP:8.2 or higher.
- Laravel: 11 or higher.
- Laravel filament: 3 or higher.

### Install

- Add in default service provider panel:
    ```php
     $panel
        ->default()
        ->id('admin')
        ->path('admin')
        ->login(\UsernameLogin\Filament\Pages\Login::class);
    ```