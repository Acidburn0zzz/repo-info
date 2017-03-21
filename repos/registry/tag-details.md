<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.6`](#registry26)
-	[`registry:2.6.0`](#registry260)
-	[`registry:latest`](#registrylatest)
-	[`registry:2.6.1-rc.2`](#registry261-rc2)

## `registry:2`

```console
$ docker pull registry@sha256:28be0609f90ef53e86e1872a11d672434ce1361711760cf1fe059efd222f8d37
```

-	Platforms:
	-	linux; amd64

### `registry:2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10492049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047218491f8cef3987c8a248b8a4ebc46025b04d7b700f711c320a290959a8a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:21 GMT
ADD file:3df55c321c1c8d73f22bc69240c0764290d6cb293da46ba8f94ed25473fb5853 in / 
# Fri, 03 Mar 2017 23:33:54 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Fri, 03 Mar 2017 23:33:54 GMT
COPY file:6ccb0558ad0a49a3f19a99428209cf72cb67a21381c8e4286365d5e0aebebd50 in /bin/registry 
# Fri, 03 Mar 2017 23:33:55 GMT
COPY file:6c4758d509045dc45381fa2df2e7ffcc661afcaa29805c75f8f1976f2b016db8 in /etc/docker/registry/config.yml 
# Fri, 03 Mar 2017 23:33:55 GMT
VOLUME [/var/lib/registry]
# Fri, 03 Mar 2017 23:33:55 GMT
EXPOSE 5000/tcp
# Fri, 03 Mar 2017 23:33:56 GMT
COPY file:7b57f7ab1a8cf85c00768560fffc926543a60c9c9f7a2b172767dcc9a3203394 in /entrypoint.sh 
# Fri, 03 Mar 2017 23:33:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Mar 2017 23:33:56 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7095154754192bfc2306f3b2b841ef82771b7ad39526537234adb1e74ae81a93`  
		Last Modified: Fri, 03 Mar 2017 20:34:19 GMT  
		Size: 2.3 MB (2313384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6e278d8f96410ac642cd0ec87254db46ed449b140b0a37dbbcceb9f6518c67`  
		Last Modified: Sat, 04 Mar 2017 05:49:43 GMT  
		Size: 2.0 MB (1974427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16218e264e887922e96872e8437ba05999c3e7926e443c27cf8b85a2b56c2c24`  
		Last Modified: Sat, 04 Mar 2017 05:49:42 GMT  
		Size: 6.2 MB (6203649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16748da81f632ba3fe62e3db0df3ef3e86f8e054052a3ccda4447ed5769066f8`  
		Last Modified: Sat, 04 Mar 2017 05:49:35 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d73e673c34c13c31e74bee594054cad249b2e09d4ca2b04a1d4941ef388d950`  
		Last Modified: Sat, 04 Mar 2017 05:49:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.6`

```console
$ docker pull registry@sha256:28be0609f90ef53e86e1872a11d672434ce1361711760cf1fe059efd222f8d37
```

-	Platforms:
	-	linux; amd64

### `registry:2.6` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10492049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047218491f8cef3987c8a248b8a4ebc46025b04d7b700f711c320a290959a8a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:21 GMT
ADD file:3df55c321c1c8d73f22bc69240c0764290d6cb293da46ba8f94ed25473fb5853 in / 
# Fri, 03 Mar 2017 23:33:54 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Fri, 03 Mar 2017 23:33:54 GMT
COPY file:6ccb0558ad0a49a3f19a99428209cf72cb67a21381c8e4286365d5e0aebebd50 in /bin/registry 
# Fri, 03 Mar 2017 23:33:55 GMT
COPY file:6c4758d509045dc45381fa2df2e7ffcc661afcaa29805c75f8f1976f2b016db8 in /etc/docker/registry/config.yml 
# Fri, 03 Mar 2017 23:33:55 GMT
VOLUME [/var/lib/registry]
# Fri, 03 Mar 2017 23:33:55 GMT
EXPOSE 5000/tcp
# Fri, 03 Mar 2017 23:33:56 GMT
COPY file:7b57f7ab1a8cf85c00768560fffc926543a60c9c9f7a2b172767dcc9a3203394 in /entrypoint.sh 
# Fri, 03 Mar 2017 23:33:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Mar 2017 23:33:56 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7095154754192bfc2306f3b2b841ef82771b7ad39526537234adb1e74ae81a93`  
		Last Modified: Fri, 03 Mar 2017 20:34:19 GMT  
		Size: 2.3 MB (2313384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6e278d8f96410ac642cd0ec87254db46ed449b140b0a37dbbcceb9f6518c67`  
		Last Modified: Sat, 04 Mar 2017 05:49:43 GMT  
		Size: 2.0 MB (1974427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16218e264e887922e96872e8437ba05999c3e7926e443c27cf8b85a2b56c2c24`  
		Last Modified: Sat, 04 Mar 2017 05:49:42 GMT  
		Size: 6.2 MB (6203649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16748da81f632ba3fe62e3db0df3ef3e86f8e054052a3ccda4447ed5769066f8`  
		Last Modified: Sat, 04 Mar 2017 05:49:35 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d73e673c34c13c31e74bee594054cad249b2e09d4ca2b04a1d4941ef388d950`  
		Last Modified: Sat, 04 Mar 2017 05:49:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.6.0`

```console
$ docker pull registry@sha256:28be0609f90ef53e86e1872a11d672434ce1361711760cf1fe059efd222f8d37
```

-	Platforms:
	-	linux; amd64

### `registry:2.6.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10492049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047218491f8cef3987c8a248b8a4ebc46025b04d7b700f711c320a290959a8a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:21 GMT
ADD file:3df55c321c1c8d73f22bc69240c0764290d6cb293da46ba8f94ed25473fb5853 in / 
# Fri, 03 Mar 2017 23:33:54 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Fri, 03 Mar 2017 23:33:54 GMT
COPY file:6ccb0558ad0a49a3f19a99428209cf72cb67a21381c8e4286365d5e0aebebd50 in /bin/registry 
# Fri, 03 Mar 2017 23:33:55 GMT
COPY file:6c4758d509045dc45381fa2df2e7ffcc661afcaa29805c75f8f1976f2b016db8 in /etc/docker/registry/config.yml 
# Fri, 03 Mar 2017 23:33:55 GMT
VOLUME [/var/lib/registry]
# Fri, 03 Mar 2017 23:33:55 GMT
EXPOSE 5000/tcp
# Fri, 03 Mar 2017 23:33:56 GMT
COPY file:7b57f7ab1a8cf85c00768560fffc926543a60c9c9f7a2b172767dcc9a3203394 in /entrypoint.sh 
# Fri, 03 Mar 2017 23:33:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Mar 2017 23:33:56 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7095154754192bfc2306f3b2b841ef82771b7ad39526537234adb1e74ae81a93`  
		Last Modified: Fri, 03 Mar 2017 20:34:19 GMT  
		Size: 2.3 MB (2313384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6e278d8f96410ac642cd0ec87254db46ed449b140b0a37dbbcceb9f6518c67`  
		Last Modified: Sat, 04 Mar 2017 05:49:43 GMT  
		Size: 2.0 MB (1974427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16218e264e887922e96872e8437ba05999c3e7926e443c27cf8b85a2b56c2c24`  
		Last Modified: Sat, 04 Mar 2017 05:49:42 GMT  
		Size: 6.2 MB (6203649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16748da81f632ba3fe62e3db0df3ef3e86f8e054052a3ccda4447ed5769066f8`  
		Last Modified: Sat, 04 Mar 2017 05:49:35 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d73e673c34c13c31e74bee594054cad249b2e09d4ca2b04a1d4941ef388d950`  
		Last Modified: Sat, 04 Mar 2017 05:49:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:28be0609f90ef53e86e1872a11d672434ce1361711760cf1fe059efd222f8d37
```

-	Platforms:
	-	linux; amd64

### `registry:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10492049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047218491f8cef3987c8a248b8a4ebc46025b04d7b700f711c320a290959a8a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:21 GMT
ADD file:3df55c321c1c8d73f22bc69240c0764290d6cb293da46ba8f94ed25473fb5853 in / 
# Fri, 03 Mar 2017 23:33:54 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Fri, 03 Mar 2017 23:33:54 GMT
COPY file:6ccb0558ad0a49a3f19a99428209cf72cb67a21381c8e4286365d5e0aebebd50 in /bin/registry 
# Fri, 03 Mar 2017 23:33:55 GMT
COPY file:6c4758d509045dc45381fa2df2e7ffcc661afcaa29805c75f8f1976f2b016db8 in /etc/docker/registry/config.yml 
# Fri, 03 Mar 2017 23:33:55 GMT
VOLUME [/var/lib/registry]
# Fri, 03 Mar 2017 23:33:55 GMT
EXPOSE 5000/tcp
# Fri, 03 Mar 2017 23:33:56 GMT
COPY file:7b57f7ab1a8cf85c00768560fffc926543a60c9c9f7a2b172767dcc9a3203394 in /entrypoint.sh 
# Fri, 03 Mar 2017 23:33:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Mar 2017 23:33:56 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7095154754192bfc2306f3b2b841ef82771b7ad39526537234adb1e74ae81a93`  
		Last Modified: Fri, 03 Mar 2017 20:34:19 GMT  
		Size: 2.3 MB (2313384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6e278d8f96410ac642cd0ec87254db46ed449b140b0a37dbbcceb9f6518c67`  
		Last Modified: Sat, 04 Mar 2017 05:49:43 GMT  
		Size: 2.0 MB (1974427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16218e264e887922e96872e8437ba05999c3e7926e443c27cf8b85a2b56c2c24`  
		Last Modified: Sat, 04 Mar 2017 05:49:42 GMT  
		Size: 6.2 MB (6203649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16748da81f632ba3fe62e3db0df3ef3e86f8e054052a3ccda4447ed5769066f8`  
		Last Modified: Sat, 04 Mar 2017 05:49:35 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d73e673c34c13c31e74bee594054cad249b2e09d4ca2b04a1d4941ef388d950`  
		Last Modified: Sat, 04 Mar 2017 05:49:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.6.1-rc.2`

```console
$ docker pull registry@sha256:4d9cb5b3e8f2f425cb5c4f86d4eb7c3efc3729b8267f248c84a398760586eb47
```

-	Platforms:
	-	linux; amd64

### `registry:2.6.1-rc.2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10491372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04f07715336b7590dc52cd22b80e89a1f6b2e7200e83fdc58a3423b00298381`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:21 GMT
ADD file:3df55c321c1c8d73f22bc69240c0764290d6cb293da46ba8f94ed25473fb5853 in / 
# Fri, 03 Mar 2017 23:33:54 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Tue, 21 Mar 2017 22:14:35 GMT
COPY file:36caf45436ef00e951061f8709671a1df9a8cba34779bc67d9b2b6abace75077 in /bin/registry 
# Tue, 21 Mar 2017 22:14:36 GMT
COPY file:6c4758d509045dc45381fa2df2e7ffcc661afcaa29805c75f8f1976f2b016db8 in /etc/docker/registry/config.yml 
# Tue, 21 Mar 2017 22:14:36 GMT
VOLUME [/var/lib/registry]
# Tue, 21 Mar 2017 22:14:37 GMT
EXPOSE 5000/tcp
# Tue, 21 Mar 2017 22:14:37 GMT
COPY file:7b57f7ab1a8cf85c00768560fffc926543a60c9c9f7a2b172767dcc9a3203394 in /entrypoint.sh 
# Tue, 21 Mar 2017 22:14:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2017 22:14:38 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7095154754192bfc2306f3b2b841ef82771b7ad39526537234adb1e74ae81a93`  
		Last Modified: Fri, 03 Mar 2017 20:34:19 GMT  
		Size: 2.3 MB (2313384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6e278d8f96410ac642cd0ec87254db46ed449b140b0a37dbbcceb9f6518c67`  
		Last Modified: Sat, 04 Mar 2017 05:49:43 GMT  
		Size: 2.0 MB (1974427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f027b7ec9b52045fff7f9e1824a98f04334c4f990d57a94afa01179149f6423f`  
		Last Modified: Tue, 21 Mar 2017 22:49:08 GMT  
		Size: 6.2 MB (6202973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2811c5233e877051fd546c5d2d43e8b136d0b89c19489bdcaeb7f9bec1e7d5f6`  
		Last Modified: Tue, 21 Mar 2017 22:49:06 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a9ab0228175f3bc50940b3f863c21e400050824919b8f0b29d2055ffee1922`  
		Last Modified: Tue, 21 Mar 2017 22:49:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
