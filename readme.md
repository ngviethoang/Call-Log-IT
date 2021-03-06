# Call Log IT

> Tool giao việc cho bộ phận IT tích hợp trên hệ thống Intranet

> Cán bộ trong công ty có thể gửi yêu cầu xử lý sự cố máy tính lên bộ phận IT để được hỗ trợ. Đội trưởng đội IT có thể giao việc các các chuyên viên IT và theo dõi tiến độ thực hiện.

## Technology & Library

    Laravel 5
    MySQL
    JQuery
    Bootstrap
    Metronic Theme By Keenthemes

## Deployment

    Create file .env, copy from .env.example
    Config file .env: change DB_USERNAME, DB_PASSWORD, MAIL account

#### Download packages
    $ composer install
    $ composer update
    $ npm install

#### Migrate db
    Create database call_log_it, fake data by running:
    $ php artisan migrate --seed
    $ php artisan key:generate

#### After editing config folder or .env file, clear cache to apply changes:
    $ composer dump-autoload
    $ php artisan cache:clear
    $ php artisan config:cache
    
#### Run app
    $ php artisan serve
    
## Development

#### Fake users for testing: 
    7 first employees
    Password: test
    
#### Email for testing
    Log In https://mailtrap.io with your email
    Open Demo inbox in mailtrap.io
    In Credentials tab, copy your username and password 
    Paste to MAIL_USERNAME and MAIL_PASSWORD in .env file
    Clear cache to apply changes
    Send emails in background by running: 
    $ php artisan queue:work
    
#### Debug, print log
    $ tail -f storage/logs/laravel.log
    
#### PhpStorm plugin instructions
    Settings > Plugins > Browse repositories... > Find 'Laravel plugin' > Set up
    Settings > Languages and Frameworks > Php > Laravel > Turn on 'Enable plugin for this project'
