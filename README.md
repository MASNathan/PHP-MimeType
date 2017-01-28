# PHP MimeType library

[![Latest Stable Version](https://poser.pugx.org/josantonius/mimetype/v/stable)](https://packagist.org/packages/josantonius/mimetype) [![Total Downloads](https://poser.pugx.org/josantonius/mimetype/downloads)](https://packagist.org/packages/josantonius/mimetype) [![Latest Unstable Version](https://poser.pugx.org/josantonius/mimetype/v/unstable)](https://packagist.org/packages/josantonius/mimetype) [![License](https://poser.pugx.org/josantonius/mimetype/license)](https://packagist.org/packages/josantonius/mimetype)

[Spanish version](README-ES.md)

PHP library for obtain headers MIME.

---

- [Installation](#installation)
- [Requirements](#requirements)
- [Quick Start and Examples](#quick-start-and-examples)
- [Available Methods](#available-methods)
- [Usage](#usage)
- [Tests](#tests)
- [Exception Handler](#exception-handler)
- [Contribute](#contribute)
- [Repository](#repository)
- [Author](#author)
- [Licensing](#licensing)

---

### Installation

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

To install PHP MimeType library, simply:

    $ composer require Josantonius/MimeType

### Requirements

This library is supported by PHP versions 7.0 or higher and is compatible with HHVM versions 3.0 or higher.

To use this library in HHVM (HipHop Virtual Machine) you will have to activate the scalar types. Add the following line "hhvm.php7.scalar_types = true" in your "/etc/hhvm/php.ini".

### Quick Start and Examples

To use this class, simply:

```php
require __DIR__ . '/vendor/autoload.php';

use Josantonius\MimeType\MimeType;
```
### Available Methods

Available methods in this library:

```php
MimeType::getMimeFromExtension();
MimeType::getExtensionFromMime();
MimeType::getAll();
```
### Usage

Example of use for this library:

```php
<?php
require __DIR__ . '/vendor/autoload.php';

use Josantonius\MimeType\MimeType;

echo "[.json] → " . MimeType::getMimeFromExtension('.json'); // [.json] → application/json

echo "[text/html] → " . MimeType::getExtensionFromMime('text/html'); // [text/html] → .html

echo MimeType::getAll();

/*
array(682) {
  [".123"]=>
  string(27) "application/vnd.lotus-1-2-3"
  [".3dml"]=>
  string(18) "text/vnd.in3d.3dml"
  [".3g2"]=>
  string(11) "video/3gpp2"
  [".3gp"]=>
  string(10) "video/3gpp"
  [".7z"]=>
  string(27) "application/x-7z-compressed"
  [".aab"]=>
  string(28) "application/x-authorware-bin"
  [".aac"]=>
  string(11) "audio/x-aac"
  [".aam"]=>
  string(28) "application/x-authorware-map"
  [".aas"]=>
  string(28) "application/x-authorware-seg"
  [".abw"]=>
  string(21) "application/x-abiword"
(...)
*/
```

### Tests 

To use the [test](tests) class, simply:

```php
<?php
$loader = require __DIR__ . '/vendor/autoload.php';

$loader->addPsr4('Josantonius\\MimeType\\Tests\\', __DIR__ . '/vendor/josantonius/mimetype/tests');

use Josantonius\MimeType\Tests\MimeTypeTest;

```
Available test methods in this library:

```php
MimeTypeTest::testGetMimeFromExtension();
MimeTypeTest::testGetMimeFromExtensionUndefined();
MimeTypeTest::testGetExtensionFromMime();
MimeTypeTest::testGetExtensionFromMimeUndefined();
MimeTypeTest::testGetAll();
```

### Exception Handler

This library uses [exception handler](src/Exception) that you can customize.
### Contribute
1. Check for open issues or open a new issue to start a discussion around a bug or feature.
1. Fork the repository on GitHub to start making your changes.
1. Write one or more tests for the new feature or that expose the bug.
1. Make code changes to implement the feature or fix the bug.
1. Send a pull request to get your changes merged and published.

This is intended for large and long-lived objects.

### Repository

All files in this repository were created and uploaded automatically with [Reposgit Creator](https://github.com/Josantonius/BASH-Reposgit).

### Author

Maintained by [Josantonius](https://github.com/Josantonius/).

### Licensing

This project is licensed under **MIT license**. See the [LICENSE](LICENSE) file for more info.