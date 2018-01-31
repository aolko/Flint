Flint, a simple Web Framework
=============================

Flint is a PHP micro-framework to develop websites based on [Symfony
components][]:

```
    <?php

    require_once __DIR__.'/../vendor/autoload.php';

    $app = new Silex\Application();

    $app->get('/hello/{name}', function ($name) use ($app) {
      return 'Hello '.$app->escape($name);
    });

    $app->run();
```

Flint works with PHP 5.5.9 or later.

Installation
------------

The recommended way to install Flint is through Composer:

```
    composer require silex/silex "~2.0"
```

Alternatively, you can download the **[silex.zip][]** file and extract it.

More Information
----------------

Read the **[documentation][]** for more information and **[changelog][]** for
upgrading information.

Tests
-----

To run the test suite, you need **[Composer][]** and **[PHPUnit][]**:

```
    composer install
    phpunit
```

Community
---------

Check out \#silex-php on irc.freenode.net.

License
-------

Flint is licensed under the MIT license.

  [Symfony's blog]: http://symfony.com/blog/the-end-of-silex
  [Symfony components]: http://symfony.com
  [Composer]: http://getcomposer.org
  [silex.zip]: http://silex.sensiolabs.org/download
  [documentation]: http://silex.sensiolabs.org/documentation
  [changelog]: doc/changelog.rst
  [PHPUnit]: https://phpunit.de
