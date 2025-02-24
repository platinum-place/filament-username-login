# Filament Username Login

## Requirements

- PHP:8.2 or higher.
- Laravel: 11 or higher.
- Laravel filament: 3 or higher.

### Install

Here's the text for your .md:

---  

To use `username` for authentication, add the field to the `users` table via a migration:

```php
php artisan make:migration add_username_to_users_table --table=users
```  

Then, update the generated migration file:

```php
    public function up(): void
    {
        Schema::table('users', function (Blueprint $table) {
            $table->string('username')->unique()->nullable();
        });
    }


    public function down(): void
    {
        Schema::table('users', function (Blueprint $table) {
            $table->dropColumn('username');
        });
    }
```  

Run the migration:

```php
php artisan migrate
```  

This ensures the `username` field is available for authentication.

Finally, Add in default service provider panel:

```php
$panel
    ->default()
     ->id('admin')
     ->path('admin')
     ->login(\UsernameLogin\Filament\Pages\Login::class);
```