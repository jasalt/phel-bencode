# Phel-bencode (alpha)

`Status: seems to roughly work, but testing needs to be done`

Phel library for converting [Phel](https://phel-lang.org/) datastructures to and from bencode using [arokettu/bencode](https://github.com/arokettu/bencode).

Some code and repository layout is based on [mabasic/phel-json](https://github.com/mabasic/phel-json) and builtin [`phel\json`](https://github.com/phel-lang/phel-lang/blob/acf3222dd6a1c30f277625018d0304c80d6db578/src/phel/json.phel) namespace.

## Overview

Library wraps `Arokettu\Bencode\Bencode` `encode` and `decode` methods.

- `encode`: Phel datastructures and basic types are converted to to PHP data structures before calling `(php/:: Bencode (encode data))` using `phel->php`.

- `decode`: Bencode strings are decoded using `(php/:: Bencode (decode data))` and converted to Phel data structures using `php->phel` function.

Functionality of `phel->php` and `php->phel` doing "deep" conversion is basically taken from functions in `phel\json` while they are renamed.

## Installation

Require with Composer into Phel project `composer require jasalt/phel-bencode`.

## Usage
REPL example:
```
(require jasalt\bencode :as bencode)

(bencode/encode ["foo" {:bar "baz"}])
# => l3:food3:bar3:bazee

(bencode/decode "l3:food3:bar3:bazee")
# => ["foo" {:bar "baz"}]  # quotes added around strings in REPL output here for convenience
```

## For developers
TODO
```
composer install
composer test  # test runner works but json library tests are not converted
```

## Contributing

Feel free to file issues in the repository or send pull requests.

## License

Phel-json is open-source software licensed under the [MIT license](https://opensource.org/licenses/MIT).
