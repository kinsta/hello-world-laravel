# Kinsta - Hello World - Laravel
An example of how to set your Laravel application up to enable deployment on Kinsta App Hosting services.

> Kinsta’s Application Hosting is a service to run your web apps and any databases side by side in a hassle-free environment, tailored for developer needs and ease of use. App Hosting is currently in an invite-only beta phase, sign up for a test account at [kinsta.com/application-hosting](https://kinsta.com/application-hosting/).

## Installation
Because Laravel is using both PHP and Node, you need to add buildpacks for Node.js and PHP. 

## Dependency Management
Laravel is a regular PHP-based application, so during the deployment process Kinsta will automatically install dependencies defined in your `composer.json` file.

## Environment Variables
Note that Laravel requires the `APP_KEY` environment variable to be set. If this key is not set you will se an error 500 page served by Laravel. You can generate an app key yourself locally, or you can use this [online Laravel key generator](https://generate-random.org/laravel-key-generator). Once you have a key you can add it as an environment variable in the Settings section of your app. 

## Web Server Setup
The default web process will be `heroku-php-apache2`. In this example we've created an `.htaccess` file that reroutes all requests to `public/index.php` for Laravel. If you'd like to change this command you can go to the Processes section in MyKinsta for your application. You could use:
* `heroku-php-apache2 /public`
* `php artisan serve --host 0.0.0.0 --port 8080`


