# Filament Laravel con Login por Username

Este repositorio explica cómo configurar Filament en Laravel para permitir el inicio de sesión utilizando un **username** en lugar de un correo electrónico.

## Uso

En el controlador de Filament (`AdminPanelProvider` o el que necesites), coloca la clase `Login` dentro de la función `login()`.

### Ejemplo:
```php
return $panel
    ->default()
    ->id('admin')
    ->path('admin')
    ->login(Login::class);
```