JsonBundle
===============

[![License](https://poser.pugx.org/sgmendez/jsonbundle/license.svg)](https://packagist.org/packages/sgmendez/jsonbundle)
[![SensioLabsInsight](https://insight.sensiolabs.com/projects/ed6e208f-d0ad-4798-bc8c-d50814977ed5/mini.png)](https://insight.sensiolabs.com/projects/ed6e208f-d0ad-4798-bc8c-d50814977ed5)
[![Latest Stable Version](https://poser.pugx.org/sgmendez/jsonbundle/v/stable.svg)](https://packagist.org/packages/sgmendez/jsonbundle) 
[![Total Downloads](https://poser.pugx.org/sgmendez/jsonbundle/downloads.svg)](https://packagist.org/packages/sgmendez/jsonbundle) 
[![Latest Unstable Version](https://poser.pugx.org/sgmendez/jsonbundle/v/unstable.svg)](https://packagist.org/packages/sgmendez/jsonbundle) 

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
$ composer require sgmendez/jsonbundle
```
Or require [`sgmendez/json`](http://sgmendez.github.io/json/)
into your `composer.json` file:


``` 
json
{
    "require": {
        "sgmendez/jsonbundle": "*"
    }
}
```

Register bundle on appKernel:

```php

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

## Use

For string JSON data:

```
php

$json = $this->get('json.parser');
$a = $json->decode($stringJson);

```

For local file JSON data:

```
php

$json = $this->get('json.parser');
$a = $json->decodeFile('file.json');

```

For remote file JSON data:

```
php

$json = $this->get('json.parser');
$a = $json->decodeFile('http://ip.jsontest.com/');

```


# License

Licensed under the BSD License:

   http://opensource.org/licenses/bsd-license.php

