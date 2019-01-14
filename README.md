# Alpine PHP Docker Images

This repository provides docker images for php versions `7.0+` in the both (separated) `CLI` and `FPM` variants with and without `xdebug` installed.
The basic image is `alpine` and always will be, therefore the `-alpine` suffix is not present.

| Flavour | CLI | PHP-FPM |
| --- | --- | --- |
| `vanilla` | `musurp/php:x-cli` | `musurp/php:x-fpm` |
| `xdebug` | `musurp/php-dev:x-cli` | `musurp/php-dev:x-fpm` |

The following versions are available:

* `7.0` (currently targeting `7.0.33`) (`final`)
* `7.1` (currently targeting `7.1.26`)
* `7.2` (currently targeting `7.2.14`)
* `7.3` (currently targeting `7.3.1`) (`stable`) (`xdebug @2.7.0-beta1`)

Alternatively for more refined version management (this is recommended) the images mentioned above have been tagged with the patch version also.
For example `musurp/php:7.1.26-cli` and `musurp/php-dev:7.2.14-fpm`.

* https://hub.docker.com/r/musurp/php/
* https://hub.docker.com/r/musurp/php-dev/

### Compiled Libraries

The images are all compiled with (where possible and required) the following libraries.

* `opcache`
* `xml`
* `zip`
* `intl`
* `bcmath`
* `mcrypt` (`<= 7.1`, `>` replaced with `openssl`)
* `pdo`
* `pgsql`

### Sizes

Image sizes are typically between `70mb` and `80mb` compressed.
Uncompressed the images sit at roughly double the size, last checked at `146mb`.
As of `7.3` images are looking around `160mb` uncompressed.

### Additional Commands

All images will also come with a few really basic commands pre-installed for developer convenience.

* `curl`
* `make`
* `git`
* `tree`
* `openssl-client`
