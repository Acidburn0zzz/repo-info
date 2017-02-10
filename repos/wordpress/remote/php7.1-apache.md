## `wordpress:php7.1-apache`

```console
$ docker pull wordpress@sha256:09f5ad558530a035aed30d9bafad2ca5b0c336a0d6de77f7968a5ec213ad8d1f
```

-	Platforms:
	-	linux; amd64

### `wordpress:php7.1-apache` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168382328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3aca02ada3458862cf32147caa9cb9871a6531183d186090e858487aab47c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 18:54:13 GMT
ENV PHPIZE_DEPS=autoconf 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Jan 2017 18:54:39 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Tue, 17 Jan 2017 18:54:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Jan 2017 18:54:40 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Tue, 17 Jan 2017 18:58:08 GMT
RUN apt-get update && apt-get install -y apache2-bin apache2.2-common --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 18:58:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Jan 2017 18:58:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Jan 2017 18:58:09 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Tue, 17 Jan 2017 18:58:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 17 Jan 2017 18:58:11 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Tue, 17 Jan 2017 18:58:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 17 Jan 2017 18:58:12 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 17 Jan 2017 18:58:13 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Tue, 17 Jan 2017 18:58:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 17 Jan 2017 18:58:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 17 Jan 2017 18:58:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Tue, 24 Jan 2017 18:31:37 GMT
ENV GPG_KEYS=A917B1ECDA84AEC2B568FED6F50ABC807BD5DCD0 528995BFEDFBA7191D46839EF9BA0ADA31CBD89E
# Tue, 24 Jan 2017 18:31:37 GMT
ENV PHP_VERSION=7.1.1
# Tue, 24 Jan 2017 18:31:38 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.1.1.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.1.1.tar.xz.asc/from/this/mirror
# Tue, 24 Jan 2017 18:31:38 GMT
ENV PHP_SHA256=b3565b0c1441064eba204821608df1ec7367abff881286898d900c2c2a5ffe70 PHP_MD5=65eef256f6e7104a05361939f5e23ada
# Tue, 24 Jan 2017 18:31:47 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove $fetchDeps
# Tue, 24 Jan 2017 18:31:48 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Tue, 24 Jan 2017 18:34:09 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& ./configure 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps
# Tue, 24 Jan 2017 18:34:10 GMT
COPY multi:2b7e23dbf0e975ef1ec1f186511e2789ab94e8c8734ca9fa8419c893f7357d6c in /usr/local/bin/ 
# Tue, 24 Jan 2017 18:34:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Jan 2017 23:15:10 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 27 Jan 2017 23:15:11 GMT
WORKDIR /var/www/html
# Fri, 27 Jan 2017 23:15:11 GMT
EXPOSE 80/tcp
# Fri, 27 Jan 2017 23:15:12 GMT
CMD ["apache2-foreground"]
# Fri, 27 Jan 2017 23:57:47 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		libjpeg-dev 		libpng12-dev 	; 	rm -rf /var/lib/apt/lists/*; 		docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr; 	docker-php-ext-install gd mysqli opcache
# Fri, 27 Jan 2017 23:57:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 27 Jan 2017 23:57:49 GMT
RUN a2enmod rewrite expires
# Fri, 27 Jan 2017 23:57:50 GMT
VOLUME [/var/www/html]
# Fri, 27 Jan 2017 23:57:50 GMT
ENV WORDPRESS_VERSION=4.7.2
# Fri, 27 Jan 2017 23:57:51 GMT
ENV WORDPRESS_SHA1=7b687f1af589c337124e6247229af209ec1d52c3
# Fri, 27 Jan 2017 23:57:53 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 10 Feb 2017 01:04:14 GMT
COPY file:b5c332f80307d4248d07b035890c0ea453c1157d9e1732225f83f63d851392b5 in /usr/local/bin/ 
# Fri, 10 Feb 2017 01:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2017 01:04:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568dce68541a55fd0fb33021383e3921145275a1f87d925f37f1246b682baf0b`  
		Last Modified: Wed, 18 Jan 2017 03:05:48 GMT  
		Size: 77.6 MB (77606810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a832068e64c0a907e1585adac98802eb69cf9fc878ba00941d59e7be57c4b93`  
		Last Modified: Wed, 18 Jan 2017 03:05:21 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0f3d176a5bf080e41340e04575cdeece539b71cd0405812474a03151cdf73f`  
		Last Modified: Wed, 18 Jan 2017 03:05:22 GMT  
		Size: 2.8 MB (2849173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cc248a5690169dac19b598857e4ecd4a6421a5c21eb699066d5006cf27834b`  
		Last Modified: Wed, 18 Jan 2017 03:05:20 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff565538ee684ae5f9d8e1c0c152bfabefa1f94202054df27edc82410555c74`  
		Last Modified: Wed, 18 Jan 2017 03:05:19 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1077228581cd19b5dc570b5831269295dd388feba6e783bd93396b0a825caa`  
		Last Modified: Wed, 18 Jan 2017 03:05:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57359f144a1928936e5079e40f75cf1e00f8eb81b3bf2045fbdbc02e9f1b78e5`  
		Last Modified: Wed, 18 Jan 2017 03:05:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02192cdb2b85b8e791facf01c6d856479e4f17deed3f1496b26f5ad80ab9b254`  
		Last Modified: Tue, 24 Jan 2017 19:45:54 GMT  
		Size: 12.9 MB (12896249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438a4f02ffc78eb4a0841f27eb20b201db9d775e2e5f87d9892ea822534246d7`  
		Last Modified: Tue, 24 Jan 2017 19:45:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf3c50aa40727b1bf4c8645dd6976963e6f3a0cd4870695613574604a1f5c17`  
		Last Modified: Tue, 24 Jan 2017 19:45:57 GMT  
		Size: 13.6 MB (13601582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7291edaaf617548d594d8855e35a9fb3c657f79ebe997aa34b2879c87502bdf4`  
		Last Modified: Tue, 24 Jan 2017 19:45:52 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac60b9af575c65836748f9ed03ccb909db120bb9b848ff3bbf217eb6151c817`  
		Last Modified: Fri, 27 Jan 2017 23:18:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93aa47e99b206a33b9203eb13c69ecf8f0fccba1635cdd22b6c31c48cbf2828`  
		Last Modified: Sat, 28 Jan 2017 00:11:17 GMT  
		Size: 2.2 MB (2230205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10038fb65ac864a1c857f2c467e37f64092f95dce38c73d63f250b5eb9eb44d0`  
		Last Modified: Sat, 28 Jan 2017 00:11:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90cefbd447361300cc244e8177fad41d44152ef9911ab8bb3d167bca741c01b`  
		Last Modified: Sat, 28 Jan 2017 00:11:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a44b2583d740848e4bc3da12cf4170470831bed3cfa81d77486d68ebe36985c`  
		Last Modified: Sat, 28 Jan 2017 00:11:19 GMT  
		Size: 7.8 MB (7827361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df522d63dc2e265d2ca6707dfaec8f7a4440ebae02b65dc3b7541653be3d7fa`  
		Last Modified: Fri, 10 Feb 2017 01:20:59 GMT  
		Size: 3.1 KB (3133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
