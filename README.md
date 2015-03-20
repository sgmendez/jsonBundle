JsonBundle
===============

Library [Json](http://sgmendez.github.io/json/) integration Symfony2 bundle.

## Instalación

You can use [Composer](https://getcomposer.org) to use this library in 
your application.

If you don't have Composer yet, download it following the instructions on
http://getcomposer.org/ or just run the following command:

```
curl -s http://getcomposer.org/installer | php
```
And then execute this command to add libary to your project:

```
$ composer require sgmendez/jsonBundle
```
Or require [`sgmendez/json`](http://sgmendez.github.io/json/)
into your `composer.json` file:


``` 
json
{
    "require": {
        "sgmendez/jsonBundle": "*"
    }
}
```

Registrar el bundle en el Kernel:

```php
<?php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Sgmendez\Bundle\JsonBundle\JsonBundle(),
        // ...
    );
}
```
