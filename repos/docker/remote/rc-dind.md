## `docker:rc-dind`

```console
$ docker pull docker@sha256:b1f1b3e3d6e3aa9e52231d9dd916dc8867d64aaf5ff6f8fdc7fec0305ab7c95b
```

-	Platforms:
	-	linux; amd64

### `docker:rc-dind` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35026265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68133536a81d49aaff0d54eeee9c97ad335dc69a474a948957b2fd8fcec03f31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Fri, 03 Mar 2017 21:48:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl
# Wed, 22 Mar 2017 23:46:00 GMT
ENV DOCKER_BUCKET=test.docker.com
# Thu, 13 Apr 2017 19:00:18 GMT
ENV DOCKER_VERSION=17.05.0-ce-rc1
# Thu, 13 Apr 2017 19:00:19 GMT
ENV DOCKER_SHA256=4561742c2174c01ffd0679621b66d29f8a504240d79aa714f6c58348979d02c6
# Thu, 13 Apr 2017 19:00:25 GMT
RUN set -x 	&& curl -fSL "https://${DOCKER_BUCKET}/builds/Linux/x86_64/docker-${DOCKER_VERSION}.tgz" -o docker.tgz 	&& echo "${DOCKER_SHA256} *docker.tgz" | sha256sum -c - 	&& tar -xzvf docker.tgz 	&& mv docker/* /usr/local/bin/ 	&& rmdir docker 	&& rm docker.tgz 	&& docker -v
# Thu, 13 Apr 2017 19:00:38 GMT
COPY file:a8b1446f032ff01ac092c29a0af328f0b9d47bbee72d1049499f2a9a89ee988a in /usr/local/bin/ 
# Thu, 13 Apr 2017 19:00:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Apr 2017 19:00:40 GMT
CMD ["sh"]
# Thu, 13 Apr 2017 19:01:14 GMT
RUN apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		xfsprogs 		xz
# Thu, 13 Apr 2017 19:01:15 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 13 Apr 2017 19:01:32 GMT
ENV DIND_COMMIT=3b5fac462d21ca164b3778647420016315289034
# Thu, 13 Apr 2017 19:01:34 GMT
RUN wget "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind" -O /usr/local/bin/dind 	&& chmod +x /usr/local/bin/dind
# Thu, 13 Apr 2017 19:01:35 GMT
COPY file:7070e4b35c137a8ec5904300d19b8f7ee74aa76659517767c617249cece98a4a in /usr/local/bin/ 
# Thu, 13 Apr 2017 19:01:36 GMT
VOLUME [/var/lib/docker]
# Thu, 13 Apr 2017 19:01:36 GMT
EXPOSE 2375/tcp
# Thu, 13 Apr 2017 19:01:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 13 Apr 2017 19:01:38 GMT
CMD []
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed492db3a66ce1d7073597aa9d3c6715468e3804abe6d8a0ba6790f61c3fe65`  
		Last Modified: Sat, 04 Mar 2017 04:39:06 GMT  
		Size: 2.2 MB (2167713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e23620b67df2cab8f5d89e308d3446df5223edd3d19042dd135cc18298dac8`  
		Last Modified: Thu, 13 Apr 2017 19:02:30 GMT  
		Size: 28.8 MB (28783157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c43de99df3228bf3d40ee6e72b05d9dab4feabe55380f1a773b0d67800a1ab`  
		Last Modified: Thu, 13 Apr 2017 19:02:24 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c91daf85a0bfac4538e826110179b9ce2876e8da64ca66599210fc197ba8b`  
		Last Modified: Thu, 13 Apr 2017 19:04:30 GMT  
		Size: 2.2 MB (2166029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3457b81321bf8a77ec94657f41b6bae9c9a972498aac5c5628add632ed116aa`  
		Last Modified: Thu, 13 Apr 2017 19:04:28 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd54d08e535b2f750d9294a8f23cb771659b50a4057564c1c0e6103214d2f06`  
		Last Modified: Thu, 13 Apr 2017 19:04:28 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a082f960a417a071953b59479bfb1dded2e37ad2d84ea6e27f725a4123de0abd`  
		Last Modified: Thu, 13 Apr 2017 19:04:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
