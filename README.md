# Building-Apps-on-Herpku
Heroku Tutorial Building a app

# Step #:1 login on Terminal
$   heroku login

# Step #:2 Creating Heroku application
$   heroku create

# Step#:3 Allow Heroku application to run nodejs and php OR if Other than Relevants command
$ heroku config: add \
> BUILDPACK_URL = https: //github.com/heroku/heroku-buildpack-multi.git
# Step#:4 Create the .buildpacks file at the root of the laravel project with the following content
    https://github.com/heroku/heroku-buildpack-nodejs
    https://github.com/heroku/heroku-buildpack-php

# Step#:5 Create Procfile at the root of the laravel project with the following content
    web: vendor / bin / heroku-php-apache2 public /

# Step#:6 Pushing to Heroku
$   git push heroku master

# Step#7 Adding a database to the Heroku application
$ heroku addons: create heroku-postgresql: hobby-dev --------instead any name of Ur DB Name

# Step#:8 Run laravel commands on Heroku
$   heroku run php artisan migrate
$   heroku run php artisan db: seed

NOTE: If you have cloned a laravel project to work and this project is on Heroku, don't forget to add the remote Heroku repository to your laravel application.

# Step#:9 To do this, use the command below.
$   git remote add heroku https://git.heroku.com/{project-name}.git
