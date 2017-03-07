<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sentry`

-	[`sentry:8.13.0`](#sentry8130)
-	[`sentry:8.13`](#sentry813)
-	[`sentry:8.13.0-onbuild`](#sentry8130-onbuild)
-	[`sentry:8.13-onbuild`](#sentry813-onbuild)
-	[`sentry:8.14.1`](#sentry8141)
-	[`sentry:8.14`](#sentry814)
-	[`sentry:8`](#sentry8)
-	[`sentry:latest`](#sentrylatest)
-	[`sentry:8.14.1-onbuild`](#sentry8141-onbuild)
-	[`sentry:8.14-onbuild`](#sentry814-onbuild)
-	[`sentry:8-onbuild`](#sentry8-onbuild)
-	[`sentry:onbuild`](#sentryonbuild)

## `sentry:8.13.0`

```console
$ docker pull sentry@sha256:832cb2530279c94427c844281ee87b5b173abbd64d79d7478b7864c4ce59ac2d
```

-	Platforms:
	-	linux; amd64

### `sentry:8.13.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183784005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bd1201547892c313c11de4d7cbffd55556e1a3c7a147b885853d8dd0b230a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 17:36:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2016 17:36:48 GMT
ENV LANG=C.UTF-8
# Wed, 14 Dec 2016 17:38:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 17:38:06 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Wed, 14 Dec 2016 17:38:07 GMT
ENV PYTHON_VERSION=2.7.12
# Wed, 14 Dec 2016 17:38:07 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Wed, 14 Dec 2016 18:47:35 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Wed, 14 Dec 2016 18:47:37 GMT
CMD ["python2"]
# Wed, 14 Dec 2016 19:40:39 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Wed, 14 Dec 2016 19:41:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 19:41:01 GMT
ENV PIP_NO_CACHE_DIR=off
# Wed, 14 Dec 2016 19:41:01 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Wed, 14 Dec 2016 19:41:01 GMT
ENV GOSU_VERSION=1.10
# Wed, 14 Dec 2016 19:41:13 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Wed, 14 Dec 2016 19:41:14 GMT
ENV TINI_VERSION=v0.10.0
# Wed, 14 Dec 2016 21:52:46 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Wed, 14 Dec 2016 21:53:03 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Wed, 01 Feb 2017 23:57:41 GMT
ENV SENTRY_VERSION=8.13.0
# Wed, 01 Feb 2017 23:59:21 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget
# Wed, 01 Feb 2017 23:59:22 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Wed, 01 Feb 2017 23:59:23 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Wed, 01 Feb 2017 23:59:25 GMT
EXPOSE 9000/tcp
# Wed, 01 Feb 2017 23:59:25 GMT
VOLUME [/var/lib/sentry/files]
# Wed, 01 Feb 2017 23:59:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2017 23:59:26 GMT
CMD ["run" "web"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4665cede9d1cf30769226da349e1f7e35bf16f75d90688b9cab8569ce00ab79`  
		Last Modified: Mon, 19 Dec 2016 18:14:55 GMT  
		Size: 3.3 MB (3339260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a044686e6e0af7e1186aff3111899868a0e203d76bfde7b2e41c4c57c9d5595c`  
		Last Modified: Mon, 19 Dec 2016 18:28:51 GMT  
		Size: 16.4 MB (16364587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac23840f8b44de4114f1914c2c8f2a30f4782ec0afc3c362e708df4e3047a20`  
		Last Modified: Wed, 21 Dec 2016 20:10:42 GMT  
		Size: 4.3 KB (4344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe0b6c43af45024ee147b72bd5bd04c5433db94fd372652f470d0ec472e28c`  
		Last Modified: Wed, 21 Dec 2016 20:11:04 GMT  
		Size: 62.6 MB (62609336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acf3a0f5af58c264b5c0dddde7f67824e2232751a2117ba090332aea984cb63`  
		Last Modified: Wed, 21 Dec 2016 20:10:38 GMT  
		Size: 613.3 KB (613280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb9ce5250ca7215bd4b4865e1bb82faef11bad7c38dae7ff8b50dc68d95eaeb`  
		Last Modified: Wed, 21 Dec 2016 20:10:39 GMT  
		Size: 130.3 KB (130333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202daee25bc50a395705ba378c430517e359eb85539e74062b6135a11af4c155`  
		Last Modified: Wed, 21 Dec 2016 20:10:41 GMT  
		Size: 2.4 MB (2352903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b808d369ebf235587a12b9ce635ba74b9a160283df8e74bfa4dc5ff843c498bd`  
		Last Modified: Thu, 02 Feb 2017 00:01:03 GMT  
		Size: 47.0 MB (47001781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd94ac1498f0ebf912cff27dc3c3e89586d502ccbd169b3c9185e3343fbff4`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8002b9f3e5d213df0ef2883033db72a953c0fca5b3aa4f382bbe6208591be6e`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 3.4 KB (3400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27163c8222c16cc804a8f4a4d8910b1ce5ccf16542aebcbb0cf726be379b2e4`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4dd5fbdbbe71c108ba4eeac8aac23ef83062ed533d849ba1741ab79da512e2`  
		Last Modified: Thu, 02 Feb 2017 00:00:48 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sentry:8.13`

```console
$ docker pull sentry@sha256:832cb2530279c94427c844281ee87b5b173abbd64d79d7478b7864c4ce59ac2d
```

-	Platforms:
	-	linux; amd64

### `sentry:8.13` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183784005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bd1201547892c313c11de4d7cbffd55556e1a3c7a147b885853d8dd0b230a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 17:36:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2016 17:36:48 GMT
ENV LANG=C.UTF-8
# Wed, 14 Dec 2016 17:38:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 17:38:06 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Wed, 14 Dec 2016 17:38:07 GMT
ENV PYTHON_VERSION=2.7.12
# Wed, 14 Dec 2016 17:38:07 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Wed, 14 Dec 2016 18:47:35 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Wed, 14 Dec 2016 18:47:37 GMT
CMD ["python2"]
# Wed, 14 Dec 2016 19:40:39 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Wed, 14 Dec 2016 19:41:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 19:41:01 GMT
ENV PIP_NO_CACHE_DIR=off
# Wed, 14 Dec 2016 19:41:01 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Wed, 14 Dec 2016 19:41:01 GMT
ENV GOSU_VERSION=1.10
# Wed, 14 Dec 2016 19:41:13 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Wed, 14 Dec 2016 19:41:14 GMT
ENV TINI_VERSION=v0.10.0
# Wed, 14 Dec 2016 21:52:46 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Wed, 14 Dec 2016 21:53:03 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Wed, 01 Feb 2017 23:57:41 GMT
ENV SENTRY_VERSION=8.13.0
# Wed, 01 Feb 2017 23:59:21 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget
# Wed, 01 Feb 2017 23:59:22 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Wed, 01 Feb 2017 23:59:23 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Wed, 01 Feb 2017 23:59:25 GMT
EXPOSE 9000/tcp
# Wed, 01 Feb 2017 23:59:25 GMT
VOLUME [/var/lib/sentry/files]
# Wed, 01 Feb 2017 23:59:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2017 23:59:26 GMT
CMD ["run" "web"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4665cede9d1cf30769226da349e1f7e35bf16f75d90688b9cab8569ce00ab79`  
		Last Modified: Mon, 19 Dec 2016 18:14:55 GMT  
		Size: 3.3 MB (3339260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a044686e6e0af7e1186aff3111899868a0e203d76bfde7b2e41c4c57c9d5595c`  
		Last Modified: Mon, 19 Dec 2016 18:28:51 GMT  
		Size: 16.4 MB (16364587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac23840f8b44de4114f1914c2c8f2a30f4782ec0afc3c362e708df4e3047a20`  
		Last Modified: Wed, 21 Dec 2016 20:10:42 GMT  
		Size: 4.3 KB (4344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe0b6c43af45024ee147b72bd5bd04c5433db94fd372652f470d0ec472e28c`  
		Last Modified: Wed, 21 Dec 2016 20:11:04 GMT  
		Size: 62.6 MB (62609336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acf3a0f5af58c264b5c0dddde7f67824e2232751a2117ba090332aea984cb63`  
		Last Modified: Wed, 21 Dec 2016 20:10:38 GMT  
		Size: 613.3 KB (613280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb9ce5250ca7215bd4b4865e1bb82faef11bad7c38dae7ff8b50dc68d95eaeb`  
		Last Modified: Wed, 21 Dec 2016 20:10:39 GMT  
		Size: 130.3 KB (130333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202daee25bc50a395705ba378c430517e359eb85539e74062b6135a11af4c155`  
		Last Modified: Wed, 21 Dec 2016 20:10:41 GMT  
		Size: 2.4 MB (2352903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b808d369ebf235587a12b9ce635ba74b9a160283df8e74bfa4dc5ff843c498bd`  
		Last Modified: Thu, 02 Feb 2017 00:01:03 GMT  
		Size: 47.0 MB (47001781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd94ac1498f0ebf912cff27dc3c3e89586d502ccbd169b3c9185e3343fbff4`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8002b9f3e5d213df0ef2883033db72a953c0fca5b3aa4f382bbe6208591be6e`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 3.4 KB (3400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27163c8222c16cc804a8f4a4d8910b1ce5ccf16542aebcbb0cf726be379b2e4`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4dd5fbdbbe71c108ba4eeac8aac23ef83062ed533d849ba1741ab79da512e2`  
		Last Modified: Thu, 02 Feb 2017 00:00:48 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sentry:8.13.0-onbuild`

```console
$ docker pull sentry@sha256:a28238e5a80e00b5cf93321b86be036bf8df39a52c4c8eccb8901ef13666a194
```

-	Platforms:
	-	linux; amd64

### `sentry:8.13.0-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183784137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2632a2b00712fcd12e4a468adbf2425509f29915f106eab3e38469ff332ce108`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 17:36:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2016 17:36:48 GMT
ENV LANG=C.UTF-8
# Wed, 14 Dec 2016 17:38:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 17:38:06 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Wed, 14 Dec 2016 17:38:07 GMT
ENV PYTHON_VERSION=2.7.12
# Wed, 14 Dec 2016 17:38:07 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Wed, 14 Dec 2016 18:47:35 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Wed, 14 Dec 2016 18:47:37 GMT
CMD ["python2"]
# Wed, 14 Dec 2016 19:40:39 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Wed, 14 Dec 2016 19:41:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 19:41:01 GMT
ENV PIP_NO_CACHE_DIR=off
# Wed, 14 Dec 2016 19:41:01 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Wed, 14 Dec 2016 19:41:01 GMT
ENV GOSU_VERSION=1.10
# Wed, 14 Dec 2016 19:41:13 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Wed, 14 Dec 2016 19:41:14 GMT
ENV TINI_VERSION=v0.10.0
# Wed, 14 Dec 2016 21:52:46 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Wed, 14 Dec 2016 21:53:03 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Wed, 01 Feb 2017 23:57:41 GMT
ENV SENTRY_VERSION=8.13.0
# Wed, 01 Feb 2017 23:59:21 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget
# Wed, 01 Feb 2017 23:59:22 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Wed, 01 Feb 2017 23:59:23 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Wed, 01 Feb 2017 23:59:25 GMT
EXPOSE 9000/tcp
# Wed, 01 Feb 2017 23:59:25 GMT
VOLUME [/var/lib/sentry/files]
# Wed, 01 Feb 2017 23:59:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2017 23:59:26 GMT
CMD ["run" "web"]
# Wed, 01 Feb 2017 23:59:26 GMT
WORKDIR /usr/src/sentry
# Wed, 01 Feb 2017 23:59:27 GMT
ENV PYTHONPATH=/usr/src/sentry
# Wed, 01 Feb 2017 23:59:27 GMT
ONBUILD COPY . /usr/src/sentry
# Wed, 01 Feb 2017 23:59:27 GMT
ONBUILD RUN if [ -s requirements.txt ]; then pip install -r requirements.txt; fi
# Wed, 01 Feb 2017 23:59:28 GMT
ONBUILD RUN if [ -s setup.py ]; then pip install -e .; fi
# Wed, 01 Feb 2017 23:59:28 GMT
ONBUILD RUN if [ -s sentry.conf.py ]; then cp sentry.conf.py $SENTRY_CONF/; fi 	&& if [ -s config.yml ]; then cp config.yml $SENTRY_CONF/; fi
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4665cede9d1cf30769226da349e1f7e35bf16f75d90688b9cab8569ce00ab79`  
		Last Modified: Mon, 19 Dec 2016 18:14:55 GMT  
		Size: 3.3 MB (3339260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a044686e6e0af7e1186aff3111899868a0e203d76bfde7b2e41c4c57c9d5595c`  
		Last Modified: Mon, 19 Dec 2016 18:28:51 GMT  
		Size: 16.4 MB (16364587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac23840f8b44de4114f1914c2c8f2a30f4782ec0afc3c362e708df4e3047a20`  
		Last Modified: Wed, 21 Dec 2016 20:10:42 GMT  
		Size: 4.3 KB (4344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe0b6c43af45024ee147b72bd5bd04c5433db94fd372652f470d0ec472e28c`  
		Last Modified: Wed, 21 Dec 2016 20:11:04 GMT  
		Size: 62.6 MB (62609336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acf3a0f5af58c264b5c0dddde7f67824e2232751a2117ba090332aea984cb63`  
		Last Modified: Wed, 21 Dec 2016 20:10:38 GMT  
		Size: 613.3 KB (613280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb9ce5250ca7215bd4b4865e1bb82faef11bad7c38dae7ff8b50dc68d95eaeb`  
		Last Modified: Wed, 21 Dec 2016 20:10:39 GMT  
		Size: 130.3 KB (130333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202daee25bc50a395705ba378c430517e359eb85539e74062b6135a11af4c155`  
		Last Modified: Wed, 21 Dec 2016 20:10:41 GMT  
		Size: 2.4 MB (2352903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b808d369ebf235587a12b9ce635ba74b9a160283df8e74bfa4dc5ff843c498bd`  
		Last Modified: Thu, 02 Feb 2017 00:01:03 GMT  
		Size: 47.0 MB (47001781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd94ac1498f0ebf912cff27dc3c3e89586d502ccbd169b3c9185e3343fbff4`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8002b9f3e5d213df0ef2883033db72a953c0fca5b3aa4f382bbe6208591be6e`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 3.4 KB (3400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27163c8222c16cc804a8f4a4d8910b1ce5ccf16542aebcbb0cf726be379b2e4`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4dd5fbdbbe71c108ba4eeac8aac23ef83062ed533d849ba1741ab79da512e2`  
		Last Modified: Thu, 02 Feb 2017 00:00:48 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a24224556806ac0e086054b46d3c84d1a42839cafff83ab0f7219f04a2d0445`  
		Last Modified: Thu, 02 Feb 2017 00:02:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sentry:8.13-onbuild`

```console
$ docker pull sentry@sha256:a28238e5a80e00b5cf93321b86be036bf8df39a52c4c8eccb8901ef13666a194
```

-	Platforms:
	-	linux; amd64

### `sentry:8.13-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183784137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2632a2b00712fcd12e4a468adbf2425509f29915f106eab3e38469ff332ce108`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 17:36:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2016 17:36:48 GMT
ENV LANG=C.UTF-8
# Wed, 14 Dec 2016 17:38:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 17:38:06 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Wed, 14 Dec 2016 17:38:07 GMT
ENV PYTHON_VERSION=2.7.12
# Wed, 14 Dec 2016 17:38:07 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Wed, 14 Dec 2016 18:47:35 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Wed, 14 Dec 2016 18:47:37 GMT
CMD ["python2"]
# Wed, 14 Dec 2016 19:40:39 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Wed, 14 Dec 2016 19:41:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 19:41:01 GMT
ENV PIP_NO_CACHE_DIR=off
# Wed, 14 Dec 2016 19:41:01 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Wed, 14 Dec 2016 19:41:01 GMT
ENV GOSU_VERSION=1.10
# Wed, 14 Dec 2016 19:41:13 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Wed, 14 Dec 2016 19:41:14 GMT
ENV TINI_VERSION=v0.10.0
# Wed, 14 Dec 2016 21:52:46 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Wed, 14 Dec 2016 21:53:03 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Wed, 01 Feb 2017 23:57:41 GMT
ENV SENTRY_VERSION=8.13.0
# Wed, 01 Feb 2017 23:59:21 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget
# Wed, 01 Feb 2017 23:59:22 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Wed, 01 Feb 2017 23:59:23 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Wed, 01 Feb 2017 23:59:24 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Wed, 01 Feb 2017 23:59:25 GMT
EXPOSE 9000/tcp
# Wed, 01 Feb 2017 23:59:25 GMT
VOLUME [/var/lib/sentry/files]
# Wed, 01 Feb 2017 23:59:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2017 23:59:26 GMT
CMD ["run" "web"]
# Wed, 01 Feb 2017 23:59:26 GMT
WORKDIR /usr/src/sentry
# Wed, 01 Feb 2017 23:59:27 GMT
ENV PYTHONPATH=/usr/src/sentry
# Wed, 01 Feb 2017 23:59:27 GMT
ONBUILD COPY . /usr/src/sentry
# Wed, 01 Feb 2017 23:59:27 GMT
ONBUILD RUN if [ -s requirements.txt ]; then pip install -r requirements.txt; fi
# Wed, 01 Feb 2017 23:59:28 GMT
ONBUILD RUN if [ -s setup.py ]; then pip install -e .; fi
# Wed, 01 Feb 2017 23:59:28 GMT
ONBUILD RUN if [ -s sentry.conf.py ]; then cp sentry.conf.py $SENTRY_CONF/; fi 	&& if [ -s config.yml ]; then cp config.yml $SENTRY_CONF/; fi
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4665cede9d1cf30769226da349e1f7e35bf16f75d90688b9cab8569ce00ab79`  
		Last Modified: Mon, 19 Dec 2016 18:14:55 GMT  
		Size: 3.3 MB (3339260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a044686e6e0af7e1186aff3111899868a0e203d76bfde7b2e41c4c57c9d5595c`  
		Last Modified: Mon, 19 Dec 2016 18:28:51 GMT  
		Size: 16.4 MB (16364587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac23840f8b44de4114f1914c2c8f2a30f4782ec0afc3c362e708df4e3047a20`  
		Last Modified: Wed, 21 Dec 2016 20:10:42 GMT  
		Size: 4.3 KB (4344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe0b6c43af45024ee147b72bd5bd04c5433db94fd372652f470d0ec472e28c`  
		Last Modified: Wed, 21 Dec 2016 20:11:04 GMT  
		Size: 62.6 MB (62609336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acf3a0f5af58c264b5c0dddde7f67824e2232751a2117ba090332aea984cb63`  
		Last Modified: Wed, 21 Dec 2016 20:10:38 GMT  
		Size: 613.3 KB (613280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb9ce5250ca7215bd4b4865e1bb82faef11bad7c38dae7ff8b50dc68d95eaeb`  
		Last Modified: Wed, 21 Dec 2016 20:10:39 GMT  
		Size: 130.3 KB (130333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202daee25bc50a395705ba378c430517e359eb85539e74062b6135a11af4c155`  
		Last Modified: Wed, 21 Dec 2016 20:10:41 GMT  
		Size: 2.4 MB (2352903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b808d369ebf235587a12b9ce635ba74b9a160283df8e74bfa4dc5ff843c498bd`  
		Last Modified: Thu, 02 Feb 2017 00:01:03 GMT  
		Size: 47.0 MB (47001781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd94ac1498f0ebf912cff27dc3c3e89586d502ccbd169b3c9185e3343fbff4`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8002b9f3e5d213df0ef2883033db72a953c0fca5b3aa4f382bbe6208591be6e`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 3.4 KB (3400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27163c8222c16cc804a8f4a4d8910b1ce5ccf16542aebcbb0cf726be379b2e4`  
		Last Modified: Thu, 02 Feb 2017 00:00:47 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4dd5fbdbbe71c108ba4eeac8aac23ef83062ed533d849ba1741ab79da512e2`  
		Last Modified: Thu, 02 Feb 2017 00:00:48 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a24224556806ac0e086054b46d3c84d1a42839cafff83ab0f7219f04a2d0445`  
		Last Modified: Thu, 02 Feb 2017 00:02:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sentry:8.14.1`

```console
$ docker pull sentry@sha256:f460a801572b429a1b9f70a90460fda20af39a09899ae8e4ec480c9a155de338
```

-	Platforms:
	-	linux; amd64

### `sentry:8.14.1` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184345837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc709630a61e485634f71284b5eb63d26b41ab38268fab97887ae06674cf5bb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:15:23 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 28 Feb 2017 22:15:23 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 28 Feb 2017 22:15:24 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:17:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:17:40 GMT
CMD ["python2"]
# Thu, 02 Mar 2017 18:42:29 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Thu, 02 Mar 2017 18:42:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2017 18:42:51 GMT
ENV PIP_NO_CACHE_DIR=off
# Thu, 02 Mar 2017 18:42:52 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Thu, 02 Mar 2017 18:42:52 GMT
ENV GOSU_VERSION=1.10
# Thu, 02 Mar 2017 18:43:01 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:02 GMT
ENV TINI_VERSION=v0.14.0
# Thu, 02 Mar 2017 18:43:09 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:23 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Tue, 07 Mar 2017 00:19:03 GMT
ENV SENTRY_VERSION=8.14.1
# Tue, 07 Mar 2017 00:20:52 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget g++ && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget g++
# Tue, 07 Mar 2017 00:20:53 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Tue, 07 Mar 2017 00:20:54 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Tue, 07 Mar 2017 00:20:54 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:55 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:56 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Tue, 07 Mar 2017 00:20:56 GMT
EXPOSE 9000/tcp
# Tue, 07 Mar 2017 00:20:56 GMT
VOLUME [/var/lib/sentry/files]
# Tue, 07 Mar 2017 00:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Mar 2017 00:20:57 GMT
CMD ["run" "web"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690360b5f9532df86160b5644bc5509dc8db409884dae5178f0fc9729b1ddece`  
		Last Modified: Wed, 01 Mar 2017 15:55:28 GMT  
		Size: 16.4 MB (16400684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aad146e1bab066b7901773949807508011f0da956400d0529237d5e99a2552`  
		Last Modified: Thu, 02 Mar 2017 18:46:41 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39481c73b78fdd5d38b067c05cdc2af8d193f1bccf5e360adf7d05323907f1b6`  
		Last Modified: Thu, 02 Mar 2017 18:46:59 GMT  
		Size: 62.6 MB (62624277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21299fe3cc31d215384bfd6c9dba7687ce908beae25b90075223d7e6c2e61add`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 613.1 KB (613150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f4cc611c12eb08fa2d3fe099babd519d8cc7ef90203e3eafe49aceabd7e9a1`  
		Last Modified: Thu, 02 Mar 2017 18:46:40 GMT  
		Size: 130.5 KB (130533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1108d3f27dc9cf230b216fd226e4134185949a33b21a53ba55e4da489e85c79`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 2.4 MB (2350956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3433bfc3a9e5a818d5865c6524508d5b9a85fc3ccbf25d64f52d163354b1142`  
		Last Modified: Tue, 07 Mar 2017 00:22:50 GMT  
		Size: 47.5 MB (47508978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b0629b2f1b089956ca26fcbbc25a9d85efbea1378ddc3e4ac3ec176d3702f9`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e541e3baa7f7445a08d79ca9a477273d9a393f2f23e72a0a96ac0df454f23624`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 3.4 KB (3396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604b798097260991af15ef2fd47179a49e88d0a84b1ca1af6902e9fffb8431a0`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b005a0139d2df656fa3ccfda3c47949a9823596f2f782e7e3cfc2816126fc7b5`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sentry:8.14`

```console
$ docker pull sentry@sha256:f460a801572b429a1b9f70a90460fda20af39a09899ae8e4ec480c9a155de338
```

-	Platforms:
	-	linux; amd64

### `sentry:8.14` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184345837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc709630a61e485634f71284b5eb63d26b41ab38268fab97887ae06674cf5bb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:15:23 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 28 Feb 2017 22:15:23 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 28 Feb 2017 22:15:24 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:17:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:17:40 GMT
CMD ["python2"]
# Thu, 02 Mar 2017 18:42:29 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Thu, 02 Mar 2017 18:42:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2017 18:42:51 GMT
ENV PIP_NO_CACHE_DIR=off
# Thu, 02 Mar 2017 18:42:52 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Thu, 02 Mar 2017 18:42:52 GMT
ENV GOSU_VERSION=1.10
# Thu, 02 Mar 2017 18:43:01 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:02 GMT
ENV TINI_VERSION=v0.14.0
# Thu, 02 Mar 2017 18:43:09 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:23 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Tue, 07 Mar 2017 00:19:03 GMT
ENV SENTRY_VERSION=8.14.1
# Tue, 07 Mar 2017 00:20:52 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget g++ && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget g++
# Tue, 07 Mar 2017 00:20:53 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Tue, 07 Mar 2017 00:20:54 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Tue, 07 Mar 2017 00:20:54 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:55 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:56 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Tue, 07 Mar 2017 00:20:56 GMT
EXPOSE 9000/tcp
# Tue, 07 Mar 2017 00:20:56 GMT
VOLUME [/var/lib/sentry/files]
# Tue, 07 Mar 2017 00:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Mar 2017 00:20:57 GMT
CMD ["run" "web"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690360b5f9532df86160b5644bc5509dc8db409884dae5178f0fc9729b1ddece`  
		Last Modified: Wed, 01 Mar 2017 15:55:28 GMT  
		Size: 16.4 MB (16400684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aad146e1bab066b7901773949807508011f0da956400d0529237d5e99a2552`  
		Last Modified: Thu, 02 Mar 2017 18:46:41 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39481c73b78fdd5d38b067c05cdc2af8d193f1bccf5e360adf7d05323907f1b6`  
		Last Modified: Thu, 02 Mar 2017 18:46:59 GMT  
		Size: 62.6 MB (62624277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21299fe3cc31d215384bfd6c9dba7687ce908beae25b90075223d7e6c2e61add`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 613.1 KB (613150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f4cc611c12eb08fa2d3fe099babd519d8cc7ef90203e3eafe49aceabd7e9a1`  
		Last Modified: Thu, 02 Mar 2017 18:46:40 GMT  
		Size: 130.5 KB (130533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1108d3f27dc9cf230b216fd226e4134185949a33b21a53ba55e4da489e85c79`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 2.4 MB (2350956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3433bfc3a9e5a818d5865c6524508d5b9a85fc3ccbf25d64f52d163354b1142`  
		Last Modified: Tue, 07 Mar 2017 00:22:50 GMT  
		Size: 47.5 MB (47508978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b0629b2f1b089956ca26fcbbc25a9d85efbea1378ddc3e4ac3ec176d3702f9`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e541e3baa7f7445a08d79ca9a477273d9a393f2f23e72a0a96ac0df454f23624`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 3.4 KB (3396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604b798097260991af15ef2fd47179a49e88d0a84b1ca1af6902e9fffb8431a0`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b005a0139d2df656fa3ccfda3c47949a9823596f2f782e7e3cfc2816126fc7b5`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sentry:8`

```console
$ docker pull sentry@sha256:f460a801572b429a1b9f70a90460fda20af39a09899ae8e4ec480c9a155de338
```

-	Platforms:
	-	linux; amd64

### `sentry:8` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184345837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc709630a61e485634f71284b5eb63d26b41ab38268fab97887ae06674cf5bb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:15:23 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 28 Feb 2017 22:15:23 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 28 Feb 2017 22:15:24 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:17:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:17:40 GMT
CMD ["python2"]
# Thu, 02 Mar 2017 18:42:29 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Thu, 02 Mar 2017 18:42:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2017 18:42:51 GMT
ENV PIP_NO_CACHE_DIR=off
# Thu, 02 Mar 2017 18:42:52 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Thu, 02 Mar 2017 18:42:52 GMT
ENV GOSU_VERSION=1.10
# Thu, 02 Mar 2017 18:43:01 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:02 GMT
ENV TINI_VERSION=v0.14.0
# Thu, 02 Mar 2017 18:43:09 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:23 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Tue, 07 Mar 2017 00:19:03 GMT
ENV SENTRY_VERSION=8.14.1
# Tue, 07 Mar 2017 00:20:52 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget g++ && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget g++
# Tue, 07 Mar 2017 00:20:53 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Tue, 07 Mar 2017 00:20:54 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Tue, 07 Mar 2017 00:20:54 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:55 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:56 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Tue, 07 Mar 2017 00:20:56 GMT
EXPOSE 9000/tcp
# Tue, 07 Mar 2017 00:20:56 GMT
VOLUME [/var/lib/sentry/files]
# Tue, 07 Mar 2017 00:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Mar 2017 00:20:57 GMT
CMD ["run" "web"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690360b5f9532df86160b5644bc5509dc8db409884dae5178f0fc9729b1ddece`  
		Last Modified: Wed, 01 Mar 2017 15:55:28 GMT  
		Size: 16.4 MB (16400684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aad146e1bab066b7901773949807508011f0da956400d0529237d5e99a2552`  
		Last Modified: Thu, 02 Mar 2017 18:46:41 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39481c73b78fdd5d38b067c05cdc2af8d193f1bccf5e360adf7d05323907f1b6`  
		Last Modified: Thu, 02 Mar 2017 18:46:59 GMT  
		Size: 62.6 MB (62624277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21299fe3cc31d215384bfd6c9dba7687ce908beae25b90075223d7e6c2e61add`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 613.1 KB (613150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f4cc611c12eb08fa2d3fe099babd519d8cc7ef90203e3eafe49aceabd7e9a1`  
		Last Modified: Thu, 02 Mar 2017 18:46:40 GMT  
		Size: 130.5 KB (130533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1108d3f27dc9cf230b216fd226e4134185949a33b21a53ba55e4da489e85c79`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 2.4 MB (2350956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3433bfc3a9e5a818d5865c6524508d5b9a85fc3ccbf25d64f52d163354b1142`  
		Last Modified: Tue, 07 Mar 2017 00:22:50 GMT  
		Size: 47.5 MB (47508978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b0629b2f1b089956ca26fcbbc25a9d85efbea1378ddc3e4ac3ec176d3702f9`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e541e3baa7f7445a08d79ca9a477273d9a393f2f23e72a0a96ac0df454f23624`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 3.4 KB (3396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604b798097260991af15ef2fd47179a49e88d0a84b1ca1af6902e9fffb8431a0`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b005a0139d2df656fa3ccfda3c47949a9823596f2f782e7e3cfc2816126fc7b5`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sentry:latest`

```console
$ docker pull sentry@sha256:f460a801572b429a1b9f70a90460fda20af39a09899ae8e4ec480c9a155de338
```

-	Platforms:
	-	linux; amd64

### `sentry:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184345837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc709630a61e485634f71284b5eb63d26b41ab38268fab97887ae06674cf5bb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:15:23 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 28 Feb 2017 22:15:23 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 28 Feb 2017 22:15:24 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:17:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:17:40 GMT
CMD ["python2"]
# Thu, 02 Mar 2017 18:42:29 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Thu, 02 Mar 2017 18:42:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2017 18:42:51 GMT
ENV PIP_NO_CACHE_DIR=off
# Thu, 02 Mar 2017 18:42:52 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Thu, 02 Mar 2017 18:42:52 GMT
ENV GOSU_VERSION=1.10
# Thu, 02 Mar 2017 18:43:01 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:02 GMT
ENV TINI_VERSION=v0.14.0
# Thu, 02 Mar 2017 18:43:09 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:23 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Tue, 07 Mar 2017 00:19:03 GMT
ENV SENTRY_VERSION=8.14.1
# Tue, 07 Mar 2017 00:20:52 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget g++ && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget g++
# Tue, 07 Mar 2017 00:20:53 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Tue, 07 Mar 2017 00:20:54 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Tue, 07 Mar 2017 00:20:54 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:55 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:56 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Tue, 07 Mar 2017 00:20:56 GMT
EXPOSE 9000/tcp
# Tue, 07 Mar 2017 00:20:56 GMT
VOLUME [/var/lib/sentry/files]
# Tue, 07 Mar 2017 00:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Mar 2017 00:20:57 GMT
CMD ["run" "web"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690360b5f9532df86160b5644bc5509dc8db409884dae5178f0fc9729b1ddece`  
		Last Modified: Wed, 01 Mar 2017 15:55:28 GMT  
		Size: 16.4 MB (16400684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aad146e1bab066b7901773949807508011f0da956400d0529237d5e99a2552`  
		Last Modified: Thu, 02 Mar 2017 18:46:41 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39481c73b78fdd5d38b067c05cdc2af8d193f1bccf5e360adf7d05323907f1b6`  
		Last Modified: Thu, 02 Mar 2017 18:46:59 GMT  
		Size: 62.6 MB (62624277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21299fe3cc31d215384bfd6c9dba7687ce908beae25b90075223d7e6c2e61add`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 613.1 KB (613150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f4cc611c12eb08fa2d3fe099babd519d8cc7ef90203e3eafe49aceabd7e9a1`  
		Last Modified: Thu, 02 Mar 2017 18:46:40 GMT  
		Size: 130.5 KB (130533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1108d3f27dc9cf230b216fd226e4134185949a33b21a53ba55e4da489e85c79`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 2.4 MB (2350956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3433bfc3a9e5a818d5865c6524508d5b9a85fc3ccbf25d64f52d163354b1142`  
		Last Modified: Tue, 07 Mar 2017 00:22:50 GMT  
		Size: 47.5 MB (47508978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b0629b2f1b089956ca26fcbbc25a9d85efbea1378ddc3e4ac3ec176d3702f9`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e541e3baa7f7445a08d79ca9a477273d9a393f2f23e72a0a96ac0df454f23624`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 3.4 KB (3396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604b798097260991af15ef2fd47179a49e88d0a84b1ca1af6902e9fffb8431a0`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b005a0139d2df656fa3ccfda3c47949a9823596f2f782e7e3cfc2816126fc7b5`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sentry:8.14.1-onbuild`

```console
$ docker pull sentry@sha256:3847510a5850152b8f9f6f2b40bf8f436b15152ddb26f19cb3426fcda638ca14
```

-	Platforms:
	-	linux; amd64

### `sentry:8.14.1-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184345969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be70f9b5465385fa198efc42c10dbd1563f707ce45083c3fb3fd4158a41f7d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:15:23 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 28 Feb 2017 22:15:23 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 28 Feb 2017 22:15:24 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:17:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:17:40 GMT
CMD ["python2"]
# Thu, 02 Mar 2017 18:42:29 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Thu, 02 Mar 2017 18:42:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2017 18:42:51 GMT
ENV PIP_NO_CACHE_DIR=off
# Thu, 02 Mar 2017 18:42:52 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Thu, 02 Mar 2017 18:42:52 GMT
ENV GOSU_VERSION=1.10
# Thu, 02 Mar 2017 18:43:01 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:02 GMT
ENV TINI_VERSION=v0.14.0
# Thu, 02 Mar 2017 18:43:09 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:23 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Tue, 07 Mar 2017 00:19:03 GMT
ENV SENTRY_VERSION=8.14.1
# Tue, 07 Mar 2017 00:20:52 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget g++ && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget g++
# Tue, 07 Mar 2017 00:20:53 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Tue, 07 Mar 2017 00:20:54 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Tue, 07 Mar 2017 00:20:54 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:55 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:56 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Tue, 07 Mar 2017 00:20:56 GMT
EXPOSE 9000/tcp
# Tue, 07 Mar 2017 00:20:56 GMT
VOLUME [/var/lib/sentry/files]
# Tue, 07 Mar 2017 00:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Mar 2017 00:20:57 GMT
CMD ["run" "web"]
# Tue, 07 Mar 2017 00:20:58 GMT
WORKDIR /usr/src/sentry
# Tue, 07 Mar 2017 00:20:58 GMT
ENV PYTHONPATH=/usr/src/sentry
# Tue, 07 Mar 2017 00:20:59 GMT
ONBUILD COPY . /usr/src/sentry
# Tue, 07 Mar 2017 00:20:59 GMT
ONBUILD RUN if [ -s requirements.txt ]; then pip install -r requirements.txt; fi
# Tue, 07 Mar 2017 00:21:00 GMT
ONBUILD RUN if [ -s setup.py ]; then pip install -e .; fi
# Tue, 07 Mar 2017 00:21:00 GMT
ONBUILD RUN if [ -s sentry.conf.py ]; then cp sentry.conf.py $SENTRY_CONF/; fi 	&& if [ -s config.yml ]; then cp config.yml $SENTRY_CONF/; fi
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690360b5f9532df86160b5644bc5509dc8db409884dae5178f0fc9729b1ddece`  
		Last Modified: Wed, 01 Mar 2017 15:55:28 GMT  
		Size: 16.4 MB (16400684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aad146e1bab066b7901773949807508011f0da956400d0529237d5e99a2552`  
		Last Modified: Thu, 02 Mar 2017 18:46:41 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39481c73b78fdd5d38b067c05cdc2af8d193f1bccf5e360adf7d05323907f1b6`  
		Last Modified: Thu, 02 Mar 2017 18:46:59 GMT  
		Size: 62.6 MB (62624277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21299fe3cc31d215384bfd6c9dba7687ce908beae25b90075223d7e6c2e61add`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 613.1 KB (613150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f4cc611c12eb08fa2d3fe099babd519d8cc7ef90203e3eafe49aceabd7e9a1`  
		Last Modified: Thu, 02 Mar 2017 18:46:40 GMT  
		Size: 130.5 KB (130533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1108d3f27dc9cf230b216fd226e4134185949a33b21a53ba55e4da489e85c79`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 2.4 MB (2350956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3433bfc3a9e5a818d5865c6524508d5b9a85fc3ccbf25d64f52d163354b1142`  
		Last Modified: Tue, 07 Mar 2017 00:22:50 GMT  
		Size: 47.5 MB (47508978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b0629b2f1b089956ca26fcbbc25a9d85efbea1378ddc3e4ac3ec176d3702f9`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e541e3baa7f7445a08d79ca9a477273d9a393f2f23e72a0a96ac0df454f23624`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 3.4 KB (3396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604b798097260991af15ef2fd47179a49e88d0a84b1ca1af6902e9fffb8431a0`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b005a0139d2df656fa3ccfda3c47949a9823596f2f782e7e3cfc2816126fc7b5`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3977a502b90338dd2c7d918d000fbf84586f26d99f95d2919557b662cf4c3c3a`  
		Last Modified: Tue, 07 Mar 2017 00:24:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sentry:8.14-onbuild`

```console
$ docker pull sentry@sha256:3847510a5850152b8f9f6f2b40bf8f436b15152ddb26f19cb3426fcda638ca14
```

-	Platforms:
	-	linux; amd64

### `sentry:8.14-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184345969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be70f9b5465385fa198efc42c10dbd1563f707ce45083c3fb3fd4158a41f7d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:15:23 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 28 Feb 2017 22:15:23 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 28 Feb 2017 22:15:24 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:17:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:17:40 GMT
CMD ["python2"]
# Thu, 02 Mar 2017 18:42:29 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Thu, 02 Mar 2017 18:42:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2017 18:42:51 GMT
ENV PIP_NO_CACHE_DIR=off
# Thu, 02 Mar 2017 18:42:52 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Thu, 02 Mar 2017 18:42:52 GMT
ENV GOSU_VERSION=1.10
# Thu, 02 Mar 2017 18:43:01 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:02 GMT
ENV TINI_VERSION=v0.14.0
# Thu, 02 Mar 2017 18:43:09 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:23 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Tue, 07 Mar 2017 00:19:03 GMT
ENV SENTRY_VERSION=8.14.1
# Tue, 07 Mar 2017 00:20:52 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget g++ && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget g++
# Tue, 07 Mar 2017 00:20:53 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Tue, 07 Mar 2017 00:20:54 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Tue, 07 Mar 2017 00:20:54 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:55 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:56 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Tue, 07 Mar 2017 00:20:56 GMT
EXPOSE 9000/tcp
# Tue, 07 Mar 2017 00:20:56 GMT
VOLUME [/var/lib/sentry/files]
# Tue, 07 Mar 2017 00:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Mar 2017 00:20:57 GMT
CMD ["run" "web"]
# Tue, 07 Mar 2017 00:20:58 GMT
WORKDIR /usr/src/sentry
# Tue, 07 Mar 2017 00:20:58 GMT
ENV PYTHONPATH=/usr/src/sentry
# Tue, 07 Mar 2017 00:20:59 GMT
ONBUILD COPY . /usr/src/sentry
# Tue, 07 Mar 2017 00:20:59 GMT
ONBUILD RUN if [ -s requirements.txt ]; then pip install -r requirements.txt; fi
# Tue, 07 Mar 2017 00:21:00 GMT
ONBUILD RUN if [ -s setup.py ]; then pip install -e .; fi
# Tue, 07 Mar 2017 00:21:00 GMT
ONBUILD RUN if [ -s sentry.conf.py ]; then cp sentry.conf.py $SENTRY_CONF/; fi 	&& if [ -s config.yml ]; then cp config.yml $SENTRY_CONF/; fi
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690360b5f9532df86160b5644bc5509dc8db409884dae5178f0fc9729b1ddece`  
		Last Modified: Wed, 01 Mar 2017 15:55:28 GMT  
		Size: 16.4 MB (16400684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aad146e1bab066b7901773949807508011f0da956400d0529237d5e99a2552`  
		Last Modified: Thu, 02 Mar 2017 18:46:41 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39481c73b78fdd5d38b067c05cdc2af8d193f1bccf5e360adf7d05323907f1b6`  
		Last Modified: Thu, 02 Mar 2017 18:46:59 GMT  
		Size: 62.6 MB (62624277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21299fe3cc31d215384bfd6c9dba7687ce908beae25b90075223d7e6c2e61add`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 613.1 KB (613150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f4cc611c12eb08fa2d3fe099babd519d8cc7ef90203e3eafe49aceabd7e9a1`  
		Last Modified: Thu, 02 Mar 2017 18:46:40 GMT  
		Size: 130.5 KB (130533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1108d3f27dc9cf230b216fd226e4134185949a33b21a53ba55e4da489e85c79`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 2.4 MB (2350956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3433bfc3a9e5a818d5865c6524508d5b9a85fc3ccbf25d64f52d163354b1142`  
		Last Modified: Tue, 07 Mar 2017 00:22:50 GMT  
		Size: 47.5 MB (47508978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b0629b2f1b089956ca26fcbbc25a9d85efbea1378ddc3e4ac3ec176d3702f9`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e541e3baa7f7445a08d79ca9a477273d9a393f2f23e72a0a96ac0df454f23624`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 3.4 KB (3396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604b798097260991af15ef2fd47179a49e88d0a84b1ca1af6902e9fffb8431a0`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b005a0139d2df656fa3ccfda3c47949a9823596f2f782e7e3cfc2816126fc7b5`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3977a502b90338dd2c7d918d000fbf84586f26d99f95d2919557b662cf4c3c3a`  
		Last Modified: Tue, 07 Mar 2017 00:24:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sentry:8-onbuild`

```console
$ docker pull sentry@sha256:3847510a5850152b8f9f6f2b40bf8f436b15152ddb26f19cb3426fcda638ca14
```

-	Platforms:
	-	linux; amd64

### `sentry:8-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184345969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be70f9b5465385fa198efc42c10dbd1563f707ce45083c3fb3fd4158a41f7d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:15:23 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 28 Feb 2017 22:15:23 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 28 Feb 2017 22:15:24 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:17:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:17:40 GMT
CMD ["python2"]
# Thu, 02 Mar 2017 18:42:29 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Thu, 02 Mar 2017 18:42:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2017 18:42:51 GMT
ENV PIP_NO_CACHE_DIR=off
# Thu, 02 Mar 2017 18:42:52 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Thu, 02 Mar 2017 18:42:52 GMT
ENV GOSU_VERSION=1.10
# Thu, 02 Mar 2017 18:43:01 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:02 GMT
ENV TINI_VERSION=v0.14.0
# Thu, 02 Mar 2017 18:43:09 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:23 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Tue, 07 Mar 2017 00:19:03 GMT
ENV SENTRY_VERSION=8.14.1
# Tue, 07 Mar 2017 00:20:52 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget g++ && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget g++
# Tue, 07 Mar 2017 00:20:53 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Tue, 07 Mar 2017 00:20:54 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Tue, 07 Mar 2017 00:20:54 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:55 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:56 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Tue, 07 Mar 2017 00:20:56 GMT
EXPOSE 9000/tcp
# Tue, 07 Mar 2017 00:20:56 GMT
VOLUME [/var/lib/sentry/files]
# Tue, 07 Mar 2017 00:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Mar 2017 00:20:57 GMT
CMD ["run" "web"]
# Tue, 07 Mar 2017 00:20:58 GMT
WORKDIR /usr/src/sentry
# Tue, 07 Mar 2017 00:20:58 GMT
ENV PYTHONPATH=/usr/src/sentry
# Tue, 07 Mar 2017 00:20:59 GMT
ONBUILD COPY . /usr/src/sentry
# Tue, 07 Mar 2017 00:20:59 GMT
ONBUILD RUN if [ -s requirements.txt ]; then pip install -r requirements.txt; fi
# Tue, 07 Mar 2017 00:21:00 GMT
ONBUILD RUN if [ -s setup.py ]; then pip install -e .; fi
# Tue, 07 Mar 2017 00:21:00 GMT
ONBUILD RUN if [ -s sentry.conf.py ]; then cp sentry.conf.py $SENTRY_CONF/; fi 	&& if [ -s config.yml ]; then cp config.yml $SENTRY_CONF/; fi
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690360b5f9532df86160b5644bc5509dc8db409884dae5178f0fc9729b1ddece`  
		Last Modified: Wed, 01 Mar 2017 15:55:28 GMT  
		Size: 16.4 MB (16400684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aad146e1bab066b7901773949807508011f0da956400d0529237d5e99a2552`  
		Last Modified: Thu, 02 Mar 2017 18:46:41 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39481c73b78fdd5d38b067c05cdc2af8d193f1bccf5e360adf7d05323907f1b6`  
		Last Modified: Thu, 02 Mar 2017 18:46:59 GMT  
		Size: 62.6 MB (62624277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21299fe3cc31d215384bfd6c9dba7687ce908beae25b90075223d7e6c2e61add`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 613.1 KB (613150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f4cc611c12eb08fa2d3fe099babd519d8cc7ef90203e3eafe49aceabd7e9a1`  
		Last Modified: Thu, 02 Mar 2017 18:46:40 GMT  
		Size: 130.5 KB (130533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1108d3f27dc9cf230b216fd226e4134185949a33b21a53ba55e4da489e85c79`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 2.4 MB (2350956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3433bfc3a9e5a818d5865c6524508d5b9a85fc3ccbf25d64f52d163354b1142`  
		Last Modified: Tue, 07 Mar 2017 00:22:50 GMT  
		Size: 47.5 MB (47508978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b0629b2f1b089956ca26fcbbc25a9d85efbea1378ddc3e4ac3ec176d3702f9`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e541e3baa7f7445a08d79ca9a477273d9a393f2f23e72a0a96ac0df454f23624`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 3.4 KB (3396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604b798097260991af15ef2fd47179a49e88d0a84b1ca1af6902e9fffb8431a0`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b005a0139d2df656fa3ccfda3c47949a9823596f2f782e7e3cfc2816126fc7b5`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3977a502b90338dd2c7d918d000fbf84586f26d99f95d2919557b662cf4c3c3a`  
		Last Modified: Tue, 07 Mar 2017 00:24:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sentry:onbuild`

```console
$ docker pull sentry@sha256:3847510a5850152b8f9f6f2b40bf8f436b15152ddb26f19cb3426fcda638ca14
```

-	Platforms:
	-	linux; amd64

### `sentry:onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184345969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be70f9b5465385fa198efc42c10dbd1563f707ce45083c3fb3fd4158a41f7d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:15:23 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 28 Feb 2017 22:15:23 GMT
ENV PYTHON_VERSION=2.7.13
# Tue, 28 Feb 2017 22:15:24 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:17:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-shared 		--enable-unicode=ucs4 	&& make -j$(nproc) 	&& make install 	&& ldconfig 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python2 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:17:40 GMT
CMD ["python2"]
# Thu, 02 Mar 2017 18:42:29 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Thu, 02 Mar 2017 18:42:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2017 18:42:51 GMT
ENV PIP_NO_CACHE_DIR=off
# Thu, 02 Mar 2017 18:42:52 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Thu, 02 Mar 2017 18:42:52 GMT
ENV GOSU_VERSION=1.10
# Thu, 02 Mar 2017 18:43:01 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:02 GMT
ENV TINI_VERSION=v0.14.0
# Thu, 02 Mar 2017 18:43:09 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Thu, 02 Mar 2017 18:43:23 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Tue, 07 Mar 2017 00:19:03 GMT
ENV SENTRY_VERSION=8.14.1
# Tue, 07 Mar 2017 00:20:52 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget g++ && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget g++
# Tue, 07 Mar 2017 00:20:53 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Tue, 07 Mar 2017 00:20:54 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Tue, 07 Mar 2017 00:20:54 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:55 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Tue, 07 Mar 2017 00:20:56 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Tue, 07 Mar 2017 00:20:56 GMT
EXPOSE 9000/tcp
# Tue, 07 Mar 2017 00:20:56 GMT
VOLUME [/var/lib/sentry/files]
# Tue, 07 Mar 2017 00:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Mar 2017 00:20:57 GMT
CMD ["run" "web"]
# Tue, 07 Mar 2017 00:20:58 GMT
WORKDIR /usr/src/sentry
# Tue, 07 Mar 2017 00:20:58 GMT
ENV PYTHONPATH=/usr/src/sentry
# Tue, 07 Mar 2017 00:20:59 GMT
ONBUILD COPY . /usr/src/sentry
# Tue, 07 Mar 2017 00:20:59 GMT
ONBUILD RUN if [ -s requirements.txt ]; then pip install -r requirements.txt; fi
# Tue, 07 Mar 2017 00:21:00 GMT
ONBUILD RUN if [ -s setup.py ]; then pip install -e .; fi
# Tue, 07 Mar 2017 00:21:00 GMT
ONBUILD RUN if [ -s sentry.conf.py ]; then cp sentry.conf.py $SENTRY_CONF/; fi 	&& if [ -s config.yml ]; then cp config.yml $SENTRY_CONF/; fi
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690360b5f9532df86160b5644bc5509dc8db409884dae5178f0fc9729b1ddece`  
		Last Modified: Wed, 01 Mar 2017 15:55:28 GMT  
		Size: 16.4 MB (16400684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aad146e1bab066b7901773949807508011f0da956400d0529237d5e99a2552`  
		Last Modified: Thu, 02 Mar 2017 18:46:41 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39481c73b78fdd5d38b067c05cdc2af8d193f1bccf5e360adf7d05323907f1b6`  
		Last Modified: Thu, 02 Mar 2017 18:46:59 GMT  
		Size: 62.6 MB (62624277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21299fe3cc31d215384bfd6c9dba7687ce908beae25b90075223d7e6c2e61add`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 613.1 KB (613150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f4cc611c12eb08fa2d3fe099babd519d8cc7ef90203e3eafe49aceabd7e9a1`  
		Last Modified: Thu, 02 Mar 2017 18:46:40 GMT  
		Size: 130.5 KB (130533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1108d3f27dc9cf230b216fd226e4134185949a33b21a53ba55e4da489e85c79`  
		Last Modified: Thu, 02 Mar 2017 18:46:39 GMT  
		Size: 2.4 MB (2350956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3433bfc3a9e5a818d5865c6524508d5b9a85fc3ccbf25d64f52d163354b1142`  
		Last Modified: Tue, 07 Mar 2017 00:22:50 GMT  
		Size: 47.5 MB (47508978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b0629b2f1b089956ca26fcbbc25a9d85efbea1378ddc3e4ac3ec176d3702f9`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e541e3baa7f7445a08d79ca9a477273d9a393f2f23e72a0a96ac0df454f23624`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 3.4 KB (3396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604b798097260991af15ef2fd47179a49e88d0a84b1ca1af6902e9fffb8431a0`  
		Last Modified: Tue, 07 Mar 2017 00:22:34 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b005a0139d2df656fa3ccfda3c47949a9823596f2f782e7e3cfc2816126fc7b5`  
		Last Modified: Tue, 07 Mar 2017 00:22:35 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3977a502b90338dd2c7d918d000fbf84586f26d99f95d2919557b662cf4c3c3a`  
		Last Modified: Tue, 07 Mar 2017 00:24:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
