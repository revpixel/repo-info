# `nextcloud:12.0.10-fpm-alpine`

## Docker Metadata

- Image ID: `sha256:7b9b930cce0a1125cf1faba5d3fcc269785e4d33903b1bac599da54258e35025`
- Created: `2018-07-23T21:28:01.319951743Z`
- Virtual Size: ~ 278.62 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/entrypoint.sh"]`
- Command: `["php-fpm"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c`
  - `PHP_INI_DIR=/usr/local/etc/php`
  - `PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi`
  - `PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2`
  - `PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2`
  - `PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie`
  - `GPG_KEYS=A917B1ECDA84AEC2B568FED6F50ABC807BD5DCD0 528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 1729F83938DA44E27BA0F4D3DBDB397470D12172`
  - `PHP_VERSION=7.1.20`
  - `PHP_URL=https://secure.php.net/get/php-7.1.20.tar.xz/from/this/mirror`
  - `PHP_ASC_URL=https://secure.php.net/get/php-7.1.20.tar.xz.asc/from/this/mirror`
  - `PHP_SHA256=cd7d1006201459d43fae0790cce4eb3451add5c87f4cadb13b228d4c179b850c`
  - `PHP_MD5=`
  - `NEXTCLOUD_VERSION=12.0.10`
