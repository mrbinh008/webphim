# Server Requirements:
- Laravel Framework 8.
- PHP 7.3 or higher.
    + Configure `php.ini`:

    ```
    max_input_vars=100000
    ```
- MySQL 5.7 or higher.

# Installation:
1. CD to project root and run: `composer install`
2. Configuration your database connection information in file `.env`
3. Then, run command: `php artisan ophim:install`
4. Create new user by command: `php artisan ophim:user`
5. Run `php artisan optimize:clear`

# Update:
1. CD to project root and run: `composer update hacoidev/ophim-core -W`
2. Then, run command: `php artisan ophim:install`
3. Run `php artisan optimize:clear`
4. Clear PHP Opcache in server (if enabled)

# Note
- Command CMS
    + `php artisan ophim:menu:generate` : Generate menu
    + `php artisan ophim:episode:change_domain` : Change episode domain play stream

# Command:
- Generate menu categories & regions: `php artisan ophim:menu:generate`

# Reset view counter:
- Setup crontab, add this entry:
```
* * * * * cd /path/to/project && php artisan schedule:run >> /dev/null 2>&1
```
