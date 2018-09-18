# docker-cakephp3-template

By using Docker-Compose, you can build CakePHP3 environment easily.

# Environment

* Docker 18.06.1-ce
* Docker Compose 1.22.0
* Docker Machine 0.15.0

## Initialization (Build CakePHP3 Project)
Since CakePHP3 has an execution environment for each project, so create a project. To create another project, follow the same procedure.

### Create Docker Images
It will take about two or three minutes.

```
$ docker-compose build
```

### Run Containers 

```
$ docker-compose up -d
```

### Enter PHP-FPM Container

```
$ docker exec -it docker-cakephp3-template_phpfpm_1 /bin/sh
```


### Get Composer Installer

```
/var/www/html # curl -s https://getcomposer.org/installer | php
```

### Make Project
Here, create a `sample` project

```
/var/www/html # php composer.phar create-project --prefer-dist cakephp/app sample
Do not run Composer as root/super user! See https://getcomposer.org/root for details
Installing cakephp/app (3.6.5)
  - Installing cakephp/app (3.6.5): Downloading (100%)
Created project in sample
Loading composer repositories with package information
Updating dependencies (including require-dev)
Package operations: 47 installs, 0 updates, 0 removals
  - Installing cakephp/plugin-installer (1.1.0): Downloading (100%)
  - Installing psr/http-message (1.0.1): Downloading (100%)
  - Installing zendframework/zend-diactoros (1.8.6): Downloading (100%)
  - Installing psr/log (1.0.2): Downloading (100%)
  - Installing aura/intl (3.0.0): Downloading (100%)
  - Installing cakephp/chronos (1.2.2): Downloading (100%)
  - Installing cakephp/cakephp (3.6.11): Downloading (100%)
  - Installing symfony/polyfill-ctype (v1.9.0): Downloading (100%)
  - Installing symfony/yaml (v4.1.4): Downloading (100%)
  - Installing symfony/polyfill-mbstring (v1.9.0): Downloading (100%)
  - Installing symfony/console (v4.1.4): Downloading (100%)
  - Installing symfony/filesystem (v4.1.4): Downloading (100%)
  - Installing symfony/config (v4.1.4): Downloading (100%)
  - Installing robmorgan/phinx (0.10.6): Downloading (100%)
  - Installing cakephp/migrations (2.0.0): Downloading (100%)
  - Installing m1/env (2.1.2): Downloading (100%)
  - Installing josegonzalez/dotenv (3.2.0): Downloading (100%)
  - Installing mobiledetect/mobiledetectlib (2.8.33): Downloading (100%)
  - Installing twig/twig (v1.35.4): Downloading (100%)
  - Installing umpirsky/twig-php-function (v0.1): Downloading (100%)
  - Installing jasny/twig-extensions (v1.2.0): Downloading (100%)
  - Installing asm89/twig-cache-extension (1.3.2): Downloading (100%)
  - Installing aptoma/twig-markdown (2.0.0): Downloading (100%)
  - Installing ajgl/breakpoint-twig-extension (0.3.1): Downloading (100%)
  - Installing wyrihaximus/twig-view (4.3.5): Downloading (100%)
  - Installing cakephp/bake (1.8.4): Downloading (100%)
  - Installing squizlabs/php_codesniffer (3.3.1): Downloading (100%)
  - Installing cakephp/cakephp-codesniffer (3.0.5): Downloading (100%)
  - Installing jdorn/sql-formatter (v1.2.17): Downloading (100%)
  - Installing symfony/process (v4.1.4): Downloading (100%)
  - Installing symfony/finder (v4.1.4): Downloading (100%)
  - Installing seld/phar-utils (1.0.1): Downloading (100%)
  - Installing seld/jsonlint (1.7.1): Downloading (100%)
  - Installing justinrainbow/json-schema (5.2.7): Downloading (100%)
  - Installing composer/xdebug-handler (1.3.0): Downloading (100%)
  - Installing composer/spdx-licenses (1.4.0): Downloading (100%)
  - Installing composer/semver (1.4.2): Downloading (100%)
  - Installing composer/ca-bundle (1.1.2): Downloading (100%)
  - Installing composer/composer (1.7.2): Downloading (100%)
  - Installing cakephp/debug_kit (3.16.4): Downloading (100%)
  - Installing symfony/polyfill-php72 (v1.9.0): Downloading (100%)
  - Installing symfony/var-dumper (v4.1.4): Downloading (100%)
  - Installing nikic/php-parser (v4.0.3): Downloading (100%)
  - Installing jakub-onderka/php-console-color (0.1): Downloading (100%)
  - Installing jakub-onderka/php-console-highlighter (v0.3.2): Downloading (100%)
  - Installing dnoegel/php-xdg-base-dir (0.1): Downloading (100%)
  - Installing psy/psysh (v0.9.8): Downloading (100%)
cakephp/app suggests installing markstory/asset_compress (An asset compression plugin which provides file concatenation and a flexible filter system for preprocessing and minification.)
cakephp/app suggests installing dereuromark/cakephp-ide-helper (After baking your code, this keeps your annotations in sync with the code evolving from there on for maximum IDE and PHPStan compatibility.)
cakephp/app suggests installing phpunit/phpunit (Allows automated tests to be run without system-wide install.)
cakephp/cakephp suggests installing lib-ICU (The intl PHP library, to use Text::transliterate() or Text::slug())
symfony/console suggests installing psr/log-implementation (For using the console logger)
symfony/console suggests installing symfony/event-dispatcher
symfony/console suggests installing symfony/lock
m1/env suggests installing m1/vars (For loading of configs)
asm89/twig-cache-extension suggests installing psr/cache-implementation (To make use of PSR-6 cache implementation via PsrCacheAdapter.)
aptoma/twig-markdown suggests installing michelf/php-markdown (Original Markdown engine with MarkdownExtra.)
aptoma/twig-markdown suggests installing knplabs/github-api (Needed for using GitHub's Markdown engine provided through their API.)
ajgl/breakpoint-twig-extension suggests installing ext-xdebug (The Xdebug extension is required for the breakpoint to work)
ajgl/breakpoint-twig-extension suggests installing symfony/framework-bundle (The framework bundle to integrate the extension into Symfony)
ajgl/breakpoint-twig-extension suggests installing symfony/twig-bundle (The twig bundle to integrate the extension into Symfony)
composer/composer suggests installing ext-zip (Enabling the zip extension allows you to unzip archives)
psy/psysh suggests installing ext-pcntl (Enabling the PCNTL extension makes PsySH a lot happier :))
psy/psysh suggests installing ext-pdo-sqlite (The doc command requires SQLite to work.)
psy/psysh suggests installing hoa/console (A pure PHP readline implementation. You'll want this if your PHP install doesn't already support readline or libedit.)
Writing lock file
Generating autoload files
> Cake\Composer\Installer\PluginInstaller::postAutoloadDump
> App\Console\Installer::postInstall
Created `config/app.php` file
Created `/var/www/html/sample/tmp/cache/views` directory
Set Folder Permissions ? (Default to Y) [Y,n]? Y # ここではYを選択してください。
Permissions set on /var/www/html/sample/tmp/cache/views
Updated Security.salt value in config/app.php
```

### Exit Container

```
/var/www/html # exit
```

### Fix Configuration
Update `data/htdocs/sample/config/app.php` at line 251

```data/htdocs/sample/config/app.php
-   'host' => 'localhost',
+   'host' => 'mysql',
```

## Build Up

```
$ docker-compose up -d
```

You can check at http://localhost:8765

<img width="1602" alt="スクリーンショット 2018-09-18 3.26.26.png" src="https://qiita-image-store.s3.amazonaws.com/0/291512/b748a76d-e2fa-e56b-0cf1-f938b6194a30.png">

## Remove Containers

```
$ docker-compose down 
```


