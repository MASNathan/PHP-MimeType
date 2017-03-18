# PHP MimeType library

[![Latest Stable Version](https://poser.pugx.org/josantonius/mimetype/v/stable)](https://packagist.org/packages/josantonius/mimetype) [![Total Downloads](https://poser.pugx.org/josantonius/mimetype/downloads)](https://packagist.org/packages/josantonius/mimetype) [![Latest Unstable Version](https://poser.pugx.org/josantonius/mimetype/v/unstable)](https://packagist.org/packages/josantonius/mimetype) [![License](https://poser.pugx.org/josantonius/mimetype/license)](https://packagist.org/packages/josantonius/mimetype)

[English version](README.md)

Librería PHP para obtener encabezados MIME y extensiones a partir de ellos.

---

- [Instalación](#instalación)
- [Requisitos](#requisitos)
- [Cómo empezar y ejemplos](#cómo-empezar-y-ejemplos)
- [Métodos disponibles](#métodos-disponibles)
- [Uso](#uso)
- [Tests](#tests)
- [Manejador de excepciones](#manejador-de-excepciones)
- [Contribuir](#contribuir)
- [Repositorio](#repositorio)
- [Licencia](#licencia)
- [Copyright](#copyright)

---

### Instalación 

La mejor forma de instalar esta extensión es a través de [composer](http://getcomposer.org/download/).

Para instalar PHP MimeType library, simplemente escribe:

    $ composer require Josantonius/MimeType

El comando anterior solamente instalará los archivos necesarios, si prefieres descargar todo el código, incluyendo tests, puedes utilizar:

    $ composer require Josantonius/MimeType --prefer-source

También puedes clonar el repositorio completo con Git:

  $ git clone https://github.com/Josantonius/PHP-MimeType.git 

### Requisitos

Esta ĺibrería es soportada por versiones de PHP 5.6 o superiores y es compatible con versiones de HHVM 3.0 o superiores.

### Cómo empezar y ejemplos

Para utilizar esta librería, simplemente:

```php
require __DIR__ . '/vendor/autoload.php';

use Josantonius\MimeType\MimeType;
```
### Métodos disponibles

Métodos disponibles en esta librería:

```php
MimeType::getMimeFromExtension();
MimeType::getExtensionFromMime();
MimeType::getAll();
```
### Uso

Ejemplo de uso para esta librería:

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

Para utilizar la clase de [pruebas](tests), simplemente:

```php
<?php
$loader = require __DIR__ . '/vendor/autoload.php';

$loader->addPsr4('Josantonius\\MimeType\\Tests\\', __DIR__ . '/vendor/josantonius/mimetype/tests');

use Josantonius\MimeType\Tests\MimeTypeTest;
```
Métodos de prueba disponibles en esta librería:

```php
MimeTypeTest::testGetMimeFromExtension();
MimeTypeTest::testGetMimeFromExtensionUndefined();
MimeTypeTest::testGetExtensionFromMime();
MimeTypeTest::testGetExtensionFromMimeUndefined();
MimeTypeTest::testGetAll();
```

### Manejador de excepciones

Esta librería utiliza [control de excepciones](src/Exception) que puedes personalizar a tu gusto.
### Contribuir
1. Comprobar si hay incidencias abiertas o abrir una nueva para iniciar una discusión en torno a un fallo o función.
1. Bifurca la rama del repositorio en GitHub para iniciar la operación de ajuste.
1. Escribe una o más pruebas para la nueva característica o expón el error.
1. Haz cambios en el código para implementar la característica o reparar el fallo.
1. Envía pull request para fusionar los cambios y que sean publicados.

Esto está pensado para proyectos grandes y de larga duración.

### Repositorio

Los archivos de este repositorio se crearon y subieron automáticamente con [Reposgit Creator](https://github.com/Josantonius/BASH-Reposgit).

### Licencia

Este proyecto está licenciado bajo **licencia MIT**. Consulta el archivo [LICENSE](LICENSE) para más información.

## Copyright

2017 Josantonius, [josantonius.com](https://josantonius.com/)

Si te ha resultado útil, házmelo saber :wink:

Puedes contactarme en [Twitter](https://twitter.com/Josantonius) o a través de mi [correo electrónico](mailto:hello@josantonius.com).