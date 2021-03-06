<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `plone`

-	[`plone:5.0.7`](#plone507)
-	[`plone:5.0`](#plone50)
-	[`plone:5`](#plone5)
-	[`plone:latest`](#plonelatest)
-	[`plone:4.3.12`](#plone4312)
-	[`plone:4.3`](#plone43)
-	[`plone:4`](#plone4)

## `plone:5.0.7`

```console
$ docker pull plone@sha256:cb1212880951f7efd243a066ff6054354f4e1c14ed8748dedd1419de03fdca60
```

-	Platforms:
	-	linux; amd64

### `plone:5.0.7` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139709622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8343067e71b5daea9da925a78b42a03c7d23a8a712c91e305e16467bcf6143f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 18:33:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 18:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 21 Mar 2017 23:42:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 23:42:40 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 21 Mar 2017 23:42:40 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 21 Mar 2017 23:42:41 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 21 Mar 2017 23:44:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 21 Mar 2017 23:44:39 GMT
CMD ["python2"]
# Wed, 22 Mar 2017 22:35:03 GMT
MAINTAINER "Plone Community" http://community.plone.org
# Wed, 22 Mar 2017 22:35:05 GMT
RUN useradd --system -U -u 500 plone  && mkdir -p /plone /data/filestorage /data/blobstorage  && chown -R plone:plone /plone /data
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_MAJOR=5.0
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_VERSION=5.0.7
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_MD5=347e787d10a6a02d8156ed8c05effcdb
# Wed, 22 Mar 2017 22:39:16 GMT
LABEL plone.version=5.0.7
# Wed, 22 Mar 2017 22:39:16 GMT
LABEL os=debian os.version=8
# Wed, 22 Mar 2017 22:42:52 GMT
RUN buildDeps="curl sudo python-setuptools python-dev build-essential libssl-dev libxml2-dev libxslt1-dev libbz2-dev libjpeg62-turbo-dev"  && runDeps="libxml2 libxslt1.1 libjpeg62 rsync"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && curl -o Plone.tgz -SL https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && ./Plone-$PLONE_VERSION-UnifiedInstaller/install.sh       --password=admin       --daemon-user=plone       --owner=plone       --group=plone       --target=/plone       --instance=instance       --var=/data       none  && cd /plone/instance  && sed -i 's/parts =/parts =\n    zeoserver/g' buildout.cfg  && echo '\n[zeoserver]\n<= zeoserver_base\nrecipe = plone.recipe.zeoserver' >> buildout.cfg  && sudo -u plone bin/buildout  && chown -R plone:plone /plone /data  && rm -rf /Plone*  && SUDO_FORCE_REMOVE=yes apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/*  && find /plone \( -type f -a -name '*.pyc' -o -name '*.pyo' \) -exec rm -rf '{}' +
# Wed, 22 Mar 2017 22:42:53 GMT
VOLUME [/data]
# Wed, 22 Mar 2017 22:42:54 GMT
COPY multi:df870708d456e9785c9b887f2caba9a08a7b0644a7384dc8873e8ff7b1eed3b4 in / 
# Wed, 22 Mar 2017 22:42:54 GMT
EXPOSE 8080/tcp
# Wed, 22 Mar 2017 22:42:55 GMT
USER [plone]
# Wed, 22 Mar 2017 22:42:56 GMT
WORKDIR /plone/instance
# Wed, 22 Mar 2017 22:42:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Mar 2017 22:42:57 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2632a1ec5c592db4aa7bc3ccd6de4faea0f7792e686792e4acd54b8486f60`  
		Last Modified: Thu, 23 Mar 2017 17:02:36 GMT  
		Size: 3.4 MB (3415620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e707e000d50cb9ff7196cba36993274734b64a712732e5737df9d6e71f43d8`  
		Last Modified: Thu, 23 Mar 2017 17:02:42 GMT  
		Size: 16.5 MB (16471980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff0ff49bd6b490cb19e7a8afad2337a0598b0f6746b36f600e4d9ef52bfd882`  
		Last Modified: Thu, 23 Mar 2017 17:43:04 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61c8b38ba0afda6decc218ebd4273c29493321e80d258b04e7f32ef1289bf9b`  
		Last Modified: Thu, 23 Mar 2017 17:45:53 GMT  
		Size: 68.4 MB (68379359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faceae38755043c7fc0427691173b2837aab0e77dc0cb1270cc3570d50cf137`  
		Last Modified: Thu, 23 Mar 2017 17:45:16 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `plone:5.0`

```console
$ docker pull plone@sha256:cb1212880951f7efd243a066ff6054354f4e1c14ed8748dedd1419de03fdca60
```

-	Platforms:
	-	linux; amd64

### `plone:5.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139709622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8343067e71b5daea9da925a78b42a03c7d23a8a712c91e305e16467bcf6143f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 18:33:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 18:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 21 Mar 2017 23:42:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 23:42:40 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 21 Mar 2017 23:42:40 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 21 Mar 2017 23:42:41 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 21 Mar 2017 23:44:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 21 Mar 2017 23:44:39 GMT
CMD ["python2"]
# Wed, 22 Mar 2017 22:35:03 GMT
MAINTAINER "Plone Community" http://community.plone.org
# Wed, 22 Mar 2017 22:35:05 GMT
RUN useradd --system -U -u 500 plone  && mkdir -p /plone /data/filestorage /data/blobstorage  && chown -R plone:plone /plone /data
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_MAJOR=5.0
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_VERSION=5.0.7
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_MD5=347e787d10a6a02d8156ed8c05effcdb
# Wed, 22 Mar 2017 22:39:16 GMT
LABEL plone.version=5.0.7
# Wed, 22 Mar 2017 22:39:16 GMT
LABEL os=debian os.version=8
# Wed, 22 Mar 2017 22:42:52 GMT
RUN buildDeps="curl sudo python-setuptools python-dev build-essential libssl-dev libxml2-dev libxslt1-dev libbz2-dev libjpeg62-turbo-dev"  && runDeps="libxml2 libxslt1.1 libjpeg62 rsync"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && curl -o Plone.tgz -SL https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && ./Plone-$PLONE_VERSION-UnifiedInstaller/install.sh       --password=admin       --daemon-user=plone       --owner=plone       --group=plone       --target=/plone       --instance=instance       --var=/data       none  && cd /plone/instance  && sed -i 's/parts =/parts =\n    zeoserver/g' buildout.cfg  && echo '\n[zeoserver]\n<= zeoserver_base\nrecipe = plone.recipe.zeoserver' >> buildout.cfg  && sudo -u plone bin/buildout  && chown -R plone:plone /plone /data  && rm -rf /Plone*  && SUDO_FORCE_REMOVE=yes apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/*  && find /plone \( -type f -a -name '*.pyc' -o -name '*.pyo' \) -exec rm -rf '{}' +
# Wed, 22 Mar 2017 22:42:53 GMT
VOLUME [/data]
# Wed, 22 Mar 2017 22:42:54 GMT
COPY multi:df870708d456e9785c9b887f2caba9a08a7b0644a7384dc8873e8ff7b1eed3b4 in / 
# Wed, 22 Mar 2017 22:42:54 GMT
EXPOSE 8080/tcp
# Wed, 22 Mar 2017 22:42:55 GMT
USER [plone]
# Wed, 22 Mar 2017 22:42:56 GMT
WORKDIR /plone/instance
# Wed, 22 Mar 2017 22:42:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Mar 2017 22:42:57 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2632a1ec5c592db4aa7bc3ccd6de4faea0f7792e686792e4acd54b8486f60`  
		Last Modified: Thu, 23 Mar 2017 17:02:36 GMT  
		Size: 3.4 MB (3415620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e707e000d50cb9ff7196cba36993274734b64a712732e5737df9d6e71f43d8`  
		Last Modified: Thu, 23 Mar 2017 17:02:42 GMT  
		Size: 16.5 MB (16471980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff0ff49bd6b490cb19e7a8afad2337a0598b0f6746b36f600e4d9ef52bfd882`  
		Last Modified: Thu, 23 Mar 2017 17:43:04 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61c8b38ba0afda6decc218ebd4273c29493321e80d258b04e7f32ef1289bf9b`  
		Last Modified: Thu, 23 Mar 2017 17:45:53 GMT  
		Size: 68.4 MB (68379359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faceae38755043c7fc0427691173b2837aab0e77dc0cb1270cc3570d50cf137`  
		Last Modified: Thu, 23 Mar 2017 17:45:16 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `plone:5`

```console
$ docker pull plone@sha256:cb1212880951f7efd243a066ff6054354f4e1c14ed8748dedd1419de03fdca60
```

-	Platforms:
	-	linux; amd64

### `plone:5` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139709622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8343067e71b5daea9da925a78b42a03c7d23a8a712c91e305e16467bcf6143f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 18:33:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 18:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 21 Mar 2017 23:42:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 23:42:40 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 21 Mar 2017 23:42:40 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 21 Mar 2017 23:42:41 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 21 Mar 2017 23:44:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 21 Mar 2017 23:44:39 GMT
CMD ["python2"]
# Wed, 22 Mar 2017 22:35:03 GMT
MAINTAINER "Plone Community" http://community.plone.org
# Wed, 22 Mar 2017 22:35:05 GMT
RUN useradd --system -U -u 500 plone  && mkdir -p /plone /data/filestorage /data/blobstorage  && chown -R plone:plone /plone /data
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_MAJOR=5.0
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_VERSION=5.0.7
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_MD5=347e787d10a6a02d8156ed8c05effcdb
# Wed, 22 Mar 2017 22:39:16 GMT
LABEL plone.version=5.0.7
# Wed, 22 Mar 2017 22:39:16 GMT
LABEL os=debian os.version=8
# Wed, 22 Mar 2017 22:42:52 GMT
RUN buildDeps="curl sudo python-setuptools python-dev build-essential libssl-dev libxml2-dev libxslt1-dev libbz2-dev libjpeg62-turbo-dev"  && runDeps="libxml2 libxslt1.1 libjpeg62 rsync"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && curl -o Plone.tgz -SL https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && ./Plone-$PLONE_VERSION-UnifiedInstaller/install.sh       --password=admin       --daemon-user=plone       --owner=plone       --group=plone       --target=/plone       --instance=instance       --var=/data       none  && cd /plone/instance  && sed -i 's/parts =/parts =\n    zeoserver/g' buildout.cfg  && echo '\n[zeoserver]\n<= zeoserver_base\nrecipe = plone.recipe.zeoserver' >> buildout.cfg  && sudo -u plone bin/buildout  && chown -R plone:plone /plone /data  && rm -rf /Plone*  && SUDO_FORCE_REMOVE=yes apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/*  && find /plone \( -type f -a -name '*.pyc' -o -name '*.pyo' \) -exec rm -rf '{}' +
# Wed, 22 Mar 2017 22:42:53 GMT
VOLUME [/data]
# Wed, 22 Mar 2017 22:42:54 GMT
COPY multi:df870708d456e9785c9b887f2caba9a08a7b0644a7384dc8873e8ff7b1eed3b4 in / 
# Wed, 22 Mar 2017 22:42:54 GMT
EXPOSE 8080/tcp
# Wed, 22 Mar 2017 22:42:55 GMT
USER [plone]
# Wed, 22 Mar 2017 22:42:56 GMT
WORKDIR /plone/instance
# Wed, 22 Mar 2017 22:42:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Mar 2017 22:42:57 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2632a1ec5c592db4aa7bc3ccd6de4faea0f7792e686792e4acd54b8486f60`  
		Last Modified: Thu, 23 Mar 2017 17:02:36 GMT  
		Size: 3.4 MB (3415620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e707e000d50cb9ff7196cba36993274734b64a712732e5737df9d6e71f43d8`  
		Last Modified: Thu, 23 Mar 2017 17:02:42 GMT  
		Size: 16.5 MB (16471980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff0ff49bd6b490cb19e7a8afad2337a0598b0f6746b36f600e4d9ef52bfd882`  
		Last Modified: Thu, 23 Mar 2017 17:43:04 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61c8b38ba0afda6decc218ebd4273c29493321e80d258b04e7f32ef1289bf9b`  
		Last Modified: Thu, 23 Mar 2017 17:45:53 GMT  
		Size: 68.4 MB (68379359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faceae38755043c7fc0427691173b2837aab0e77dc0cb1270cc3570d50cf137`  
		Last Modified: Thu, 23 Mar 2017 17:45:16 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `plone:latest`

```console
$ docker pull plone@sha256:cb1212880951f7efd243a066ff6054354f4e1c14ed8748dedd1419de03fdca60
```

-	Platforms:
	-	linux; amd64

### `plone:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139709622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8343067e71b5daea9da925a78b42a03c7d23a8a712c91e305e16467bcf6143f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 18:33:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 18:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 21 Mar 2017 23:42:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 23:42:40 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 21 Mar 2017 23:42:40 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 21 Mar 2017 23:42:41 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 21 Mar 2017 23:44:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 21 Mar 2017 23:44:39 GMT
CMD ["python2"]
# Wed, 22 Mar 2017 22:35:03 GMT
MAINTAINER "Plone Community" http://community.plone.org
# Wed, 22 Mar 2017 22:35:05 GMT
RUN useradd --system -U -u 500 plone  && mkdir -p /plone /data/filestorage /data/blobstorage  && chown -R plone:plone /plone /data
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_MAJOR=5.0
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_VERSION=5.0.7
# Wed, 22 Mar 2017 22:39:15 GMT
ENV PLONE_MD5=347e787d10a6a02d8156ed8c05effcdb
# Wed, 22 Mar 2017 22:39:16 GMT
LABEL plone.version=5.0.7
# Wed, 22 Mar 2017 22:39:16 GMT
LABEL os=debian os.version=8
# Wed, 22 Mar 2017 22:42:52 GMT
RUN buildDeps="curl sudo python-setuptools python-dev build-essential libssl-dev libxml2-dev libxslt1-dev libbz2-dev libjpeg62-turbo-dev"  && runDeps="libxml2 libxslt1.1 libjpeg62 rsync"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && curl -o Plone.tgz -SL https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && ./Plone-$PLONE_VERSION-UnifiedInstaller/install.sh       --password=admin       --daemon-user=plone       --owner=plone       --group=plone       --target=/plone       --instance=instance       --var=/data       none  && cd /plone/instance  && sed -i 's/parts =/parts =\n    zeoserver/g' buildout.cfg  && echo '\n[zeoserver]\n<= zeoserver_base\nrecipe = plone.recipe.zeoserver' >> buildout.cfg  && sudo -u plone bin/buildout  && chown -R plone:plone /plone /data  && rm -rf /Plone*  && SUDO_FORCE_REMOVE=yes apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/*  && find /plone \( -type f -a -name '*.pyc' -o -name '*.pyo' \) -exec rm -rf '{}' +
# Wed, 22 Mar 2017 22:42:53 GMT
VOLUME [/data]
# Wed, 22 Mar 2017 22:42:54 GMT
COPY multi:df870708d456e9785c9b887f2caba9a08a7b0644a7384dc8873e8ff7b1eed3b4 in / 
# Wed, 22 Mar 2017 22:42:54 GMT
EXPOSE 8080/tcp
# Wed, 22 Mar 2017 22:42:55 GMT
USER [plone]
# Wed, 22 Mar 2017 22:42:56 GMT
WORKDIR /plone/instance
# Wed, 22 Mar 2017 22:42:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Mar 2017 22:42:57 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2632a1ec5c592db4aa7bc3ccd6de4faea0f7792e686792e4acd54b8486f60`  
		Last Modified: Thu, 23 Mar 2017 17:02:36 GMT  
		Size: 3.4 MB (3415620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e707e000d50cb9ff7196cba36993274734b64a712732e5737df9d6e71f43d8`  
		Last Modified: Thu, 23 Mar 2017 17:02:42 GMT  
		Size: 16.5 MB (16471980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff0ff49bd6b490cb19e7a8afad2337a0598b0f6746b36f600e4d9ef52bfd882`  
		Last Modified: Thu, 23 Mar 2017 17:43:04 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61c8b38ba0afda6decc218ebd4273c29493321e80d258b04e7f32ef1289bf9b`  
		Last Modified: Thu, 23 Mar 2017 17:45:53 GMT  
		Size: 68.4 MB (68379359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faceae38755043c7fc0427691173b2837aab0e77dc0cb1270cc3570d50cf137`  
		Last Modified: Thu, 23 Mar 2017 17:45:16 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `plone:4.3.12`

```console
$ docker pull plone@sha256:bb173c0d524fdffff1f0d40fb578494289f9ca25117cca322dadbf614d7c25a6
```

-	Platforms:
	-	linux; amd64

### `plone:4.3.12` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115373445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356d1ebe0b343dff13aae4823c71bd25e8832b72cbc9e901295ac67b6dd22b4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 18:33:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 18:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 21 Mar 2017 23:42:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 23:42:40 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 21 Mar 2017 23:42:40 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 21 Mar 2017 23:42:41 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 21 Mar 2017 23:44:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 21 Mar 2017 23:44:39 GMT
CMD ["python2"]
# Wed, 22 Mar 2017 22:35:03 GMT
MAINTAINER "Plone Community" http://community.plone.org
# Wed, 22 Mar 2017 22:35:05 GMT
RUN useradd --system -U -u 500 plone  && mkdir -p /plone /data/filestorage /data/blobstorage  && chown -R plone:plone /plone /data
# Wed, 22 Mar 2017 22:35:05 GMT
ENV PLONE_MAJOR=4.3
# Wed, 22 Mar 2017 22:35:05 GMT
ENV PLONE_VERSION=4.3.12
# Wed, 22 Mar 2017 22:35:06 GMT
ENV PLONE_MD5=62291e00e1b86b8794772e6841a29570
# Wed, 22 Mar 2017 22:35:06 GMT
LABEL plone.version=4.3.12
# Wed, 22 Mar 2017 22:35:06 GMT
LABEL os=debian os.version=8
# Wed, 22 Mar 2017 22:39:09 GMT
RUN buildDeps="curl sudo python-setuptools python-dev build-essential libssl-dev libxml2-dev libxslt1-dev libbz2-dev libjpeg62-turbo-dev"  && runDeps="libxml2 libxslt1.1 libjpeg62 rsync"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && curl -o Plone.tgz -SL https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && ./Plone-$PLONE_VERSION-UnifiedInstaller/install.sh       --password=admin       --daemon-user=plone       --owner=plone       --group=plone       --target=/plone       --instance=instance       --var=/data       none  && cd /plone/instance  && sed -i 's/parts =/parts =\n    zeoserver/g' buildout.cfg  && echo '\n[zeoserver]\n<= zeoserver_base\nrecipe = plone.recipe.zeoserver' >> buildout.cfg  && sudo -u plone bin/buildout  && chown -R plone:plone /plone /data  && rm -rf /Plone*  && SUDO_FORCE_REMOVE=yes apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/*  && find /plone \( -type f -a -name '*.pyc' -o -name '*.pyo' \) -exec rm -rf '{}' +
# Wed, 22 Mar 2017 22:39:09 GMT
VOLUME [/data]
# Wed, 22 Mar 2017 22:39:10 GMT
COPY multi:df870708d456e9785c9b887f2caba9a08a7b0644a7384dc8873e8ff7b1eed3b4 in / 
# Wed, 22 Mar 2017 22:39:11 GMT
EXPOSE 8080/tcp
# Wed, 22 Mar 2017 22:39:11 GMT
USER [plone]
# Wed, 22 Mar 2017 22:39:12 GMT
WORKDIR /plone/instance
# Wed, 22 Mar 2017 22:39:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Mar 2017 22:39:13 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2632a1ec5c592db4aa7bc3ccd6de4faea0f7792e686792e4acd54b8486f60`  
		Last Modified: Thu, 23 Mar 2017 17:02:36 GMT  
		Size: 3.4 MB (3415620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e707e000d50cb9ff7196cba36993274734b64a712732e5737df9d6e71f43d8`  
		Last Modified: Thu, 23 Mar 2017 17:02:42 GMT  
		Size: 16.5 MB (16471980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff0ff49bd6b490cb19e7a8afad2337a0598b0f6746b36f600e4d9ef52bfd882`  
		Last Modified: Thu, 23 Mar 2017 17:43:04 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abddf30118acc60851ede14e261527d720b8f2f06008103fde5fd71d40e6fd6f`  
		Last Modified: Thu, 23 Mar 2017 17:43:35 GMT  
		Size: 44.0 MB (44043182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad44c4759a9d20a78dedee380095321a12873c431357c102b6d4b4c6856f2a68`  
		Last Modified: Thu, 23 Mar 2017 17:43:04 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `plone:4.3`

```console
$ docker pull plone@sha256:bb173c0d524fdffff1f0d40fb578494289f9ca25117cca322dadbf614d7c25a6
```

-	Platforms:
	-	linux; amd64

### `plone:4.3` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115373445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356d1ebe0b343dff13aae4823c71bd25e8832b72cbc9e901295ac67b6dd22b4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 18:33:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 18:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 21 Mar 2017 23:42:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 23:42:40 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 21 Mar 2017 23:42:40 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 21 Mar 2017 23:42:41 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 21 Mar 2017 23:44:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 21 Mar 2017 23:44:39 GMT
CMD ["python2"]
# Wed, 22 Mar 2017 22:35:03 GMT
MAINTAINER "Plone Community" http://community.plone.org
# Wed, 22 Mar 2017 22:35:05 GMT
RUN useradd --system -U -u 500 plone  && mkdir -p /plone /data/filestorage /data/blobstorage  && chown -R plone:plone /plone /data
# Wed, 22 Mar 2017 22:35:05 GMT
ENV PLONE_MAJOR=4.3
# Wed, 22 Mar 2017 22:35:05 GMT
ENV PLONE_VERSION=4.3.12
# Wed, 22 Mar 2017 22:35:06 GMT
ENV PLONE_MD5=62291e00e1b86b8794772e6841a29570
# Wed, 22 Mar 2017 22:35:06 GMT
LABEL plone.version=4.3.12
# Wed, 22 Mar 2017 22:35:06 GMT
LABEL os=debian os.version=8
# Wed, 22 Mar 2017 22:39:09 GMT
RUN buildDeps="curl sudo python-setuptools python-dev build-essential libssl-dev libxml2-dev libxslt1-dev libbz2-dev libjpeg62-turbo-dev"  && runDeps="libxml2 libxslt1.1 libjpeg62 rsync"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && curl -o Plone.tgz -SL https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && ./Plone-$PLONE_VERSION-UnifiedInstaller/install.sh       --password=admin       --daemon-user=plone       --owner=plone       --group=plone       --target=/plone       --instance=instance       --var=/data       none  && cd /plone/instance  && sed -i 's/parts =/parts =\n    zeoserver/g' buildout.cfg  && echo '\n[zeoserver]\n<= zeoserver_base\nrecipe = plone.recipe.zeoserver' >> buildout.cfg  && sudo -u plone bin/buildout  && chown -R plone:plone /plone /data  && rm -rf /Plone*  && SUDO_FORCE_REMOVE=yes apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/*  && find /plone \( -type f -a -name '*.pyc' -o -name '*.pyo' \) -exec rm -rf '{}' +
# Wed, 22 Mar 2017 22:39:09 GMT
VOLUME [/data]
# Wed, 22 Mar 2017 22:39:10 GMT
COPY multi:df870708d456e9785c9b887f2caba9a08a7b0644a7384dc8873e8ff7b1eed3b4 in / 
# Wed, 22 Mar 2017 22:39:11 GMT
EXPOSE 8080/tcp
# Wed, 22 Mar 2017 22:39:11 GMT
USER [plone]
# Wed, 22 Mar 2017 22:39:12 GMT
WORKDIR /plone/instance
# Wed, 22 Mar 2017 22:39:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Mar 2017 22:39:13 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2632a1ec5c592db4aa7bc3ccd6de4faea0f7792e686792e4acd54b8486f60`  
		Last Modified: Thu, 23 Mar 2017 17:02:36 GMT  
		Size: 3.4 MB (3415620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e707e000d50cb9ff7196cba36993274734b64a712732e5737df9d6e71f43d8`  
		Last Modified: Thu, 23 Mar 2017 17:02:42 GMT  
		Size: 16.5 MB (16471980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff0ff49bd6b490cb19e7a8afad2337a0598b0f6746b36f600e4d9ef52bfd882`  
		Last Modified: Thu, 23 Mar 2017 17:43:04 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abddf30118acc60851ede14e261527d720b8f2f06008103fde5fd71d40e6fd6f`  
		Last Modified: Thu, 23 Mar 2017 17:43:35 GMT  
		Size: 44.0 MB (44043182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad44c4759a9d20a78dedee380095321a12873c431357c102b6d4b4c6856f2a68`  
		Last Modified: Thu, 23 Mar 2017 17:43:04 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `plone:4`

```console
$ docker pull plone@sha256:bb173c0d524fdffff1f0d40fb578494289f9ca25117cca322dadbf614d7c25a6
```

-	Platforms:
	-	linux; amd64

### `plone:4` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115373445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356d1ebe0b343dff13aae4823c71bd25e8832b72cbc9e901295ac67b6dd22b4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 18:33:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 18:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 21 Mar 2017 23:42:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 23:42:40 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 21 Mar 2017 23:42:40 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 21 Mar 2017 23:42:41 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 21 Mar 2017 23:44:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 21 Mar 2017 23:44:39 GMT
CMD ["python2"]
# Wed, 22 Mar 2017 22:35:03 GMT
MAINTAINER "Plone Community" http://community.plone.org
# Wed, 22 Mar 2017 22:35:05 GMT
RUN useradd --system -U -u 500 plone  && mkdir -p /plone /data/filestorage /data/blobstorage  && chown -R plone:plone /plone /data
# Wed, 22 Mar 2017 22:35:05 GMT
ENV PLONE_MAJOR=4.3
# Wed, 22 Mar 2017 22:35:05 GMT
ENV PLONE_VERSION=4.3.12
# Wed, 22 Mar 2017 22:35:06 GMT
ENV PLONE_MD5=62291e00e1b86b8794772e6841a29570
# Wed, 22 Mar 2017 22:35:06 GMT
LABEL plone.version=4.3.12
# Wed, 22 Mar 2017 22:35:06 GMT
LABEL os=debian os.version=8
# Wed, 22 Mar 2017 22:39:09 GMT
RUN buildDeps="curl sudo python-setuptools python-dev build-essential libssl-dev libxml2-dev libxslt1-dev libbz2-dev libjpeg62-turbo-dev"  && runDeps="libxml2 libxslt1.1 libjpeg62 rsync"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && curl -o Plone.tgz -SL https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && ./Plone-$PLONE_VERSION-UnifiedInstaller/install.sh       --password=admin       --daemon-user=plone       --owner=plone       --group=plone       --target=/plone       --instance=instance       --var=/data       none  && cd /plone/instance  && sed -i 's/parts =/parts =\n    zeoserver/g' buildout.cfg  && echo '\n[zeoserver]\n<= zeoserver_base\nrecipe = plone.recipe.zeoserver' >> buildout.cfg  && sudo -u plone bin/buildout  && chown -R plone:plone /plone /data  && rm -rf /Plone*  && SUDO_FORCE_REMOVE=yes apt-get purge -y --auto-remove $buildDeps  && apt-get install -y --no-install-recommends $runDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/*  && find /plone \( -type f -a -name '*.pyc' -o -name '*.pyo' \) -exec rm -rf '{}' +
# Wed, 22 Mar 2017 22:39:09 GMT
VOLUME [/data]
# Wed, 22 Mar 2017 22:39:10 GMT
COPY multi:df870708d456e9785c9b887f2caba9a08a7b0644a7384dc8873e8ff7b1eed3b4 in / 
# Wed, 22 Mar 2017 22:39:11 GMT
EXPOSE 8080/tcp
# Wed, 22 Mar 2017 22:39:11 GMT
USER [plone]
# Wed, 22 Mar 2017 22:39:12 GMT
WORKDIR /plone/instance
# Wed, 22 Mar 2017 22:39:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Mar 2017 22:39:13 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2632a1ec5c592db4aa7bc3ccd6de4faea0f7792e686792e4acd54b8486f60`  
		Last Modified: Thu, 23 Mar 2017 17:02:36 GMT  
		Size: 3.4 MB (3415620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e707e000d50cb9ff7196cba36993274734b64a712732e5737df9d6e71f43d8`  
		Last Modified: Thu, 23 Mar 2017 17:02:42 GMT  
		Size: 16.5 MB (16471980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff0ff49bd6b490cb19e7a8afad2337a0598b0f6746b36f600e4d9ef52bfd882`  
		Last Modified: Thu, 23 Mar 2017 17:43:04 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abddf30118acc60851ede14e261527d720b8f2f06008103fde5fd71d40e6fd6f`  
		Last Modified: Thu, 23 Mar 2017 17:43:35 GMT  
		Size: 44.0 MB (44043182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad44c4759a9d20a78dedee380095321a12873c431357c102b6d4b4c6856f2a68`  
		Last Modified: Thu, 23 Mar 2017 17:43:04 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
