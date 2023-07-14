![Photo by Łukasz Nieścioruk on Unsplash](https://user-images.githubusercontent.com/2342458/202705067-769a52f1-1b44-421d-84ee-cbf8ee4cfb26.png)

# Kinsta - Hello World - Laravel
An example of how to set your Laravel application up to enable deployment on Kinsta App Hosting services.

---
Kinsta is a developer-centric cloud host / PaaS. We’re striving to make it easier for you to share your web projects with your users. Focus on coding and building, and we’ll take care of deployment and provide fast, scalable hosting. + 24/7 expert-only support.

- [Start your free trial](https://kinsta.com/signup/?product_type=app-db)
- [Application Hosting](https://kinsta.com/application-hosting)
- [Database Hosting](https://kinsta.com/database-hosting)

## Installation
Because Laravel is using both PHP and Node, you need to add buildpacks for Node.js and PHP. 

## Dependency Management
Laravel is a regular PHP-based application, so during the deployment process Kinsta will automatically install dependencies defined in your `composer.json` file.

## Environment Variables
Note that Laravel requires the `APP_KEY` environment variable to be set. If this key is not set you will see an error 500 page served by Laravel. You can generate an app key yourself locally, or you can use this [online Laravel key generator](https://generate-random.org/laravel-key-generator). Once you have a key you can add it as an environment variable in the Settings section of your app. 

## Web Server Setup
The default web process will be `heroku-php-apache2`. In this example we've created an `.htaccess` file that reroutes all requests to `public/index.php` for Laravel. If you'd like to change this command you can go to the Processes section in MyKinsta for your application. You could use:
* `heroku-php-apache2 /public`
* `php artisan serve --host 0.0.0.0 --port 8080`

## Watch How to Set Up a Laravel Application on Kinsta
[![Watch the video](https://img.youtube.com/vi/pw-AChDwH7I/maxresdefault.jpg)](https://www.youtube.com/watch?v=pw-AChDwH7I)
