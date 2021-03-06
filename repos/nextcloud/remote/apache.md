## `nextcloud:apache`

```console
$ docker pull nextcloud@sha256:edd044328819a141d295a248632e5c0afc67f5a0d9f6c752f8de7ec622aaca3a
```

-	Platforms:
	-	linux; amd64

### `nextcloud:apache` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238499636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0d70f314ea679ac1a244c061f72f5f6d1fa09cabbace3a6187ef13aa4cc529`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 22:55:44 GMT
ENV PHPIZE_DEPS=autoconf 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Mar 2017 22:56:13 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Tue, 21 Mar 2017 22:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Mar 2017 22:56:15 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Tue, 21 Mar 2017 22:59:49 GMT
RUN apt-get update && apt-get install -y apache2-bin apache2.2-common --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 22:59:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Mar 2017 22:59:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Mar 2017 22:59:50 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Tue, 21 Mar 2017 22:59:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Mar 2017 22:59:52 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Tue, 21 Mar 2017 22:59:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Mar 2017 22:59:54 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 21 Mar 2017 22:59:54 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Tue, 21 Mar 2017 22:59:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 21 Mar 2017 22:59:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 21 Mar 2017 22:59:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Tue, 21 Mar 2017 23:13:11 GMT
ENV GPG_KEYS=A917B1ECDA84AEC2B568FED6F50ABC807BD5DCD0 528995BFEDFBA7191D46839EF9BA0ADA31CBD89E
# Tue, 21 Mar 2017 23:13:12 GMT
ENV PHP_VERSION=7.1.3
# Tue, 21 Mar 2017 23:13:12 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.1.3.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.1.3.tar.xz.asc/from/this/mirror
# Tue, 21 Mar 2017 23:13:12 GMT
ENV PHP_SHA256=e4887c2634778e37fd962fbdf5c4a7d32cd708482fe07b448804625570cb0bb0 PHP_MD5=d604d688be17f4a05b99dbb7fb9581f4
# Tue, 21 Mar 2017 23:13:21 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove $fetchDeps
# Tue, 21 Mar 2017 23:13:21 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Tue, 21 Mar 2017 23:15:42 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& ./configure 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps
# Tue, 21 Mar 2017 23:15:43 GMT
COPY multi:2b7e23dbf0e975ef1ec1f186511e2789ab94e8c8734ca9fa8419c893f7357d6c in /usr/local/bin/ 
# Tue, 21 Mar 2017 23:15:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Mar 2017 23:15:44 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Tue, 21 Mar 2017 23:15:45 GMT
WORKDIR /var/www/html
# Tue, 21 Mar 2017 23:15:45 GMT
EXPOSE 80/tcp
# Tue, 21 Mar 2017 23:15:46 GMT
CMD ["apache2-foreground"]
# Wed, 22 Mar 2017 21:48:53 GMT
RUN apt-get update && apt-get install -y   bzip2   libcurl4-openssl-dev   libfreetype6-dev   libicu-dev   libjpeg-dev   libldap2-dev   libmcrypt-dev   libmemcached-dev   libpng12-dev   libpq-dev   libxml2-dev   && rm -rf /var/lib/apt/lists/*
# Wed, 22 Mar 2017 21:50:51 GMT
RUN docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr   && docker-php-ext-configure ldap --with-libdir=lib/x86_64-linux-gnu   && docker-php-ext-install gd exif intl mbstring mcrypt ldap mysqli opcache pdo_mysql pdo_pgsql pgsql zip
# Wed, 22 Mar 2017 21:50:53 GMT
RUN {     echo 'opcache.memory_consumption=128';     echo 'opcache.interned_strings_buffer=8';     echo 'opcache.max_accelerated_files=4000';     echo 'opcache.revalidate_freq=60';     echo 'opcache.fast_shutdown=1';     echo 'opcache.enable_cli=1';   } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 22 Mar 2017 21:50:54 GMT
RUN a2enmod rewrite
# Wed, 22 Mar 2017 21:51:21 GMT
RUN set -ex  && pecl install APCu-5.1.8  && pecl install memcached-3.0.2  && pecl install redis-3.1.1  && docker-php-ext-enable apcu redis memcached
# Wed, 22 Mar 2017 21:51:22 GMT
RUN a2enmod rewrite
# Wed, 22 Mar 2017 21:51:22 GMT
ENV NEXTCLOUD_VERSION=11.0.2
# Wed, 22 Mar 2017 21:51:23 GMT
VOLUME [/var/www/html]
# Wed, 22 Mar 2017 21:51:38 GMT
RUN curl -fsSL -o nextcloud.tar.bz2     "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2"  && curl -fsSL -o nextcloud.tar.bz2.asc     "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A  && gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2  && rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc  && tar -xjf nextcloud.tar.bz2 -C /usr/src/  && rm nextcloud.tar.bz2
# Wed, 22 Mar 2017 21:51:39 GMT
COPY file:c7f1f4a0f998c8c0da4d04648ceaf6cc3023bcb1ce16653971a83aa733746efc in /entrypoint.sh 
# Wed, 22 Mar 2017 21:51:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Mar 2017 21:51:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fe8fbc743a3c84e20d43e0182ec42fa98d63745f81abae17307558e542e3cf`  
		Last Modified: Wed, 22 Mar 2017 23:53:42 GMT  
		Size: 77.7 MB (77681981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d1a8d304ab1e86f676f962451a74e23764dcc6c68021f0ad77f3ace17f4c5f`  
		Last Modified: Wed, 22 Mar 2017 23:53:17 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf3547d9b739f2f04846520e0d804358ac8bb09d8fe087b9b22776466591147`  
		Last Modified: Wed, 22 Mar 2017 23:53:17 GMT  
		Size: 2.9 MB (2858770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004db2760ff505c8cb29d8b6e0c3807eb12a9c4f75dfe899ec12330443ae4c0`  
		Last Modified: Wed, 22 Mar 2017 23:53:16 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e2d66a547e35efdd6f59963e788cec2b96be1c0a95952c5760430c405c6466`  
		Last Modified: Wed, 22 Mar 2017 23:53:15 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfaa62c234a9168aa1e9a43ad031162a50b71dc0ebff0a48c05b33497a93d51`  
		Last Modified: Wed, 22 Mar 2017 23:53:14 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce8807f4d1a92b890a7878d0f6aadef4fe718b2d1a07b9c98ed585e87dc2e9`  
		Last Modified: Wed, 22 Mar 2017 23:53:13 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f8d35ca798303c3a272c8b66590122bd5431a807f752815bcf74c7240199e7`  
		Last Modified: Thu, 23 Mar 2017 17:42:52 GMT  
		Size: 12.9 MB (12919540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5594b4d2a52081bd08983b536696b3a40f6784595493054493ff4a19370ce90`  
		Last Modified: Thu, 23 Mar 2017 17:42:48 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f1cbd038cf08a7f67c568548dcc899bc4770bdae242a2e64978da79367e9a2`  
		Last Modified: Thu, 23 Mar 2017 17:42:55 GMT  
		Size: 13.7 MB (13686268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739656e85cbe1e91b6cc9eaa3066bcc7f78a15709d41bbe40a45991638b4475`  
		Last Modified: Thu, 23 Mar 2017 17:42:47 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6a5f245a1a29065cc5f5aeac6c8d77ee5edf7083a05d2d36ea0fc344cb303`  
		Last Modified: Thu, 23 Mar 2017 17:42:45 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bd38a02a3d6a15a7542838df7bd13cae3379d3911ce25e889175912a790740`  
		Last Modified: Thu, 23 Mar 2017 23:01:01 GMT  
		Size: 34.3 MB (34342773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c065cd1dd5a294e9f31a8d8fa0992affb96aee048fb6936f20e68a18987485`  
		Last Modified: Thu, 23 Mar 2017 23:00:49 GMT  
		Size: 1.9 MB (1865593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb2b825c262332634a4247b571557dab5d77e3ac4e0e6d6493831cc1d0a86e5`  
		Last Modified: Thu, 23 Mar 2017 23:00:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8a2e01225fd1008c49a1fd63fd552b166333b0c2e7089f95e61faaa8f1489b`  
		Last Modified: Thu, 23 Mar 2017 23:00:46 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1fb0a958c2a057a8320e2e601f84fcee8faf3db5852adce810d8e24d47690c`  
		Last Modified: Thu, 23 Mar 2017 23:00:47 GMT  
		Size: 1.3 MB (1313078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c3b8a9a94f980d909f8ef6a4e9e252a4d3e75f6ed3b01acdcefca9d05efab8`  
		Last Modified: Thu, 23 Mar 2017 23:01:05 GMT  
		Size: 42.4 MB (42386329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ca1e5ac8a770e05f1bf4ac0facda884ef18eee2c2058b6168dee3da440321e`  
		Last Modified: Thu, 23 Mar 2017 23:00:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
