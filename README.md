# Phel-bencode

Phel library for converting [Phel](https://phel-lang.org/) datastructures to and from bencode using [arokettu/bencode](https://github.com/arokettu/bencode) based on [mabasic/phel-json](https://github.com/mabasic/phel-json).

## Overview

This Phel library is a wrapper library around `Arokettu\Bencode\Bencode` `encode` and `decode` methods.

It converts Phel datastructures and basic types to a format that PHP understands before calling `(php/:: Bencode (encode data))`.

It generates valid Phel datastructures (map, vector) from given JSON strings using `(php/:: Bencode (decode data))`.

## Installation
TODO

## Usage
TODO
## For developers
TODO
```
composer install
composer test
```

## Contributing

Feel free to file issues in the repository after WIP status has been removed.

## License

Phel-json is open-source software licensed under the [MIT license](https://opensource.org/licenses/MIT).
