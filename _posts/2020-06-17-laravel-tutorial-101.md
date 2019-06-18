---
layout: single
title:  "Laravel tutorial 101"
date:   2019-06-17 19:09:12 +0700
excerpt: "Laravel tutorial 101"
categories:
    - Laravel
tags :
    - web developer

gallery:
  - url: https://upload.wikimedia.org/wikipedia/commons/9/9a/Laravel.svg
    image_path: https://upload.wikimedia.org/wikipedia/commons/9/9a/Laravel.svg
    alt: "Laravel Logo SVG"
    title: "Laravel Logo SVG"
  - url: https://upload.wikimedia.org/wikipedia/commons/9/9a/Laravel.svg
    image_path: https://upload.wikimedia.org/wikipedia/commons/9/9a/Laravel.svg
    alt: "Laravel Logo SVG"
    title: "Laravel Logo SVG"
  - url: https://upload.wikimedia.org/wikipedia/commons/9/9a/Laravel.svg
    image_path: https://upload.wikimedia.org/wikipedia/commons/9/9a/Laravel.svg
    alt: "Laravel Logo SVG"
    title: "Laravel Logo SVG"
---

{% include gallery caption="Laravel **Pack**." %}

Hi semuanya kali ini saya sharing step belajar laravel dari installation - ~

# Table of Contents
- [Installation](#installation)
- [Env](#env)
- [Database Migration](#Migration)
- [Model](#model)
- [View](#view)
- [Controller](#controller)
- [ORM](#orm)
- [Deploy Laravel to Heroku](#heroku)
- [Excerpt](#excerpt)
- [Pagination](#pagination)
- [Image For Testing](#image)

## Installation
``laravel new YourAppName``

## CLI
``php artisan serve``

## Env
## Database 
### Migration
1. ``php artisan make:model ModelName -m``
1. ``php artisan migrate``
1. ``use Illuminate\Support\Facades\Schema;``
1. ``Schema::defaultStringLength(191);``

## Seeding
1. ``php artisan make:factory ModelNameFactory --model=ModelName``
1. ``php artisan make:seeder ModelNamesTableSeeder``
1. Call factory in [DatabaseSeeder](database\seeds\DatabaseSeeder.php)
``$this->call(ModelNamesTableSeeder::class);``
1. ``factory(ModelName::class, 5)->create();``
1. ``php artisan db:seed``

## Blade Template
## Route
## Model
``php artisan make:model ModelName -m``

## View
## Controller
## Auth
## Eloquent ORM  

## Heroku
1. ``echo web: vendor/bin/heroku-php-apache2 public/ > Procfile``
1. ``heroku create``
1. ``heroku addons:create cleardb:ignite``
1. ``heroku config:get CLEARDB_DATABASE_URL``

## Excerpt
``str_limit($value, $limit = 100, $end = '...')``

## Pagination
``$modelnames = ModelName::paginate(9);``

# Image
![Image for testing](https://picsum.photos/300/200 "Test")
