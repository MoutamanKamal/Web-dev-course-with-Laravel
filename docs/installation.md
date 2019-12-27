#### <sup> 📕 [Web dev course using Laravel](../README.md) →installation and Environment Setup</sup>

---

# **[Composer](https://getcomposer.org/)**
[Composer](https://getcomposer.org/) is a tool for dependency management in PHP. It allows you to declare the libraries your project depends on and it will manage (install/update) them for you.

Laravel can be installed using two methods, both utilize [composer](https://getcomposer.org/), so before starting make sure you have composer installed.
## What is composer?

# **Installing Laravel**
- ## **Using Laravel Installer**
    - First, download the Laravel installer using Composer:  
   
        `composer global require laravel/installer`

        After installation, the `laravel new` command will create a fresh Laravel installation in the directory you specify. For instance, laravel new blog will create a directory named blog containing a fresh Laravel installation with all of Laravel's dependencies already installed:

        `laravel new blog`

- ## **Using Laravel Composer Create-Project**
    - The second method to install Laravel, is by using the Composer `create-project` command in your terminal:

        `composer create-project --prefer-dist laravel/laravel blog`

# **Application Key**

The next thing you should do after installing Laravel is set your application key to a random string. If you installed Laravel via Composer or the Laravel installer, this key has already been set for you by the `php artisan key:generate` command, if not just run the previous command.

# **Running a Local Development Server**
- Using PHP built in development server:

    `PHP -S localhost:8000`
- Using Laravel's Artisan:

    `PHP artisan serve`
    
    Both will start a development server at http://localhost:8000:
