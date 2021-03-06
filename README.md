# LolautruchePaylineBundle

[![SensioLabsInsight](https://insight.sensiolabs.com/projects/4d54fe75-e1ee-4c67-94b6-7db9bbbda418/big.png)](https://insight.sensiolabs.com/projects/4d54fe75-e1ee-4c67-94b6-7db9bbbda418)
[![Build Status](https://travis-ci.org/lolautruche/LolautruchePaylineBundle.svg?branch=master)](https://travis-ci.org/lolautruche/LolautruchePaylineBundle)

Integrates [Payline payment solution](http://www.payline.com/) with Symfony.


## Features

* Service integration and simple semantic configuration
* Simplified API for web payments
* Automatically validates web payments
* Extensibility using events


## Prerequisites

### Payline account
You will of course need a valid Payline account.

Mandatory elements from you Payline account are:
* **Merchant ID**
* **Access key**, which you can generate in Payline admin
* **Contract number**, related to the means of payment you configured in Payline admin

### PHP
* PHP 5.4+ / 7.0+
* [PHP SOAP extension](http://php.net/soap) for Payline SDK

### Symfony
Symfony 2.7.10+ / 3.0.3+


## Installation

This bundle is available on [Packagist](https://packagist.org/packages/lolautruche/payline-bundle).
You can install it using Composer.

```
composer require lolautruche/payline-bundle
```

Then add it to your application:

```php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = [
        // ...
        new Lolautruche\PaylineBundle\LolautruchePaylineBundle,
        // ...
    ];
}
```

Add the routes to your `routing.yml`:

```yaml
LolautruchePaylineBundle:
    resource: "@LolautruchePaylineBundle/Resources/config/routing.yml"
    prefix:   /
```


## Documentation

See [Resources/doc/](Resources/doc/00-index.md)
