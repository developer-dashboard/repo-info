<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `adminer`

-	[`adminer:4.3.1-standalone`](#adminer431-standalone)
-	[`adminer:4.3-standalone`](#adminer43-standalone)
-	[`adminer:4-standalone`](#adminer4-standalone)
-	[`adminer:standalone`](#adminerstandalone)
-	[`adminer:4.3.1`](#adminer431)
-	[`adminer:4.3`](#adminer43)
-	[`adminer:4`](#adminer4)
-	[`adminer:latest`](#adminerlatest)
-	[`adminer:4.3.1-fastcgi`](#adminer431-fastcgi)
-	[`adminer:4.3-fastcgi`](#adminer43-fastcgi)
-	[`adminer:4-fastcgi`](#adminer4-fastcgi)
-	[`adminer:fastcgi`](#adminerfastcgi)

## `adminer:4.3.1-standalone`

```console
$ docker pull adminer@sha256:adfc8f4bddc169d80030e2550a2fb5e9738fd1e1d7d53887e8346d5022fec871
```

-	Platforms:
	-	linux; amd64

### `adminer:4.3.1-standalone` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28252939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c8c0237c2814591c029ed1eaed333377278cadb1dc1919b182fb04e0f78272`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","0.0.0.0:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 14:58:40 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 14:58:41 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 14:58:51 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 14:58:52 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:13 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:02:15 GMT
COPY multi:a2a7a051ede432913cebaf532ceb4314b5a5c79d08a5a33e42d3563097520588 in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:02:16 GMT
CMD ["php" "-a"]
# Tue, 30 May 2017 16:04:39 GMT
STOPSIGNAL [SIGINT]
# Tue, 30 May 2017 16:04:40 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:04:41 GMT
WORKDIR /var/www/html
# Tue, 30 May 2017 16:04:45 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:05:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:05:06 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:05:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:05:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:05:12 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:05:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:05:14 GMT
USER [adminer]
# Tue, 30 May 2017 16:05:15 GMT
CMD ["php" "-S" "0.0.0.0:8080" "-t" "/var/www/html"]
# Tue, 30 May 2017 16:05:15 GMT
EXPOSE 8080/tcp
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c899104e150daa73fbb949f8359b719c13eef86f209463a4a76cab27ae535882`  
		Last Modified: Fri, 26 May 2017 15:36:30 GMT  
		Size: 12.8 MB (12769025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee6f1eff17ec8018e04e330b724d29575522c9f78f598521eee151ce068ca7a`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e142234e83a67a353b8006404caeab1f0e810961ec7da41d3ff141814c0ef2`  
		Last Modified: Fri, 26 May 2017 15:36:28 GMT  
		Size: 10.4 MB (10364730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d330f46143dcbf5b3289bacf51c1ae1edd2800f82f1a5661ae3499afcea7de`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38346e0038111f335149ab5f37998490075184f481372f64bdd58fe570fac404`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b3b3466337b9d4689b7859a08c4e9051ea645faf0d8bc214c7ef6d5986ac6a`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.2 MB (1210527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12410c90b0f7777f33ae936a3fece93ccbb6a27281b2773f78694a539165f40c`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 118.0 KB (117969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a047f0f829a4b995700b6c52c9ffa1634ba3cd7d0cbf110adf13577c68303990`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cff7efbdffdd8ad8592873e06d16b664532926928b5b61175da941d15b4e3`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57528dee1c125d6241db9af2b723e67b8c1933df5643cfb2ad0ae2a5f813fcaa`  
		Last Modified: Tue, 30 May 2017 16:07:23 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.3-standalone`

```console
$ docker pull adminer@sha256:adfc8f4bddc169d80030e2550a2fb5e9738fd1e1d7d53887e8346d5022fec871
```

-	Platforms:
	-	linux; amd64

### `adminer:4.3-standalone` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28252939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c8c0237c2814591c029ed1eaed333377278cadb1dc1919b182fb04e0f78272`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","0.0.0.0:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 14:58:40 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 14:58:41 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 14:58:51 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 14:58:52 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:13 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:02:15 GMT
COPY multi:a2a7a051ede432913cebaf532ceb4314b5a5c79d08a5a33e42d3563097520588 in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:02:16 GMT
CMD ["php" "-a"]
# Tue, 30 May 2017 16:04:39 GMT
STOPSIGNAL [SIGINT]
# Tue, 30 May 2017 16:04:40 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:04:41 GMT
WORKDIR /var/www/html
# Tue, 30 May 2017 16:04:45 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:05:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:05:06 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:05:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:05:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:05:12 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:05:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:05:14 GMT
USER [adminer]
# Tue, 30 May 2017 16:05:15 GMT
CMD ["php" "-S" "0.0.0.0:8080" "-t" "/var/www/html"]
# Tue, 30 May 2017 16:05:15 GMT
EXPOSE 8080/tcp
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c899104e150daa73fbb949f8359b719c13eef86f209463a4a76cab27ae535882`  
		Last Modified: Fri, 26 May 2017 15:36:30 GMT  
		Size: 12.8 MB (12769025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee6f1eff17ec8018e04e330b724d29575522c9f78f598521eee151ce068ca7a`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e142234e83a67a353b8006404caeab1f0e810961ec7da41d3ff141814c0ef2`  
		Last Modified: Fri, 26 May 2017 15:36:28 GMT  
		Size: 10.4 MB (10364730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d330f46143dcbf5b3289bacf51c1ae1edd2800f82f1a5661ae3499afcea7de`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38346e0038111f335149ab5f37998490075184f481372f64bdd58fe570fac404`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b3b3466337b9d4689b7859a08c4e9051ea645faf0d8bc214c7ef6d5986ac6a`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.2 MB (1210527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12410c90b0f7777f33ae936a3fece93ccbb6a27281b2773f78694a539165f40c`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 118.0 KB (117969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a047f0f829a4b995700b6c52c9ffa1634ba3cd7d0cbf110adf13577c68303990`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cff7efbdffdd8ad8592873e06d16b664532926928b5b61175da941d15b4e3`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57528dee1c125d6241db9af2b723e67b8c1933df5643cfb2ad0ae2a5f813fcaa`  
		Last Modified: Tue, 30 May 2017 16:07:23 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:adfc8f4bddc169d80030e2550a2fb5e9738fd1e1d7d53887e8346d5022fec871
```

-	Platforms:
	-	linux; amd64

### `adminer:4-standalone` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28252939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c8c0237c2814591c029ed1eaed333377278cadb1dc1919b182fb04e0f78272`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","0.0.0.0:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 14:58:40 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 14:58:41 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 14:58:51 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 14:58:52 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:13 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:02:15 GMT
COPY multi:a2a7a051ede432913cebaf532ceb4314b5a5c79d08a5a33e42d3563097520588 in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:02:16 GMT
CMD ["php" "-a"]
# Tue, 30 May 2017 16:04:39 GMT
STOPSIGNAL [SIGINT]
# Tue, 30 May 2017 16:04:40 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:04:41 GMT
WORKDIR /var/www/html
# Tue, 30 May 2017 16:04:45 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:05:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:05:06 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:05:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:05:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:05:12 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:05:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:05:14 GMT
USER [adminer]
# Tue, 30 May 2017 16:05:15 GMT
CMD ["php" "-S" "0.0.0.0:8080" "-t" "/var/www/html"]
# Tue, 30 May 2017 16:05:15 GMT
EXPOSE 8080/tcp
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c899104e150daa73fbb949f8359b719c13eef86f209463a4a76cab27ae535882`  
		Last Modified: Fri, 26 May 2017 15:36:30 GMT  
		Size: 12.8 MB (12769025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee6f1eff17ec8018e04e330b724d29575522c9f78f598521eee151ce068ca7a`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e142234e83a67a353b8006404caeab1f0e810961ec7da41d3ff141814c0ef2`  
		Last Modified: Fri, 26 May 2017 15:36:28 GMT  
		Size: 10.4 MB (10364730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d330f46143dcbf5b3289bacf51c1ae1edd2800f82f1a5661ae3499afcea7de`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38346e0038111f335149ab5f37998490075184f481372f64bdd58fe570fac404`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b3b3466337b9d4689b7859a08c4e9051ea645faf0d8bc214c7ef6d5986ac6a`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.2 MB (1210527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12410c90b0f7777f33ae936a3fece93ccbb6a27281b2773f78694a539165f40c`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 118.0 KB (117969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a047f0f829a4b995700b6c52c9ffa1634ba3cd7d0cbf110adf13577c68303990`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cff7efbdffdd8ad8592873e06d16b664532926928b5b61175da941d15b4e3`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57528dee1c125d6241db9af2b723e67b8c1933df5643cfb2ad0ae2a5f813fcaa`  
		Last Modified: Tue, 30 May 2017 16:07:23 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:standalone`

```console
$ docker pull adminer@sha256:adfc8f4bddc169d80030e2550a2fb5e9738fd1e1d7d53887e8346d5022fec871
```

-	Platforms:
	-	linux; amd64

### `adminer:standalone` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28252939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c8c0237c2814591c029ed1eaed333377278cadb1dc1919b182fb04e0f78272`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","0.0.0.0:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 14:58:40 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 14:58:41 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 14:58:51 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 14:58:52 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:13 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:02:15 GMT
COPY multi:a2a7a051ede432913cebaf532ceb4314b5a5c79d08a5a33e42d3563097520588 in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:02:16 GMT
CMD ["php" "-a"]
# Tue, 30 May 2017 16:04:39 GMT
STOPSIGNAL [SIGINT]
# Tue, 30 May 2017 16:04:40 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:04:41 GMT
WORKDIR /var/www/html
# Tue, 30 May 2017 16:04:45 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:05:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:05:06 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:05:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:05:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:05:12 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:05:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:05:14 GMT
USER [adminer]
# Tue, 30 May 2017 16:05:15 GMT
CMD ["php" "-S" "0.0.0.0:8080" "-t" "/var/www/html"]
# Tue, 30 May 2017 16:05:15 GMT
EXPOSE 8080/tcp
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c899104e150daa73fbb949f8359b719c13eef86f209463a4a76cab27ae535882`  
		Last Modified: Fri, 26 May 2017 15:36:30 GMT  
		Size: 12.8 MB (12769025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee6f1eff17ec8018e04e330b724d29575522c9f78f598521eee151ce068ca7a`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e142234e83a67a353b8006404caeab1f0e810961ec7da41d3ff141814c0ef2`  
		Last Modified: Fri, 26 May 2017 15:36:28 GMT  
		Size: 10.4 MB (10364730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d330f46143dcbf5b3289bacf51c1ae1edd2800f82f1a5661ae3499afcea7de`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38346e0038111f335149ab5f37998490075184f481372f64bdd58fe570fac404`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b3b3466337b9d4689b7859a08c4e9051ea645faf0d8bc214c7ef6d5986ac6a`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.2 MB (1210527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12410c90b0f7777f33ae936a3fece93ccbb6a27281b2773f78694a539165f40c`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 118.0 KB (117969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a047f0f829a4b995700b6c52c9ffa1634ba3cd7d0cbf110adf13577c68303990`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cff7efbdffdd8ad8592873e06d16b664532926928b5b61175da941d15b4e3`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57528dee1c125d6241db9af2b723e67b8c1933df5643cfb2ad0ae2a5f813fcaa`  
		Last Modified: Tue, 30 May 2017 16:07:23 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.3.1`

```console
$ docker pull adminer@sha256:adfc8f4bddc169d80030e2550a2fb5e9738fd1e1d7d53887e8346d5022fec871
```

-	Platforms:
	-	linux; amd64

### `adminer:4.3.1` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28252939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c8c0237c2814591c029ed1eaed333377278cadb1dc1919b182fb04e0f78272`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","0.0.0.0:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 14:58:40 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 14:58:41 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 14:58:51 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 14:58:52 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:13 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:02:15 GMT
COPY multi:a2a7a051ede432913cebaf532ceb4314b5a5c79d08a5a33e42d3563097520588 in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:02:16 GMT
CMD ["php" "-a"]
# Tue, 30 May 2017 16:04:39 GMT
STOPSIGNAL [SIGINT]
# Tue, 30 May 2017 16:04:40 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:04:41 GMT
WORKDIR /var/www/html
# Tue, 30 May 2017 16:04:45 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:05:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:05:06 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:05:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:05:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:05:12 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:05:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:05:14 GMT
USER [adminer]
# Tue, 30 May 2017 16:05:15 GMT
CMD ["php" "-S" "0.0.0.0:8080" "-t" "/var/www/html"]
# Tue, 30 May 2017 16:05:15 GMT
EXPOSE 8080/tcp
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c899104e150daa73fbb949f8359b719c13eef86f209463a4a76cab27ae535882`  
		Last Modified: Fri, 26 May 2017 15:36:30 GMT  
		Size: 12.8 MB (12769025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee6f1eff17ec8018e04e330b724d29575522c9f78f598521eee151ce068ca7a`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e142234e83a67a353b8006404caeab1f0e810961ec7da41d3ff141814c0ef2`  
		Last Modified: Fri, 26 May 2017 15:36:28 GMT  
		Size: 10.4 MB (10364730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d330f46143dcbf5b3289bacf51c1ae1edd2800f82f1a5661ae3499afcea7de`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38346e0038111f335149ab5f37998490075184f481372f64bdd58fe570fac404`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b3b3466337b9d4689b7859a08c4e9051ea645faf0d8bc214c7ef6d5986ac6a`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.2 MB (1210527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12410c90b0f7777f33ae936a3fece93ccbb6a27281b2773f78694a539165f40c`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 118.0 KB (117969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a047f0f829a4b995700b6c52c9ffa1634ba3cd7d0cbf110adf13577c68303990`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cff7efbdffdd8ad8592873e06d16b664532926928b5b61175da941d15b4e3`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57528dee1c125d6241db9af2b723e67b8c1933df5643cfb2ad0ae2a5f813fcaa`  
		Last Modified: Tue, 30 May 2017 16:07:23 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.3`

```console
$ docker pull adminer@sha256:adfc8f4bddc169d80030e2550a2fb5e9738fd1e1d7d53887e8346d5022fec871
```

-	Platforms:
	-	linux; amd64

### `adminer:4.3` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28252939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c8c0237c2814591c029ed1eaed333377278cadb1dc1919b182fb04e0f78272`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","0.0.0.0:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 14:58:40 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 14:58:41 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 14:58:51 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 14:58:52 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:13 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:02:15 GMT
COPY multi:a2a7a051ede432913cebaf532ceb4314b5a5c79d08a5a33e42d3563097520588 in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:02:16 GMT
CMD ["php" "-a"]
# Tue, 30 May 2017 16:04:39 GMT
STOPSIGNAL [SIGINT]
# Tue, 30 May 2017 16:04:40 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:04:41 GMT
WORKDIR /var/www/html
# Tue, 30 May 2017 16:04:45 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:05:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:05:06 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:05:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:05:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:05:12 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:05:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:05:14 GMT
USER [adminer]
# Tue, 30 May 2017 16:05:15 GMT
CMD ["php" "-S" "0.0.0.0:8080" "-t" "/var/www/html"]
# Tue, 30 May 2017 16:05:15 GMT
EXPOSE 8080/tcp
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c899104e150daa73fbb949f8359b719c13eef86f209463a4a76cab27ae535882`  
		Last Modified: Fri, 26 May 2017 15:36:30 GMT  
		Size: 12.8 MB (12769025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee6f1eff17ec8018e04e330b724d29575522c9f78f598521eee151ce068ca7a`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e142234e83a67a353b8006404caeab1f0e810961ec7da41d3ff141814c0ef2`  
		Last Modified: Fri, 26 May 2017 15:36:28 GMT  
		Size: 10.4 MB (10364730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d330f46143dcbf5b3289bacf51c1ae1edd2800f82f1a5661ae3499afcea7de`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38346e0038111f335149ab5f37998490075184f481372f64bdd58fe570fac404`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b3b3466337b9d4689b7859a08c4e9051ea645faf0d8bc214c7ef6d5986ac6a`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.2 MB (1210527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12410c90b0f7777f33ae936a3fece93ccbb6a27281b2773f78694a539165f40c`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 118.0 KB (117969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a047f0f829a4b995700b6c52c9ffa1634ba3cd7d0cbf110adf13577c68303990`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cff7efbdffdd8ad8592873e06d16b664532926928b5b61175da941d15b4e3`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57528dee1c125d6241db9af2b723e67b8c1933df5643cfb2ad0ae2a5f813fcaa`  
		Last Modified: Tue, 30 May 2017 16:07:23 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4`

```console
$ docker pull adminer@sha256:adfc8f4bddc169d80030e2550a2fb5e9738fd1e1d7d53887e8346d5022fec871
```

-	Platforms:
	-	linux; amd64

### `adminer:4` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28252939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c8c0237c2814591c029ed1eaed333377278cadb1dc1919b182fb04e0f78272`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","0.0.0.0:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 14:58:40 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 14:58:41 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 14:58:51 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 14:58:52 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:13 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:02:15 GMT
COPY multi:a2a7a051ede432913cebaf532ceb4314b5a5c79d08a5a33e42d3563097520588 in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:02:16 GMT
CMD ["php" "-a"]
# Tue, 30 May 2017 16:04:39 GMT
STOPSIGNAL [SIGINT]
# Tue, 30 May 2017 16:04:40 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:04:41 GMT
WORKDIR /var/www/html
# Tue, 30 May 2017 16:04:45 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:05:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:05:06 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:05:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:05:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:05:12 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:05:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:05:14 GMT
USER [adminer]
# Tue, 30 May 2017 16:05:15 GMT
CMD ["php" "-S" "0.0.0.0:8080" "-t" "/var/www/html"]
# Tue, 30 May 2017 16:05:15 GMT
EXPOSE 8080/tcp
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c899104e150daa73fbb949f8359b719c13eef86f209463a4a76cab27ae535882`  
		Last Modified: Fri, 26 May 2017 15:36:30 GMT  
		Size: 12.8 MB (12769025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee6f1eff17ec8018e04e330b724d29575522c9f78f598521eee151ce068ca7a`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e142234e83a67a353b8006404caeab1f0e810961ec7da41d3ff141814c0ef2`  
		Last Modified: Fri, 26 May 2017 15:36:28 GMT  
		Size: 10.4 MB (10364730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d330f46143dcbf5b3289bacf51c1ae1edd2800f82f1a5661ae3499afcea7de`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38346e0038111f335149ab5f37998490075184f481372f64bdd58fe570fac404`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b3b3466337b9d4689b7859a08c4e9051ea645faf0d8bc214c7ef6d5986ac6a`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.2 MB (1210527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12410c90b0f7777f33ae936a3fece93ccbb6a27281b2773f78694a539165f40c`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 118.0 KB (117969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a047f0f829a4b995700b6c52c9ffa1634ba3cd7d0cbf110adf13577c68303990`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cff7efbdffdd8ad8592873e06d16b664532926928b5b61175da941d15b4e3`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57528dee1c125d6241db9af2b723e67b8c1933df5643cfb2ad0ae2a5f813fcaa`  
		Last Modified: Tue, 30 May 2017 16:07:23 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:latest`

```console
$ docker pull adminer@sha256:adfc8f4bddc169d80030e2550a2fb5e9738fd1e1d7d53887e8346d5022fec871
```

-	Platforms:
	-	linux; amd64

### `adminer:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28252939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c8c0237c2814591c029ed1eaed333377278cadb1dc1919b182fb04e0f78272`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","0.0.0.0:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:39:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 14:58:40 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 14:58:41 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 14:58:42 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 14:58:51 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 14:58:52 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:13 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:02:15 GMT
COPY multi:a2a7a051ede432913cebaf532ceb4314b5a5c79d08a5a33e42d3563097520588 in /usr/local/bin/ 
# Fri, 26 May 2017 15:02:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:02:16 GMT
CMD ["php" "-a"]
# Tue, 30 May 2017 16:04:39 GMT
STOPSIGNAL [SIGINT]
# Tue, 30 May 2017 16:04:40 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:04:41 GMT
WORKDIR /var/www/html
# Tue, 30 May 2017 16:04:45 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:05:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:05:06 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:05:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:05:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:05:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:05:12 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:05:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:05:14 GMT
USER [adminer]
# Tue, 30 May 2017 16:05:15 GMT
CMD ["php" "-S" "0.0.0.0:8080" "-t" "/var/www/html"]
# Tue, 30 May 2017 16:05:15 GMT
EXPOSE 8080/tcp
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c899104e150daa73fbb949f8359b719c13eef86f209463a4a76cab27ae535882`  
		Last Modified: Fri, 26 May 2017 15:36:30 GMT  
		Size: 12.8 MB (12769025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee6f1eff17ec8018e04e330b724d29575522c9f78f598521eee151ce068ca7a`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e142234e83a67a353b8006404caeab1f0e810961ec7da41d3ff141814c0ef2`  
		Last Modified: Fri, 26 May 2017 15:36:28 GMT  
		Size: 10.4 MB (10364730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d330f46143dcbf5b3289bacf51c1ae1edd2800f82f1a5661ae3499afcea7de`  
		Last Modified: Fri, 26 May 2017 15:36:26 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38346e0038111f335149ab5f37998490075184f481372f64bdd58fe570fac404`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b3b3466337b9d4689b7859a08c4e9051ea645faf0d8bc214c7ef6d5986ac6a`  
		Last Modified: Tue, 30 May 2017 16:07:21 GMT  
		Size: 1.2 MB (1210527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12410c90b0f7777f33ae936a3fece93ccbb6a27281b2773f78694a539165f40c`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 118.0 KB (117969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a047f0f829a4b995700b6c52c9ffa1634ba3cd7d0cbf110adf13577c68303990`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cff7efbdffdd8ad8592873e06d16b664532926928b5b61175da941d15b4e3`  
		Last Modified: Tue, 30 May 2017 16:07:20 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57528dee1c125d6241db9af2b723e67b8c1933df5643cfb2ad0ae2a5f813fcaa`  
		Last Modified: Tue, 30 May 2017 16:07:23 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.3.1-fastcgi`

```console
$ docker pull adminer@sha256:c02e6cd1683288a8774745f40415be06d3c592275747e03c07c7b8e1c430e699
```

-	Platforms:
	-	linux; amd64

### `adminer:4.3.1-fastcgi` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31955635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a913061a534c28d99d66333a5deadc44459d6087b8cd4afdd9cd4c916bc7fd8`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:49:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Fri, 26 May 2017 14:49:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:49:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:49:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 15:02:39 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 15:02:39 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 15:02:40 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 15:02:41 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 15:02:48 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 15:02:49 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:06:15 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:06:17 GMT
COPY multi:1401feee8064a06ad514519ec870939c946ecfdf381c82a90cb2035486938ee9 in /usr/local/bin/ 
# Fri, 26 May 2017 15:06:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:06:18 GMT
WORKDIR /var/www/html
# Fri, 26 May 2017 15:06:20 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 26 May 2017 15:06:21 GMT
EXPOSE 9000/tcp
# Fri, 26 May 2017 15:06:21 GMT
CMD ["php-fpm"]
# Tue, 30 May 2017 16:03:46 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:03:50 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:04:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:04:09 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:04:10 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:04:11 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:04:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:04:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:04:15 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:04:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:04:17 GMT
USER [adminer]
# Tue, 30 May 2017 16:04:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87959aa873124b10b69066e4668db64c75fd8a16dc8118e3de8878cf99065d7`  
		Last Modified: Fri, 26 May 2017 15:38:57 GMT  
		Size: 12.8 MB (12769026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad35336e465e1720333b4d90a4b3d30c925109c9fd0e216d42950e5cd8ce9928`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 484.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb46f99aeee7bf390bf8c3b37e081fc7b0973f5178fd00f1838617536b96c50`  
		Last Modified: Fri, 26 May 2017 15:38:58 GMT  
		Size: 14.1 MB (14059644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be0078492bc2657aa9b7d5430827c67882fe5fa8f298d7cf3894ee2dd1d13d0`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba81a0e17b2cdca00e27acdddaa4a9d83e3868804e58d42f3cd4fbddba828691`  
		Last Modified: Fri, 26 May 2017 15:38:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc5954361df3c3b3f47844c62f38babad709b56d618cca32fc80cb84109bb0b`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aef245e79767c445ac7895105739a20ace7f7841d99c6fb7d3fda9d1d8b9d04`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb5b7cf70ded65be8bdd0cca34e03527f014cd8e16b9f65ad614d70a4387d02`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.2 MB (1210524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e2537d23fd6823f335c8be0a6b4652bf47b8a50ac45aff54555ece99a7a75d`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 118.0 KB (117967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382afa8f1ecd0dcfe3550ec5267aa91935502e4f0fe35d6afc8eb2568dc19a42`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84229ee9c2a0af5e27ee0560b9b7981e1ff0b41f3f60b74ec5ab1467011f7ba3`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f82f4ce706b55dd8e8ac3e953cc4f0d4faa51a1f5cec8415cf6fc272e4747ab`  
		Last Modified: Tue, 30 May 2017 16:05:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.3-fastcgi`

```console
$ docker pull adminer@sha256:c02e6cd1683288a8774745f40415be06d3c592275747e03c07c7b8e1c430e699
```

-	Platforms:
	-	linux; amd64

### `adminer:4.3-fastcgi` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31955635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a913061a534c28d99d66333a5deadc44459d6087b8cd4afdd9cd4c916bc7fd8`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:49:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Fri, 26 May 2017 14:49:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:49:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:49:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 15:02:39 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 15:02:39 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 15:02:40 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 15:02:41 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 15:02:48 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 15:02:49 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:06:15 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:06:17 GMT
COPY multi:1401feee8064a06ad514519ec870939c946ecfdf381c82a90cb2035486938ee9 in /usr/local/bin/ 
# Fri, 26 May 2017 15:06:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:06:18 GMT
WORKDIR /var/www/html
# Fri, 26 May 2017 15:06:20 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 26 May 2017 15:06:21 GMT
EXPOSE 9000/tcp
# Fri, 26 May 2017 15:06:21 GMT
CMD ["php-fpm"]
# Tue, 30 May 2017 16:03:46 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:03:50 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:04:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:04:09 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:04:10 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:04:11 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:04:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:04:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:04:15 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:04:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:04:17 GMT
USER [adminer]
# Tue, 30 May 2017 16:04:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87959aa873124b10b69066e4668db64c75fd8a16dc8118e3de8878cf99065d7`  
		Last Modified: Fri, 26 May 2017 15:38:57 GMT  
		Size: 12.8 MB (12769026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad35336e465e1720333b4d90a4b3d30c925109c9fd0e216d42950e5cd8ce9928`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 484.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb46f99aeee7bf390bf8c3b37e081fc7b0973f5178fd00f1838617536b96c50`  
		Last Modified: Fri, 26 May 2017 15:38:58 GMT  
		Size: 14.1 MB (14059644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be0078492bc2657aa9b7d5430827c67882fe5fa8f298d7cf3894ee2dd1d13d0`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba81a0e17b2cdca00e27acdddaa4a9d83e3868804e58d42f3cd4fbddba828691`  
		Last Modified: Fri, 26 May 2017 15:38:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc5954361df3c3b3f47844c62f38babad709b56d618cca32fc80cb84109bb0b`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aef245e79767c445ac7895105739a20ace7f7841d99c6fb7d3fda9d1d8b9d04`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb5b7cf70ded65be8bdd0cca34e03527f014cd8e16b9f65ad614d70a4387d02`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.2 MB (1210524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e2537d23fd6823f335c8be0a6b4652bf47b8a50ac45aff54555ece99a7a75d`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 118.0 KB (117967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382afa8f1ecd0dcfe3550ec5267aa91935502e4f0fe35d6afc8eb2568dc19a42`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84229ee9c2a0af5e27ee0560b9b7981e1ff0b41f3f60b74ec5ab1467011f7ba3`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f82f4ce706b55dd8e8ac3e953cc4f0d4faa51a1f5cec8415cf6fc272e4747ab`  
		Last Modified: Tue, 30 May 2017 16:05:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:c02e6cd1683288a8774745f40415be06d3c592275747e03c07c7b8e1c430e699
```

-	Platforms:
	-	linux; amd64

### `adminer:4-fastcgi` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31955635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a913061a534c28d99d66333a5deadc44459d6087b8cd4afdd9cd4c916bc7fd8`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:49:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Fri, 26 May 2017 14:49:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:49:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:49:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 15:02:39 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 15:02:39 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 15:02:40 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 15:02:41 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 15:02:48 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 15:02:49 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:06:15 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:06:17 GMT
COPY multi:1401feee8064a06ad514519ec870939c946ecfdf381c82a90cb2035486938ee9 in /usr/local/bin/ 
# Fri, 26 May 2017 15:06:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:06:18 GMT
WORKDIR /var/www/html
# Fri, 26 May 2017 15:06:20 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 26 May 2017 15:06:21 GMT
EXPOSE 9000/tcp
# Fri, 26 May 2017 15:06:21 GMT
CMD ["php-fpm"]
# Tue, 30 May 2017 16:03:46 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:03:50 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:04:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:04:09 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:04:10 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:04:11 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:04:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:04:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:04:15 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:04:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:04:17 GMT
USER [adminer]
# Tue, 30 May 2017 16:04:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87959aa873124b10b69066e4668db64c75fd8a16dc8118e3de8878cf99065d7`  
		Last Modified: Fri, 26 May 2017 15:38:57 GMT  
		Size: 12.8 MB (12769026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad35336e465e1720333b4d90a4b3d30c925109c9fd0e216d42950e5cd8ce9928`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 484.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb46f99aeee7bf390bf8c3b37e081fc7b0973f5178fd00f1838617536b96c50`  
		Last Modified: Fri, 26 May 2017 15:38:58 GMT  
		Size: 14.1 MB (14059644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be0078492bc2657aa9b7d5430827c67882fe5fa8f298d7cf3894ee2dd1d13d0`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba81a0e17b2cdca00e27acdddaa4a9d83e3868804e58d42f3cd4fbddba828691`  
		Last Modified: Fri, 26 May 2017 15:38:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc5954361df3c3b3f47844c62f38babad709b56d618cca32fc80cb84109bb0b`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aef245e79767c445ac7895105739a20ace7f7841d99c6fb7d3fda9d1d8b9d04`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb5b7cf70ded65be8bdd0cca34e03527f014cd8e16b9f65ad614d70a4387d02`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.2 MB (1210524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e2537d23fd6823f335c8be0a6b4652bf47b8a50ac45aff54555ece99a7a75d`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 118.0 KB (117967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382afa8f1ecd0dcfe3550ec5267aa91935502e4f0fe35d6afc8eb2568dc19a42`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84229ee9c2a0af5e27ee0560b9b7981e1ff0b41f3f60b74ec5ab1467011f7ba3`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f82f4ce706b55dd8e8ac3e953cc4f0d4faa51a1f5cec8415cf6fc272e4747ab`  
		Last Modified: Tue, 30 May 2017 16:05:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:c02e6cd1683288a8774745f40415be06d3c592275747e03c07c7b8e1c430e699
```

-	Platforms:
	-	linux; amd64

### `adminer:fastcgi` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31955635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a913061a534c28d99d66333a5deadc44459d6087b8cd4afdd9cd4c916bc7fd8`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 May 2017 23:31:54 GMT
ADD file:c34582524a7c4fa2ccb67d48efaa6edacff8bc8115a26a511b2385a03f56aa8e in / 
# Thu, 25 May 2017 23:31:55 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2017 14:39:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Fri, 26 May 2017 14:39:22 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Fri, 26 May 2017 14:39:24 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Fri, 26 May 2017 14:39:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 May 2017 14:39:26 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 26 May 2017 14:49:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Fri, 26 May 2017 14:49:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:49:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 26 May 2017 14:49:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 26 May 2017 15:02:39 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 26 May 2017 15:02:39 GMT
ENV PHP_VERSION=7.0.19
# Fri, 26 May 2017 15:02:40 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.19.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.19.tar.xz.asc/from/this/mirror
# Fri, 26 May 2017 15:02:41 GMT
ENV PHP_SHA256=640e5e3377d15a6d19adce2b94a9d876eeddabdb862d154a5e347987f4225ef6 PHP_MD5=1a17e45c8be9ce28f036d884563e8ae7
# Fri, 26 May 2017 15:02:48 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Fri, 26 May 2017 15:02:49 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 26 May 2017 15:06:15 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Fri, 26 May 2017 15:06:17 GMT
COPY multi:1401feee8064a06ad514519ec870939c946ecfdf381c82a90cb2035486938ee9 in /usr/local/bin/ 
# Fri, 26 May 2017 15:06:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 May 2017 15:06:18 GMT
WORKDIR /var/www/html
# Fri, 26 May 2017 15:06:20 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 26 May 2017 15:06:21 GMT
EXPOSE 9000/tcp
# Fri, 26 May 2017 15:06:21 GMT
CMD ["php-fpm"]
# Tue, 30 May 2017 16:03:46 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 30 May 2017 16:03:50 GMT
RUN apk add --no-cache libpq
# Tue, 30 May 2017 16:04:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Tue, 30 May 2017 16:04:09 GMT
COPY multi:515cdb7e8ed0278965e56c4b579e89987c42be4b42a309c70682464e9c9451c5 in /var/www/html/ 
# Tue, 30 May 2017 16:04:10 GMT
ENV ADMINER_VERSION=4.3.1
# Tue, 30 May 2017 16:04:11 GMT
ENV ADMINER_DOWNLOAD_SHA256=71688c5db4d4e504c48c26ec2966ad85e721ef61e0377c5505cfb50b026d5491
# Tue, 30 May 2017 16:04:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd016c93bb3bb8e85ed9cf826064584012c4db83f30c4948d701250e29a6d953
# Tue, 30 May 2017 16:04:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION-en.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 30 May 2017 16:04:15 GMT
COPY file:9bd2234bd2d16bb29c56ca41cb797761bce45cf629f48bc911f36b2c284cde46 in /usr/local/bin/ 
# Tue, 30 May 2017 16:04:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 30 May 2017 16:04:17 GMT
USER [adminer]
# Tue, 30 May 2017 16:04:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:486a8e636d6250a74d15cdb3582f4dd198271a80118f5a2f59de3d9cd8433611`  
		Last Modified: Thu, 25 May 2017 23:35:56 GMT  
		Size: 2.4 MB (2383064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41812ec2cb654115fad6678a89cace781f0cf539e2316efe2005438e428db6df`  
		Last Modified: Fri, 26 May 2017 15:25:24 GMT  
		Size: 1.1 MB (1081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095add676785194f9c4d180e50bdeb9eac882406547f0428cf26be373adff6b`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286dbb174b8d2bb248dcfc542bb4edd08165b8fd2d01f9fbf7ff36c68c8ee43c`  
		Last Modified: Fri, 26 May 2017 15:25:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87959aa873124b10b69066e4668db64c75fd8a16dc8118e3de8878cf99065d7`  
		Last Modified: Fri, 26 May 2017 15:38:57 GMT  
		Size: 12.8 MB (12769026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad35336e465e1720333b4d90a4b3d30c925109c9fd0e216d42950e5cd8ce9928`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 484.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb46f99aeee7bf390bf8c3b37e081fc7b0973f5178fd00f1838617536b96c50`  
		Last Modified: Fri, 26 May 2017 15:38:58 GMT  
		Size: 14.1 MB (14059644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be0078492bc2657aa9b7d5430827c67882fe5fa8f298d7cf3894ee2dd1d13d0`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba81a0e17b2cdca00e27acdddaa4a9d83e3868804e58d42f3cd4fbddba828691`  
		Last Modified: Fri, 26 May 2017 15:38:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc5954361df3c3b3f47844c62f38babad709b56d618cca32fc80cb84109bb0b`  
		Last Modified: Fri, 26 May 2017 15:38:56 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aef245e79767c445ac7895105739a20ace7f7841d99c6fb7d3fda9d1d8b9d04`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb5b7cf70ded65be8bdd0cca34e03527f014cd8e16b9f65ad614d70a4387d02`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.2 MB (1210524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e2537d23fd6823f335c8be0a6b4652bf47b8a50ac45aff54555ece99a7a75d`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 118.0 KB (117967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382afa8f1ecd0dcfe3550ec5267aa91935502e4f0fe35d6afc8eb2568dc19a42`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84229ee9c2a0af5e27ee0560b9b7981e1ff0b41f3f60b74ec5ab1467011f7ba3`  
		Last Modified: Tue, 30 May 2017 16:05:41 GMT  
		Size: 319.1 KB (319102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f82f4ce706b55dd8e8ac3e953cc4f0d4faa51a1f5cec8415cf6fc272e4747ab`  
		Last Modified: Tue, 30 May 2017 16:05:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
