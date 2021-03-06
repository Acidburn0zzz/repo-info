<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:5.3.0`](#kibana530)
-	[`kibana:5.3`](#kibana53)
-	[`kibana:5`](#kibana5)
-	[`kibana:latest`](#kibanalatest)
-	[`kibana:4.6.4`](#kibana464)
-	[`kibana:4.6`](#kibana46)
-	[`kibana:4`](#kibana4)
-	[`kibana:4.1.11`](#kibana4111)
-	[`kibana:4.1`](#kibana41)

## `kibana:5.3.0`

```console
$ docker pull kibana@sha256:9ddde7b0b065f523f70ed3df97a8353fc1a16bc653573f6172ea47ba3b743489
```

-	Platforms:
	-	linux; amd64

### `kibana:5.3.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113150964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb73273a30c9b15790f80a1b46cf53abf4d88b7893d0b9e21284ac386a2f2b1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kibana"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:55:30 GMT
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
# Tue, 21 Mar 2017 20:56:37 GMT
RUN apt-get update && apt-get install -y 		apt-transport-https 		ca-certificates 		wget 		libfontconfig 		libfreetype6 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:56:37 GMT
ENV GOSU_VERSION=1.7
# Tue, 21 Mar 2017 20:56:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 21 Mar 2017 20:56:43 GMT
ENV TINI_VERSION=v0.9.0
# Tue, 21 Mar 2017 20:56:45 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Tue, 21 Mar 2017 20:56:46 GMT
RUN set -ex; 	key='46095ACC8548582C1A2699A9D27D666CD88E42B4'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/elastic.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 21 Mar 2017 20:56:47 GMT
RUN echo 'deb https://artifacts.elastic.co/packages/5.x/apt stable main' > /etc/apt/sources.list.d/kibana.list
# Thu, 30 Mar 2017 21:36:51 GMT
ENV KIBANA_VERSION=5.3.0
# Thu, 30 Mar 2017 21:37:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(server\.host:).*!\2 '0.0.0.0'!" /etc/kibana/kibana.yml 	&& grep -q "^server\.host: '0.0.0.0'\$" /etc/kibana/kibana.yml 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /etc/kibana/kibana.yml 	&& grep -q "^elasticsearch\.url: 'http://elasticsearch:9200'\$" /etc/kibana/kibana.yml
# Thu, 30 Mar 2017 21:37:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2017 21:37:10 GMT
COPY file:9a3ed3a1655d5afa631fded5211f1c33f5f49f1d1e0e0d9a031c9e8601111f05 in / 
# Thu, 30 Mar 2017 21:37:10 GMT
EXPOSE 5601/tcp
# Thu, 30 Mar 2017 21:37:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2017 21:37:12 GMT
CMD ["kibana"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da41a38ea23917f9f37673d2c2acd2d08129ab37f09123586a1c72343a99aef9`  
		Last Modified: Thu, 23 Mar 2017 21:53:26 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562680f0f3bffdbee6b127731fd1ad8fd63c87062bfee8beac2fd2d92779579f`  
		Last Modified: Thu, 23 Mar 2017 21:55:54 GMT  
		Size: 21.7 MB (21710183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cade4f7688ac7c74f1ec84141cc184d9514f547ee92bd6c76d9fad84c27698b5`  
		Last Modified: Thu, 23 Mar 2017 21:55:47 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbabfdc37b0c3ebc6623ef62252adb33a70ccd697a598af75823f45abcd724d`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 7.1 KB (7123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67946bcc50478e087d7c553ed0cd6c1ac8dcad99b34c981ae462488db20b3a5`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6f8a274410c056ae9da6b2586fdd9ee35891ed0a5a4f48f4edc5b74affb1d5`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bcdf5398f6399b0afd046503f2761453358487dda98d7b34617d8bdd9342cd`  
		Last Modified: Thu, 30 Mar 2017 21:37:47 GMT  
		Size: 39.2 MB (39180894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6412aef37a5fb3babdb54718fb9b05105c7a7b6578553286be6e3c3e4f8e00d`  
		Last Modified: Thu, 30 Mar 2017 21:37:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:5.3`

```console
$ docker pull kibana@sha256:9ddde7b0b065f523f70ed3df97a8353fc1a16bc653573f6172ea47ba3b743489
```

-	Platforms:
	-	linux; amd64

### `kibana:5.3` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113150964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb73273a30c9b15790f80a1b46cf53abf4d88b7893d0b9e21284ac386a2f2b1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kibana"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:55:30 GMT
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
# Tue, 21 Mar 2017 20:56:37 GMT
RUN apt-get update && apt-get install -y 		apt-transport-https 		ca-certificates 		wget 		libfontconfig 		libfreetype6 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:56:37 GMT
ENV GOSU_VERSION=1.7
# Tue, 21 Mar 2017 20:56:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 21 Mar 2017 20:56:43 GMT
ENV TINI_VERSION=v0.9.0
# Tue, 21 Mar 2017 20:56:45 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Tue, 21 Mar 2017 20:56:46 GMT
RUN set -ex; 	key='46095ACC8548582C1A2699A9D27D666CD88E42B4'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/elastic.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 21 Mar 2017 20:56:47 GMT
RUN echo 'deb https://artifacts.elastic.co/packages/5.x/apt stable main' > /etc/apt/sources.list.d/kibana.list
# Thu, 30 Mar 2017 21:36:51 GMT
ENV KIBANA_VERSION=5.3.0
# Thu, 30 Mar 2017 21:37:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(server\.host:).*!\2 '0.0.0.0'!" /etc/kibana/kibana.yml 	&& grep -q "^server\.host: '0.0.0.0'\$" /etc/kibana/kibana.yml 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /etc/kibana/kibana.yml 	&& grep -q "^elasticsearch\.url: 'http://elasticsearch:9200'\$" /etc/kibana/kibana.yml
# Thu, 30 Mar 2017 21:37:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2017 21:37:10 GMT
COPY file:9a3ed3a1655d5afa631fded5211f1c33f5f49f1d1e0e0d9a031c9e8601111f05 in / 
# Thu, 30 Mar 2017 21:37:10 GMT
EXPOSE 5601/tcp
# Thu, 30 Mar 2017 21:37:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2017 21:37:12 GMT
CMD ["kibana"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da41a38ea23917f9f37673d2c2acd2d08129ab37f09123586a1c72343a99aef9`  
		Last Modified: Thu, 23 Mar 2017 21:53:26 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562680f0f3bffdbee6b127731fd1ad8fd63c87062bfee8beac2fd2d92779579f`  
		Last Modified: Thu, 23 Mar 2017 21:55:54 GMT  
		Size: 21.7 MB (21710183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cade4f7688ac7c74f1ec84141cc184d9514f547ee92bd6c76d9fad84c27698b5`  
		Last Modified: Thu, 23 Mar 2017 21:55:47 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbabfdc37b0c3ebc6623ef62252adb33a70ccd697a598af75823f45abcd724d`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 7.1 KB (7123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67946bcc50478e087d7c553ed0cd6c1ac8dcad99b34c981ae462488db20b3a5`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6f8a274410c056ae9da6b2586fdd9ee35891ed0a5a4f48f4edc5b74affb1d5`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bcdf5398f6399b0afd046503f2761453358487dda98d7b34617d8bdd9342cd`  
		Last Modified: Thu, 30 Mar 2017 21:37:47 GMT  
		Size: 39.2 MB (39180894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6412aef37a5fb3babdb54718fb9b05105c7a7b6578553286be6e3c3e4f8e00d`  
		Last Modified: Thu, 30 Mar 2017 21:37:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:5`

```console
$ docker pull kibana@sha256:9ddde7b0b065f523f70ed3df97a8353fc1a16bc653573f6172ea47ba3b743489
```

-	Platforms:
	-	linux; amd64

### `kibana:5` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113150964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb73273a30c9b15790f80a1b46cf53abf4d88b7893d0b9e21284ac386a2f2b1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kibana"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:55:30 GMT
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
# Tue, 21 Mar 2017 20:56:37 GMT
RUN apt-get update && apt-get install -y 		apt-transport-https 		ca-certificates 		wget 		libfontconfig 		libfreetype6 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:56:37 GMT
ENV GOSU_VERSION=1.7
# Tue, 21 Mar 2017 20:56:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 21 Mar 2017 20:56:43 GMT
ENV TINI_VERSION=v0.9.0
# Tue, 21 Mar 2017 20:56:45 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Tue, 21 Mar 2017 20:56:46 GMT
RUN set -ex; 	key='46095ACC8548582C1A2699A9D27D666CD88E42B4'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/elastic.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 21 Mar 2017 20:56:47 GMT
RUN echo 'deb https://artifacts.elastic.co/packages/5.x/apt stable main' > /etc/apt/sources.list.d/kibana.list
# Thu, 30 Mar 2017 21:36:51 GMT
ENV KIBANA_VERSION=5.3.0
# Thu, 30 Mar 2017 21:37:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(server\.host:).*!\2 '0.0.0.0'!" /etc/kibana/kibana.yml 	&& grep -q "^server\.host: '0.0.0.0'\$" /etc/kibana/kibana.yml 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /etc/kibana/kibana.yml 	&& grep -q "^elasticsearch\.url: 'http://elasticsearch:9200'\$" /etc/kibana/kibana.yml
# Thu, 30 Mar 2017 21:37:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2017 21:37:10 GMT
COPY file:9a3ed3a1655d5afa631fded5211f1c33f5f49f1d1e0e0d9a031c9e8601111f05 in / 
# Thu, 30 Mar 2017 21:37:10 GMT
EXPOSE 5601/tcp
# Thu, 30 Mar 2017 21:37:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2017 21:37:12 GMT
CMD ["kibana"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da41a38ea23917f9f37673d2c2acd2d08129ab37f09123586a1c72343a99aef9`  
		Last Modified: Thu, 23 Mar 2017 21:53:26 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562680f0f3bffdbee6b127731fd1ad8fd63c87062bfee8beac2fd2d92779579f`  
		Last Modified: Thu, 23 Mar 2017 21:55:54 GMT  
		Size: 21.7 MB (21710183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cade4f7688ac7c74f1ec84141cc184d9514f547ee92bd6c76d9fad84c27698b5`  
		Last Modified: Thu, 23 Mar 2017 21:55:47 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbabfdc37b0c3ebc6623ef62252adb33a70ccd697a598af75823f45abcd724d`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 7.1 KB (7123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67946bcc50478e087d7c553ed0cd6c1ac8dcad99b34c981ae462488db20b3a5`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6f8a274410c056ae9da6b2586fdd9ee35891ed0a5a4f48f4edc5b74affb1d5`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bcdf5398f6399b0afd046503f2761453358487dda98d7b34617d8bdd9342cd`  
		Last Modified: Thu, 30 Mar 2017 21:37:47 GMT  
		Size: 39.2 MB (39180894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6412aef37a5fb3babdb54718fb9b05105c7a7b6578553286be6e3c3e4f8e00d`  
		Last Modified: Thu, 30 Mar 2017 21:37:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:latest`

```console
$ docker pull kibana@sha256:9ddde7b0b065f523f70ed3df97a8353fc1a16bc653573f6172ea47ba3b743489
```

-	Platforms:
	-	linux; amd64

### `kibana:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113150964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb73273a30c9b15790f80a1b46cf53abf4d88b7893d0b9e21284ac386a2f2b1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kibana"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:55:30 GMT
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
# Tue, 21 Mar 2017 20:56:37 GMT
RUN apt-get update && apt-get install -y 		apt-transport-https 		ca-certificates 		wget 		libfontconfig 		libfreetype6 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:56:37 GMT
ENV GOSU_VERSION=1.7
# Tue, 21 Mar 2017 20:56:42 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 21 Mar 2017 20:56:43 GMT
ENV TINI_VERSION=v0.9.0
# Tue, 21 Mar 2017 20:56:45 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Tue, 21 Mar 2017 20:56:46 GMT
RUN set -ex; 	key='46095ACC8548582C1A2699A9D27D666CD88E42B4'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/elastic.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 21 Mar 2017 20:56:47 GMT
RUN echo 'deb https://artifacts.elastic.co/packages/5.x/apt stable main' > /etc/apt/sources.list.d/kibana.list
# Thu, 30 Mar 2017 21:36:51 GMT
ENV KIBANA_VERSION=5.3.0
# Thu, 30 Mar 2017 21:37:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(server\.host:).*!\2 '0.0.0.0'!" /etc/kibana/kibana.yml 	&& grep -q "^server\.host: '0.0.0.0'\$" /etc/kibana/kibana.yml 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /etc/kibana/kibana.yml 	&& grep -q "^elasticsearch\.url: 'http://elasticsearch:9200'\$" /etc/kibana/kibana.yml
# Thu, 30 Mar 2017 21:37:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2017 21:37:10 GMT
COPY file:9a3ed3a1655d5afa631fded5211f1c33f5f49f1d1e0e0d9a031c9e8601111f05 in / 
# Thu, 30 Mar 2017 21:37:10 GMT
EXPOSE 5601/tcp
# Thu, 30 Mar 2017 21:37:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2017 21:37:12 GMT
CMD ["kibana"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da41a38ea23917f9f37673d2c2acd2d08129ab37f09123586a1c72343a99aef9`  
		Last Modified: Thu, 23 Mar 2017 21:53:26 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562680f0f3bffdbee6b127731fd1ad8fd63c87062bfee8beac2fd2d92779579f`  
		Last Modified: Thu, 23 Mar 2017 21:55:54 GMT  
		Size: 21.7 MB (21710183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cade4f7688ac7c74f1ec84141cc184d9514f547ee92bd6c76d9fad84c27698b5`  
		Last Modified: Thu, 23 Mar 2017 21:55:47 GMT  
		Size: 807.9 KB (807934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbabfdc37b0c3ebc6623ef62252adb33a70ccd697a598af75823f45abcd724d`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 7.1 KB (7123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67946bcc50478e087d7c553ed0cd6c1ac8dcad99b34c981ae462488db20b3a5`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6f8a274410c056ae9da6b2586fdd9ee35891ed0a5a4f48f4edc5b74affb1d5`  
		Last Modified: Thu, 23 Mar 2017 21:55:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bcdf5398f6399b0afd046503f2761453358487dda98d7b34617d8bdd9342cd`  
		Last Modified: Thu, 30 Mar 2017 21:37:47 GMT  
		Size: 39.2 MB (39180894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6412aef37a5fb3babdb54718fb9b05105c7a7b6578553286be6e3c3e4f8e00d`  
		Last Modified: Thu, 30 Mar 2017 21:37:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:4.6.4`

```console
$ docker pull kibana@sha256:3e0ff21b6cee87531877f3373217eaee594702127e61d37fd46c33fa31ed4737
```

-	Platforms:
	-	linux; amd64

### `kibana:4.6.4` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108054417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468a1e1f2b33b7aa28baa362c02b19dafac08ea725cbdabb7f9f5783dc4a0563`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kibana"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:55:30 GMT
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
# Tue, 21 Mar 2017 20:55:43 GMT
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 		libfontconfig 		libfreetype6 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:55:43 GMT
ENV GOSU_VERSION=1.7
# Tue, 21 Mar 2017 20:55:48 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 21 Mar 2017 20:55:48 GMT
ENV TINI_VERSION=v0.9.0
# Tue, 21 Mar 2017 20:55:51 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Tue, 21 Mar 2017 20:55:52 GMT
RUN set -ex; 	key='46095ACC8548582C1A2699A9D27D666CD88E42B4'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/elastic.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 21 Mar 2017 20:55:53 GMT
ENV KIBANA_MAJOR=4.6
# Tue, 21 Mar 2017 20:55:53 GMT
ENV KIBANA_VERSION=4.6.4
# Tue, 21 Mar 2017 20:55:54 GMT
RUN echo "deb http://packages.elastic.co/kibana/${KIBANA_MAJOR}/debian stable main" > /etc/apt/sources.list.d/kibana.list
# Tue, 21 Mar 2017 20:56:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
# Tue, 21 Mar 2017 20:56:10 GMT
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 20:56:10 GMT
COPY file:1afe35294cf65766b0d19e7df5bfc671213b2d4cffe59decdc1cb601f7387d43 in / 
# Tue, 21 Mar 2017 20:56:11 GMT
EXPOSE 5601/tcp
# Tue, 21 Mar 2017 20:56:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Mar 2017 20:56:11 GMT
CMD ["kibana"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da41a38ea23917f9f37673d2c2acd2d08129ab37f09123586a1c72343a99aef9`  
		Last Modified: Thu, 23 Mar 2017 21:53:26 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3b40ba58af6fde7dceb42621eb9e735c9c7fc9053208fe2cd806190f17420f`  
		Last Modified: Thu, 23 Mar 2017 21:53:29 GMT  
		Size: 19.9 MB (19868774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d3cb8d97ce12c4193ccc8899a1ae5ad2befe0c5975e940faff32b7510a4c2a`  
		Last Modified: Thu, 23 Mar 2017 21:53:23 GMT  
		Size: 807.9 KB (807933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c1905b8824fdff7d6251eca4d32f892ee85217611ef97eeadffa5ae0eefda5`  
		Last Modified: Thu, 23 Mar 2017 21:53:23 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c18a2a8b4d0590780084ae94f837642c419d1f066ebaf516d418f731f056bbd`  
		Last Modified: Thu, 23 Mar 2017 21:54:17 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6caf57419bea807c88245a9e58eeb112c51953f758b0344137e20430fdb50a`  
		Last Modified: Thu, 23 Mar 2017 21:54:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6858e5b086bedbc0de7f5f8c0675ed4afcbccf3115ca2b152b0382252050c46`  
		Last Modified: Thu, 23 Mar 2017 21:54:39 GMT  
		Size: 35.9 MB (35925757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25dcce9c6d5f5ebe744455402dd6d740476502bf3a70753fcb6d884bafd91a8d`  
		Last Modified: Thu, 23 Mar 2017 21:54:17 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:4.6`

```console
$ docker pull kibana@sha256:3e0ff21b6cee87531877f3373217eaee594702127e61d37fd46c33fa31ed4737
```

-	Platforms:
	-	linux; amd64

### `kibana:4.6` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108054417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468a1e1f2b33b7aa28baa362c02b19dafac08ea725cbdabb7f9f5783dc4a0563`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kibana"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:55:30 GMT
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
# Tue, 21 Mar 2017 20:55:43 GMT
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 		libfontconfig 		libfreetype6 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:55:43 GMT
ENV GOSU_VERSION=1.7
# Tue, 21 Mar 2017 20:55:48 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 21 Mar 2017 20:55:48 GMT
ENV TINI_VERSION=v0.9.0
# Tue, 21 Mar 2017 20:55:51 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Tue, 21 Mar 2017 20:55:52 GMT
RUN set -ex; 	key='46095ACC8548582C1A2699A9D27D666CD88E42B4'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/elastic.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 21 Mar 2017 20:55:53 GMT
ENV KIBANA_MAJOR=4.6
# Tue, 21 Mar 2017 20:55:53 GMT
ENV KIBANA_VERSION=4.6.4
# Tue, 21 Mar 2017 20:55:54 GMT
RUN echo "deb http://packages.elastic.co/kibana/${KIBANA_MAJOR}/debian stable main" > /etc/apt/sources.list.d/kibana.list
# Tue, 21 Mar 2017 20:56:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
# Tue, 21 Mar 2017 20:56:10 GMT
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 20:56:10 GMT
COPY file:1afe35294cf65766b0d19e7df5bfc671213b2d4cffe59decdc1cb601f7387d43 in / 
# Tue, 21 Mar 2017 20:56:11 GMT
EXPOSE 5601/tcp
# Tue, 21 Mar 2017 20:56:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Mar 2017 20:56:11 GMT
CMD ["kibana"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da41a38ea23917f9f37673d2c2acd2d08129ab37f09123586a1c72343a99aef9`  
		Last Modified: Thu, 23 Mar 2017 21:53:26 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3b40ba58af6fde7dceb42621eb9e735c9c7fc9053208fe2cd806190f17420f`  
		Last Modified: Thu, 23 Mar 2017 21:53:29 GMT  
		Size: 19.9 MB (19868774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d3cb8d97ce12c4193ccc8899a1ae5ad2befe0c5975e940faff32b7510a4c2a`  
		Last Modified: Thu, 23 Mar 2017 21:53:23 GMT  
		Size: 807.9 KB (807933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c1905b8824fdff7d6251eca4d32f892ee85217611ef97eeadffa5ae0eefda5`  
		Last Modified: Thu, 23 Mar 2017 21:53:23 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c18a2a8b4d0590780084ae94f837642c419d1f066ebaf516d418f731f056bbd`  
		Last Modified: Thu, 23 Mar 2017 21:54:17 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6caf57419bea807c88245a9e58eeb112c51953f758b0344137e20430fdb50a`  
		Last Modified: Thu, 23 Mar 2017 21:54:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6858e5b086bedbc0de7f5f8c0675ed4afcbccf3115ca2b152b0382252050c46`  
		Last Modified: Thu, 23 Mar 2017 21:54:39 GMT  
		Size: 35.9 MB (35925757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25dcce9c6d5f5ebe744455402dd6d740476502bf3a70753fcb6d884bafd91a8d`  
		Last Modified: Thu, 23 Mar 2017 21:54:17 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:4`

```console
$ docker pull kibana@sha256:3e0ff21b6cee87531877f3373217eaee594702127e61d37fd46c33fa31ed4737
```

-	Platforms:
	-	linux; amd64

### `kibana:4` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108054417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468a1e1f2b33b7aa28baa362c02b19dafac08ea725cbdabb7f9f5783dc4a0563`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kibana"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:55:30 GMT
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
# Tue, 21 Mar 2017 20:55:43 GMT
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 		libfontconfig 		libfreetype6 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:55:43 GMT
ENV GOSU_VERSION=1.7
# Tue, 21 Mar 2017 20:55:48 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 21 Mar 2017 20:55:48 GMT
ENV TINI_VERSION=v0.9.0
# Tue, 21 Mar 2017 20:55:51 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Tue, 21 Mar 2017 20:55:52 GMT
RUN set -ex; 	key='46095ACC8548582C1A2699A9D27D666CD88E42B4'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/elastic.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 21 Mar 2017 20:55:53 GMT
ENV KIBANA_MAJOR=4.6
# Tue, 21 Mar 2017 20:55:53 GMT
ENV KIBANA_VERSION=4.6.4
# Tue, 21 Mar 2017 20:55:54 GMT
RUN echo "deb http://packages.elastic.co/kibana/${KIBANA_MAJOR}/debian stable main" > /etc/apt/sources.list.d/kibana.list
# Tue, 21 Mar 2017 20:56:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
# Tue, 21 Mar 2017 20:56:10 GMT
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 20:56:10 GMT
COPY file:1afe35294cf65766b0d19e7df5bfc671213b2d4cffe59decdc1cb601f7387d43 in / 
# Tue, 21 Mar 2017 20:56:11 GMT
EXPOSE 5601/tcp
# Tue, 21 Mar 2017 20:56:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Mar 2017 20:56:11 GMT
CMD ["kibana"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da41a38ea23917f9f37673d2c2acd2d08129ab37f09123586a1c72343a99aef9`  
		Last Modified: Thu, 23 Mar 2017 21:53:26 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3b40ba58af6fde7dceb42621eb9e735c9c7fc9053208fe2cd806190f17420f`  
		Last Modified: Thu, 23 Mar 2017 21:53:29 GMT  
		Size: 19.9 MB (19868774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d3cb8d97ce12c4193ccc8899a1ae5ad2befe0c5975e940faff32b7510a4c2a`  
		Last Modified: Thu, 23 Mar 2017 21:53:23 GMT  
		Size: 807.9 KB (807933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c1905b8824fdff7d6251eca4d32f892ee85217611ef97eeadffa5ae0eefda5`  
		Last Modified: Thu, 23 Mar 2017 21:53:23 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c18a2a8b4d0590780084ae94f837642c419d1f066ebaf516d418f731f056bbd`  
		Last Modified: Thu, 23 Mar 2017 21:54:17 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6caf57419bea807c88245a9e58eeb112c51953f758b0344137e20430fdb50a`  
		Last Modified: Thu, 23 Mar 2017 21:54:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6858e5b086bedbc0de7f5f8c0675ed4afcbccf3115ca2b152b0382252050c46`  
		Last Modified: Thu, 23 Mar 2017 21:54:39 GMT  
		Size: 35.9 MB (35925757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25dcce9c6d5f5ebe744455402dd6d740476502bf3a70753fcb6d884bafd91a8d`  
		Last Modified: Thu, 23 Mar 2017 21:54:17 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:4.1.11`

```console
$ docker pull kibana@sha256:94a4acf93d443d14891dbb4c5a132f503d04096ba474d879061393df9f4d9e59
```

-	Platforms:
	-	linux; amd64

### `kibana:4.1.11` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91132965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c60eb45abf3d6f3e5c714ee3856b41dae69aae486d009a1835b7467b46a5970`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kibana"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:55:30 GMT
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
# Tue, 21 Mar 2017 20:55:43 GMT
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 		libfontconfig 		libfreetype6 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:55:43 GMT
ENV GOSU_VERSION=1.7
# Tue, 21 Mar 2017 20:55:48 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 21 Mar 2017 20:55:48 GMT
ENV TINI_VERSION=v0.9.0
# Tue, 21 Mar 2017 20:55:51 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Tue, 21 Mar 2017 20:56:12 GMT
ENV KIBANA_VERSION=4.1.11
# Tue, 21 Mar 2017 20:56:13 GMT
ENV KIBANA_SHA1=13655cf94f5c47e8ab4d94c8170128f63be46ad5
# Tue, 21 Mar 2017 20:56:18 GMT
RUN set -x 	&& wget -O kibana.tar.gz "https://download.elastic.co/kibana/kibana/kibana-${KIBANA_VERSION}-linux-x64.tar.gz" 	&& echo "${KIBANA_SHA1} *kibana.tar.gz" | sha1sum -c - 	&& mkdir -p /opt/kibana 	&& tar -xz --strip-components=1 -C /opt/kibana -f kibana.tar.gz 	&& chown -R kibana:kibana /opt/kibana 	&& rm kibana.tar.gz 		&& sed -ri "s!^(\#\s*)?(elasticsearch_url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
# Tue, 21 Mar 2017 20:56:19 GMT
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 20:56:19 GMT
COPY file:1ad4c14d23fc99eff1a91bced98f992e275b430cc6f63f5ad27bf5e6b929be00 in / 
# Tue, 21 Mar 2017 20:56:20 GMT
EXPOSE 5601/tcp
# Tue, 21 Mar 2017 20:56:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Mar 2017 20:56:20 GMT
CMD ["kibana"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da41a38ea23917f9f37673d2c2acd2d08129ab37f09123586a1c72343a99aef9`  
		Last Modified: Thu, 23 Mar 2017 21:53:26 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3b40ba58af6fde7dceb42621eb9e735c9c7fc9053208fe2cd806190f17420f`  
		Last Modified: Thu, 23 Mar 2017 21:53:29 GMT  
		Size: 19.9 MB (19868774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d3cb8d97ce12c4193ccc8899a1ae5ad2befe0c5975e940faff32b7510a4c2a`  
		Last Modified: Thu, 23 Mar 2017 21:53:23 GMT  
		Size: 807.9 KB (807933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c1905b8824fdff7d6251eca4d32f892ee85217611ef97eeadffa5ae0eefda5`  
		Last Modified: Thu, 23 Mar 2017 21:53:23 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b7bcbf51c15114b8d94ae652f60e9ab771a651f5fb58ef0bc99b23c1a34e91`  
		Last Modified: Thu, 23 Mar 2017 21:53:35 GMT  
		Size: 19.0 MB (19005967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdf5d6c6d4d58116e3028666c90880f9ab58f9437c21ab1b736c9d5212f4277`  
		Last Modified: Thu, 23 Mar 2017 21:53:24 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:4.1`

```console
$ docker pull kibana@sha256:94a4acf93d443d14891dbb4c5a132f503d04096ba474d879061393df9f4d9e59
```

-	Platforms:
	-	linux; amd64

### `kibana:4.1` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91132965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c60eb45abf3d6f3e5c714ee3856b41dae69aae486d009a1835b7467b46a5970`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kibana"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:55:30 GMT
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
# Tue, 21 Mar 2017 20:55:43 GMT
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 		libfontconfig 		libfreetype6 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:55:43 GMT
ENV GOSU_VERSION=1.7
# Tue, 21 Mar 2017 20:55:48 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 21 Mar 2017 20:55:48 GMT
ENV TINI_VERSION=v0.9.0
# Tue, 21 Mar 2017 20:55:51 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Tue, 21 Mar 2017 20:56:12 GMT
ENV KIBANA_VERSION=4.1.11
# Tue, 21 Mar 2017 20:56:13 GMT
ENV KIBANA_SHA1=13655cf94f5c47e8ab4d94c8170128f63be46ad5
# Tue, 21 Mar 2017 20:56:18 GMT
RUN set -x 	&& wget -O kibana.tar.gz "https://download.elastic.co/kibana/kibana/kibana-${KIBANA_VERSION}-linux-x64.tar.gz" 	&& echo "${KIBANA_SHA1} *kibana.tar.gz" | sha1sum -c - 	&& mkdir -p /opt/kibana 	&& tar -xz --strip-components=1 -C /opt/kibana -f kibana.tar.gz 	&& chown -R kibana:kibana /opt/kibana 	&& rm kibana.tar.gz 		&& sed -ri "s!^(\#\s*)?(elasticsearch_url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
# Tue, 21 Mar 2017 20:56:19 GMT
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2017 20:56:19 GMT
COPY file:1ad4c14d23fc99eff1a91bced98f992e275b430cc6f63f5ad27bf5e6b929be00 in / 
# Tue, 21 Mar 2017 20:56:20 GMT
EXPOSE 5601/tcp
# Tue, 21 Mar 2017 20:56:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Mar 2017 20:56:20 GMT
CMD ["kibana"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da41a38ea23917f9f37673d2c2acd2d08129ab37f09123586a1c72343a99aef9`  
		Last Modified: Thu, 23 Mar 2017 21:53:26 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3b40ba58af6fde7dceb42621eb9e735c9c7fc9053208fe2cd806190f17420f`  
		Last Modified: Thu, 23 Mar 2017 21:53:29 GMT  
		Size: 19.9 MB (19868774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d3cb8d97ce12c4193ccc8899a1ae5ad2befe0c5975e940faff32b7510a4c2a`  
		Last Modified: Thu, 23 Mar 2017 21:53:23 GMT  
		Size: 807.9 KB (807933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c1905b8824fdff7d6251eca4d32f892ee85217611ef97eeadffa5ae0eefda5`  
		Last Modified: Thu, 23 Mar 2017 21:53:23 GMT  
		Size: 7.1 KB (7122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b7bcbf51c15114b8d94ae652f60e9ab771a651f5fb58ef0bc99b23c1a34e91`  
		Last Modified: Thu, 23 Mar 2017 21:53:35 GMT  
		Size: 19.0 MB (19005967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdf5d6c6d4d58116e3028666c90880f9ab58f9437c21ab1b736c9d5212f4277`  
		Last Modified: Thu, 23 Mar 2017 21:53:24 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
