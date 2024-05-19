<div align="center">
  <img src="https://vueschool.io/storage/media/16ce11772bf3727d68e90d9d8f41be18/laravel-backends-for-vue-js-3-not-transparent-1.jpg" width="600" height="300"/>
</div>

# 📖 About project :
This is Todo app - simple online task management application.

# :hammer_and_wrench: Languages and Tools :
<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/php/php-original.svg" title="PHP"  alt="PHP" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/laravel/laravel-original.svg" title="Laravel" alt="Laravel" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/tailwindcss/tailwindcss-original.svg" title="Tailwindcss" alt="Tailwindcss" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original-wordmark.svg" title="MySQL"  alt="MySQL" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" title="JavaScript" alt="JavaScript" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/vuejs/vuejs-original-wordmark.svg" title="Vuejs" alt="Vuejs" width="40" height="40"/>&nbsp;
</div>

# Project architecture and setup :
Project is written on laravel(back-end) and vue(front-end) in separate repositories.
## Back-end
https://github.com/g-e-g-e-r-s-o-n/agronnect_project_backend
<br>
(Written on Laravel v11.7.0 PHP v8.3.7. Both of them are latest versions.)
* #### For windows you need xampp or other webserver software. There is easy way to use xampp. Xampp doesn't support PHP 8.3.7 version. But I write it my own and supports this verion.

  - #### Step 1
    First of all install xampp latest version. Before making any changes, it's always a good idea to backup your important files and databases to avoid data loss.
    
    #### Step 2
    Make sure XAMPP is not running. You can stop the Apache and MySQL services from the XAMPP Control Panel.
    
    #### Step 3
    Go to the XAMPP installation directory and navigate to the php folder. Rename the existing php folder to something like php_backup.
    
    #### Step 4
    Visit the official PHP website (https://windows.php.net/download#php-8.3) and download the Windows version of PHP 8.3.7 (Current).
    
    Xampp using Thread Safe version so we have to download VS16 x64 Thread Safe
    This is direct link to download:
    https://windows.php.net/downloads/releases/php-8.3.7-Win32-vs16-x64.zip
    
    #### Step 5
    Then, copy the contents of the PHP 8.3.7 folder that you downloaded into the XAMPP php folder.
    
    #### Step 6
    Create new folder inside php folder and name it "windowsXamppPhp" for example you have c:\xampp\php\windowsXamppPhp path and copy again the contents of the PHP 8.3.7 into the windowsXamppPhp folder too.
    
    #### Step 7
    I also copied other folders and files from php_backup to the php folder which were now missing in the downloaded php 8.3.7, which are:
     - cfg
     - CompatInfo
     - data
     - docs
     - man
     - pear
     - scripts
     - tests
     - tmp
     - www
     - CompatInfo.php
     - webdriver-test-example.php
    
    #### Step 8
    Now we need php.ini file!
    Duplicate "php.ini-development" in php root folder and rename it "php.ini"
    
    Personally, I used the comparison tool to make the PHP configuration the same as XAMPP, so that I could compare the new php.ini file with the old one in php_backup faster and better and make sure you enabled desire php extension such as mysqli, gd, pdo_mysql, pdo_sqlite ... Also you can ```php.ini``` file which is uploaded in this repository.
    
    #### Step 9
    Now you can start the Apache and MySQL services from the XAMPP Control Panel. 
    
    Check http://localhost/dashboard/phpinfo.php

    #### step 10
    Now you can download and install composer and run laravel project.

    If mysql shutdowns unexpectedly in xampp you can use following link:
     - https://stackoverflow.com/questions/18022809/how-can-i-solve-error-mysql-shutdown-unexpectedly
    

* #### For linux just install web server, php, mariaDB, composer, then verify these installation and you can setup and run laravel project.


#### Now just download/clone back-end project and follow next steps.
* #### Create a database.
* #### Connect project to the database.
  - ```env
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=agronnect_db
    DB_USERNAME=root
    DB_PASSWORD=
    ```
* #### Configure project and install necessary packages with terminal on project root.
  - ```console
    composer install
    php artisan key:generate --ansi
    php artisan migrate
    composer require php-open-source-saver/jwt-auth
    php artisan jwt:secret
    ```
* #### Now run project back-end which provides us a Restful API service with jwt authentication. Run following command in terminal.
  - ```console
    php artisan serve
    ```

### Front-end
https://github.com/g-e-g-e-r-s-o-n/agronnect_project_frontend

