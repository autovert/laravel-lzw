# Laravel LZW

[![Latest Version on Packagist](https://img.shields.io/packagist/v/openbitapp/laravel-lzw.svg?style=flat-square)](https://packagist.org/packages/openbitapp/laravel-lzw)
[![Total Downloads](https://img.shields.io/packagist/dt/openbitapp/laravel-lzw.svg?style=flat-square)](https://packagist.org/packages/openbitapp/laravel-lzw)

Lempel–Ziv–Welch (LZW) is a universal lossless data compression algorithm. This package offers support for compressing and decompressing data using LZW.

**Updated Fork**: This fork supports PHP 8.x and Laravel 12, maintaining backward compatibility with PHP 7.1.3+ and Laravel 5.8+.

## Requirements

- PHP ^7.1.3|^8.0 (supports PHP 8.3.17+)
- Laravel ^5.8|^6.0|^7.0|^8.0|^9.0|^10.0|^11.0|^12.0

## Installation

Since this package is not published on Packagist, you need to add the GitHub repository first:

### Step 1: Add Repository
Add this to your project's `composer.json`:

```json
{
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/autovert/laravel-lzw.git"
        }
    ]
}
```

### Step 2: Install Package
Then install via composer:

```bash
composer require autovert/laravel-lzw
```

**Alternative one-liner:**
```bash
composer config repositories.autovert-laravel-lzw vcs https://github.com/autovert/laravel-lzw.git
composer require autovert/laravel-lzw
```

The package registers itself and its facade automatically.

## Usage

You can compress and decompress data using the facade.

``` php
$data = LZW::compress('String data to compress');

$data->toString();
$data->toArray();
$data->toJson();

LZW::decompress($data->toString());
LZW::decompress($data->toArray());
```

### Testing

``` bash
./vendor/bin/phpunit
```

## Credits

- [Rosetta Code](http://rosettacode.org/wiki/LZW_compression#PHP)
- [Andrea Martini](https://github.com/anmartini)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
