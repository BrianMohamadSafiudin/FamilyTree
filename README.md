## Genealogy - Open Source Family Tree Software - Laravel 10 backend
 ![Latest Stable Version](https://img.shields.io/github/release/cgdsoftware/genealogy.svg) 
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/familytree365/genealogy/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/familytree365/genealogy/?branch=master)
[![Code Intelligence Status](https://scrutinizer-ci.com/g/familytree365/genealogy/badges/code-intelligence.svg?b=master)](https://scrutinizer-ci.com/code-intelligence)
[![StyleCI](https://github.styleci.io/repos/135390590/shield?branch=master)](https://github.styleci.io/repos/135390590)
[![CodeFactor](https://www.codefactor.io/repository/github/familytree365/genealogy/badge/master)](https://www.codefactor.io/repository/github/familytree365/genealogy/overview/master)
[![codebeat badge](https://codebeat.co/badges/911f9e33-212a-4dfa-a860-751cdbbacff7)](https://codebeat.co/projects/github-com-modulargenealogy-genealogy-master)
[![CircleCI](https://circleci.com/gh/laravel-liberu/genealogy.svg?style=svg)](https://circleci.com/gh/laravel-liberu/genealogy)


## Description

Browser based Genealogy software for interacting and processing data efficiently. Easily create your
own family tree by importing your existing data or manual data entry. Storage of all data is securely on your own server and does
not leave your environment without your permission. API support for many databases of family tree records. In the future there will be optional
smart matching with other servers. This is the Laravel 9 backend using the Laravel Liberu collection of modules. Please see https://github.com/liberu-ui/genealogy for the client.

Data tables for comprehrensive amount of CRUD information. Forms easy to modify. Gedcom import and export. DNA matching. Subscriptions using Stripe and PayPal. APIs for various online databases of genealogical records.

## Demo

https://www.familytree365.com - register a free account

<!--h-->
### Official Laravel Liberu Documentation

The documentation is available [here](https://docs.laravel-enso.com) split into backend and frontend.
Note that most sections have short demo clips.

<!--/h-->

### Installation Steps

1. Download the project with `git clone https://github.com/laravel-liberu/genealogy.git`

2. Copy .env.example to .env and edit details

3. `composer install` or on Windows you need to use `composer install --ignore-platform-reqs`

4. `php artisan key:generate`

5. `php artisan serve` 
In order to serve the back-end API, take a look at the Local Development Server section of the [Laravel installation documentation](https://laravel.com/docs/6.x/#installation)
and consider using [Valet](https://laravel.com/docs/6.x/valet) for a better experience

6. Run `php artisan migrate --seed`

7. Follow installation steps for client side (https://github.com/cgd-ui/genealogy) and launch the site and log into the project with user: `admin@familytree365.com`, password: `password`

8. (optional) Setup the configuration files as needed, in `config/enso/*.php`

9. (maybe required) Setup sanctum stateful domains in `.env` and add your domains to `config/cors.php`


## Import test data

1. Make sure php artisan queue:work is running

2. Make sure root database user is being used.

3. Register a new user and login.

4. Go to gedcom / import and upload https://github.com/cgdsoftware/public-gedcoms/blob/master/files/royal92.ged


## Broadcasting Setup

```bash
# install dependencies
$ npm install -g laravel-echo-server

$ laravel-echo-server configure
$ nano .env

  BROADCAST_DRIVER=redis
  REDIS_PREFIX=

$ laravel-echo-server start
```

If you want to keep it in background proccess you should install pm2 or supervisor

## Sphinx Search Engine Setup

In this project, sphinx search engine is used to improve search result. If you want to see how to setup sphinx engine, how to use in your Laravel app, please follow this medium blog.

https://medium.com/@devknight216/how-to-setup-sphinx-search-engine-with-your-laravel-app-7ace9189762b

## DNA Matching setup

We currently use Lineage, install Python 3 and Pip and run `pip3 install lineage`

### Support services (new)
While developing genealogy, we constantly received private inquiries from devs and teams asking us about paid support. Some of these requests even lead to fruitful collaborations, so we finally decided to launch such an option.

If you're looking for premium support when building applications with genealogy we can help you with that. Our support packages start at £250 / month with 8 hours included. With premium support you will get:

a private repo on our self hosted gitlab instance where you can host your project

priority in addressing your issues

help with understanding the environment

getting you to be proficient when developing on Liberu

mentoring

code reviews

general advice & support on Laravel & Vue

assistance on version upgrades

up to 4 hours / month of remote desktop sessions and call conferences with your team

direct communication via Slack during our office hours

The support services are provided by a team of 4 members.

### Thanks

Built with Laravel Liberu 5.x which is crafted on Laravel 10.

Special thanks to [Taylor Otwell](https://laravel.com/), [Jeffrey Way](https://laracasts.com), [Evan You](https://vuejs.org/) and [Jeremy Thomas](https://bulma.io). [Laravel Liberu](https://github.com/laravel-enso)

<!--h-->
### Contributions

are welcome. Pull requests are great, but issues are good too.

### License

This package is released under the MIT license.
<!--/h-->
