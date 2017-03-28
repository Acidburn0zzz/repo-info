<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:0.6.4`](#vault064)
-	[`vault:0.6.5`](#vault065)
-	[`vault:0.7.0`](#vault070)
-	[`vault:latest`](#vaultlatest)

## `vault:0.6.4`

```console
$ docker pull vault@sha256:ebc250d1de4c20bd613b6917eb9457db5eefa404f5f894de105efa70f04b24bb
```

-	Platforms:
	-	linux; amd64

### `vault:0.6.4` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15985734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef9b4d54155ab4367252aae3f5670024331c302cc290fc9cc2afb7bf14cfe90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:21 GMT
ADD file:3df55c321c1c8d73f22bc69240c0764290d6cb293da46ba8f94ed25473fb5853 in / 
# Fri, 03 Mar 2017 23:48:52 GMT
MAINTAINER Jeff Mitchell <jeff@hashicorp.com> (@jefferai)
# Fri, 03 Mar 2017 23:49:43 GMT
ENV VAULT_VERSION=0.6.4
# Fri, 03 Mar 2017 23:49:44 GMT
ENV DOCKER_BASE_VERSION=0.0.4
# Fri, 03 Mar 2017 23:49:45 GMT
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 03 Mar 2017 23:49:55 GMT
RUN apk add --no-cache ca-certificates gnupg openssl libcap &&     gpg --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     grep ${DOCKER_BASE_VERSION}_linux_amd64.zip docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS | sha256sum -c &&     unzip docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     cp bin/gosu bin/dumb-init /bin &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_amd64.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_amd64.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 03 Mar 2017 23:49:56 GMT
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 03 Mar 2017 23:49:56 GMT
VOLUME [/vault/logs]
# Fri, 03 Mar 2017 23:49:57 GMT
VOLUME [/vault/file]
# Fri, 03 Mar 2017 23:49:57 GMT
EXPOSE 8200/tcp
# Fri, 03 Mar 2017 23:49:57 GMT
COPY file:ba639bce844e294b4d0251427ff66d5b257eca29d400982328a19a258fb09db9 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Mar 2017 23:49:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Mar 2017 23:49:58 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7095154754192bfc2306f3b2b841ef82771b7ad39526537234adb1e74ae81a93`  
		Last Modified: Fri, 03 Mar 2017 20:34:19 GMT  
		Size: 2.3 MB (2313384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c46c4fe498018a9d8cfeb48016f2d325b6f66f77f04cec802f5b57498f7de39`  
		Last Modified: Sat, 04 Mar 2017 06:36:36 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2544d626998dddbc6051c1abb63e0d8ffca77d8c7ba8477b6e15a6bac94411`  
		Last Modified: Sat, 04 Mar 2017 06:36:45 GMT  
		Size: 13.7 MB (13669177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e9d914b468d6178a192d76953f06847707a2326b1ce660e702753cd281716f`  
		Last Modified: Sat, 04 Mar 2017 06:36:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5af2f9c6c01f75186b03e8ed5322cda9fdb0021d663899f3bfd6b5165b5a8e`  
		Last Modified: Sat, 04 Mar 2017 06:36:35 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:0.6.5`

```console
$ docker pull vault@sha256:d94bef21674d739961ad45c350a61da30a5f577b709b80270d6da6f9aa209c2a
```

-	Platforms:
	-	linux; amd64

### `vault:0.6.5` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bf6d4a6a62562bc659a057a2587ac1940218080a2fbce94ad952fa1f63e990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:21 GMT
ADD file:3df55c321c1c8d73f22bc69240c0764290d6cb293da46ba8f94ed25473fb5853 in / 
# Fri, 03 Mar 2017 23:48:52 GMT
MAINTAINER Jeff Mitchell <jeff@hashicorp.com> (@jefferai)
# Fri, 03 Mar 2017 23:48:52 GMT
ENV VAULT_VERSION=0.6.5
# Fri, 03 Mar 2017 23:48:52 GMT
ENV DOCKER_BASE_VERSION=0.0.4
# Fri, 03 Mar 2017 23:48:53 GMT
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 03 Mar 2017 23:49:08 GMT
RUN apk add --no-cache ca-certificates gnupg openssl libcap &&     gpg --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     grep ${DOCKER_BASE_VERSION}_linux_amd64.zip docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS | sha256sum -c &&     unzip docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     cp bin/gosu bin/dumb-init /bin &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_amd64.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_amd64.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 03 Mar 2017 23:49:09 GMT
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 03 Mar 2017 23:49:09 GMT
VOLUME [/vault/logs]
# Fri, 03 Mar 2017 23:49:09 GMT
VOLUME [/vault/file]
# Fri, 03 Mar 2017 23:49:10 GMT
EXPOSE 8200/tcp
# Fri, 03 Mar 2017 23:49:10 GMT
COPY file:ba639bce844e294b4d0251427ff66d5b257eca29d400982328a19a258fb09db9 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Mar 2017 23:49:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Mar 2017 23:49:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7095154754192bfc2306f3b2b841ef82771b7ad39526537234adb1e74ae81a93`  
		Last Modified: Fri, 03 Mar 2017 20:34:19 GMT  
		Size: 2.3 MB (2313384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892c730be4b8d1b0280bd4bd74b00d861b18159a3316f678f4e6e77fdffff961`  
		Last Modified: Sat, 04 Mar 2017 06:34:21 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef5d465a63bb2af48e35c06f7fc1e3aa8b8a105f5e29ce96825fde1c25ceefb`  
		Last Modified: Sat, 04 Mar 2017 06:34:29 GMT  
		Size: 14.7 MB (14676444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ea3a699db2f82ee4ad753d256242f2e33a8968c72340318a25bcb2d7e2f1d3`  
		Last Modified: Sat, 04 Mar 2017 06:34:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb69a55b7a725aac8a36ca854367b72478a1ca21c8279d670cdcf8e557731e`  
		Last Modified: Sat, 04 Mar 2017 06:34:22 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:0.7.0`

```console
$ docker pull vault@sha256:b0e8b52a8932f486cfecbf1d1ba402bfd81befd97f746bd984f1f7f8a3ce168a
```

-	Platforms:
	-	linux; amd64

### `vault:0.7.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17252529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144fecac962b683dce553f5d4220c76cb2b59274ab7969814fdccdf1d455ea77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:21 GMT
ADD file:3df55c321c1c8d73f22bc69240c0764290d6cb293da46ba8f94ed25473fb5853 in / 
# Fri, 03 Mar 2017 23:48:52 GMT
MAINTAINER Jeff Mitchell <jeff@hashicorp.com> (@jefferai)
# Tue, 28 Mar 2017 17:35:37 GMT
ENV VAULT_VERSION=0.7.0
# Tue, 28 Mar 2017 17:35:38 GMT
ENV DOCKER_BASE_VERSION=0.0.4
# Tue, 28 Mar 2017 17:35:39 GMT
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 28 Mar 2017 17:35:59 GMT
RUN apk add --no-cache ca-certificates gnupg openssl libcap jq &&     gpg --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     grep ${DOCKER_BASE_VERSION}_linux_amd64.zip docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS | sha256sum -c &&     unzip docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     cp bin/gosu bin/dumb-init /bin &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_amd64.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_amd64.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 28 Mar 2017 17:36:00 GMT
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 28 Mar 2017 17:36:01 GMT
VOLUME [/vault/logs]
# Tue, 28 Mar 2017 17:36:02 GMT
VOLUME [/vault/file]
# Tue, 28 Mar 2017 17:36:02 GMT
EXPOSE 8200/tcp
# Tue, 28 Mar 2017 17:36:03 GMT
COPY file:f15519a2e908ed6cee6fe9e20257ff5316c0e9e5838295e8956e7f5b12a27da5 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 28 Mar 2017 17:36:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Mar 2017 17:36:05 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7095154754192bfc2306f3b2b841ef82771b7ad39526537234adb1e74ae81a93`  
		Last Modified: Fri, 03 Mar 2017 20:34:19 GMT  
		Size: 2.3 MB (2313384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e249a6443b186b3e69e492142f7377d07c23eb01e926c3f949469a725685358d`  
		Last Modified: Tue, 28 Mar 2017 17:37:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8d84a37751dccd5885c5b6bb66b218c16881a613ae5b96dc3550b389820a8b`  
		Last Modified: Tue, 28 Mar 2017 17:37:11 GMT  
		Size: 14.9 MB (14935953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124ed962ab5de9ca81aede1de74c27f003b3ac77dbd72e46024404f45efb3b4f`  
		Last Modified: Tue, 28 Mar 2017 17:37:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b2f3096b75f1bb461e27d42f7c6d18efc98fe8e3d6408b229f75df90034749`  
		Last Modified: Tue, 28 Mar 2017 17:37:06 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:d94bef21674d739961ad45c350a61da30a5f577b709b80270d6da6f9aa209c2a
```

-	Platforms:
	-	linux; amd64

### `vault:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bf6d4a6a62562bc659a057a2587ac1940218080a2fbce94ad952fa1f63e990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:21 GMT
ADD file:3df55c321c1c8d73f22bc69240c0764290d6cb293da46ba8f94ed25473fb5853 in / 
# Fri, 03 Mar 2017 23:48:52 GMT
MAINTAINER Jeff Mitchell <jeff@hashicorp.com> (@jefferai)
# Fri, 03 Mar 2017 23:48:52 GMT
ENV VAULT_VERSION=0.6.5
# Fri, 03 Mar 2017 23:48:52 GMT
ENV DOCKER_BASE_VERSION=0.0.4
# Fri, 03 Mar 2017 23:48:53 GMT
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 03 Mar 2017 23:49:08 GMT
RUN apk add --no-cache ca-certificates gnupg openssl libcap &&     gpg --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     grep ${DOCKER_BASE_VERSION}_linux_amd64.zip docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS | sha256sum -c &&     unzip docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     cp bin/gosu bin/dumb-init /bin &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_amd64.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_amd64.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 03 Mar 2017 23:49:09 GMT
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 03 Mar 2017 23:49:09 GMT
VOLUME [/vault/logs]
# Fri, 03 Mar 2017 23:49:09 GMT
VOLUME [/vault/file]
# Fri, 03 Mar 2017 23:49:10 GMT
EXPOSE 8200/tcp
# Fri, 03 Mar 2017 23:49:10 GMT
COPY file:ba639bce844e294b4d0251427ff66d5b257eca29d400982328a19a258fb09db9 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Mar 2017 23:49:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Mar 2017 23:49:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7095154754192bfc2306f3b2b841ef82771b7ad39526537234adb1e74ae81a93`  
		Last Modified: Fri, 03 Mar 2017 20:34:19 GMT  
		Size: 2.3 MB (2313384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892c730be4b8d1b0280bd4bd74b00d861b18159a3316f678f4e6e77fdffff961`  
		Last Modified: Sat, 04 Mar 2017 06:34:21 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef5d465a63bb2af48e35c06f7fc1e3aa8b8a105f5e29ce96825fde1c25ceefb`  
		Last Modified: Sat, 04 Mar 2017 06:34:29 GMT  
		Size: 14.7 MB (14676444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ea3a699db2f82ee4ad753d256242f2e33a8968c72340318a25bcb2d7e2f1d3`  
		Last Modified: Sat, 04 Mar 2017 06:34:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb69a55b7a725aac8a36ca854367b72478a1ca21c8279d670cdcf8e557731e`  
		Last Modified: Sat, 04 Mar 2017 06:34:22 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
