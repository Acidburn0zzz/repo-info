<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.1`](#kapacitor11)
-	[`kapacitor:1.1.1`](#kapacitor111)
-	[`kapacitor:1.1-alpine`](#kapacitor11-alpine)
-	[`kapacitor:1.1.1-alpine`](#kapacitor111-alpine)
-	[`kapacitor:1.2`](#kapacitor12)
-	[`kapacitor:1.2.0`](#kapacitor120)
-	[`kapacitor:latest`](#kapacitorlatest)
-	[`kapacitor:1.2-alpine`](#kapacitor12-alpine)
-	[`kapacitor:1.2.0-alpine`](#kapacitor120-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)

## `kapacitor:1.1`

```console
$ docker pull kapacitor@sha256:211bc18126f5173ef6d319f6d9bb68c999c10bac65bac8faabfc4987820f0bd3
```

-	Platforms:
	-	linux; amd64

### `kapacitor:1.1` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79661754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0be164944cbcb15ba5cec683ffec41b7e146c1541062b3269a3fc5ce3ac9fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:14:51 GMT
RUN gpg     --keyserver hkp://ha.pool.sks-keyservers.net     --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5
# Tue, 21 Mar 2017 20:55:14 GMT
ENV KAPACITOR_VERSION=1.1.1
# Tue, 21 Mar 2017 20:55:18 GMT
RUN wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_amd64.deb*
# Tue, 21 Mar 2017 20:55:19 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Tue, 21 Mar 2017 20:55:19 GMT
EXPOSE 9092/tcp
# Tue, 21 Mar 2017 20:55:19 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 21 Mar 2017 20:55:20 GMT
COPY file:e5d90b0779cb7845ca3a7981c04a97fd959fea211a2ce19c8da8b949f9d9d04c in /entrypoint.sh 
# Tue, 21 Mar 2017 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2017 20:55:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726297beaf19be957416750338c095ae15b94adc0e8c1306cebbf113f8b9a5c`  
		Last Modified: Tue, 21 Mar 2017 19:58:58 GMT  
		Size: 18.6 MB (18606479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d75e2f3672c90fad945d048bb41578640b801cc97c2ca3dd9642e60de13ffd`  
		Last Modified: Thu, 23 Mar 2017 17:26:57 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c9260f557bbd2368cdea8aa894799d69834699f83371d9ac2f4ba0599b70c5`  
		Last Modified: Thu, 23 Mar 2017 21:51:32 GMT  
		Size: 9.6 MB (9609594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4a3caa3cbbf2914478611d11747f302e3847320baa2e48265cd06fb56d2c7`  
		Last Modified: Thu, 23 Mar 2017 21:51:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee8221718abed39918eb06d9329d212195a3ef1d15d7ec2fa47cc55243d47a4`  
		Last Modified: Thu, 23 Mar 2017 21:51:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.1.1`

```console
$ docker pull kapacitor@sha256:211bc18126f5173ef6d319f6d9bb68c999c10bac65bac8faabfc4987820f0bd3
```

-	Platforms:
	-	linux; amd64

### `kapacitor:1.1.1` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79661754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0be164944cbcb15ba5cec683ffec41b7e146c1541062b3269a3fc5ce3ac9fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:14:51 GMT
RUN gpg     --keyserver hkp://ha.pool.sks-keyservers.net     --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5
# Tue, 21 Mar 2017 20:55:14 GMT
ENV KAPACITOR_VERSION=1.1.1
# Tue, 21 Mar 2017 20:55:18 GMT
RUN wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_amd64.deb*
# Tue, 21 Mar 2017 20:55:19 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Tue, 21 Mar 2017 20:55:19 GMT
EXPOSE 9092/tcp
# Tue, 21 Mar 2017 20:55:19 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 21 Mar 2017 20:55:20 GMT
COPY file:e5d90b0779cb7845ca3a7981c04a97fd959fea211a2ce19c8da8b949f9d9d04c in /entrypoint.sh 
# Tue, 21 Mar 2017 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2017 20:55:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726297beaf19be957416750338c095ae15b94adc0e8c1306cebbf113f8b9a5c`  
		Last Modified: Tue, 21 Mar 2017 19:58:58 GMT  
		Size: 18.6 MB (18606479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d75e2f3672c90fad945d048bb41578640b801cc97c2ca3dd9642e60de13ffd`  
		Last Modified: Thu, 23 Mar 2017 17:26:57 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c9260f557bbd2368cdea8aa894799d69834699f83371d9ac2f4ba0599b70c5`  
		Last Modified: Thu, 23 Mar 2017 21:51:32 GMT  
		Size: 9.6 MB (9609594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4a3caa3cbbf2914478611d11747f302e3847320baa2e48265cd06fb56d2c7`  
		Last Modified: Thu, 23 Mar 2017 21:51:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee8221718abed39918eb06d9329d212195a3ef1d15d7ec2fa47cc55243d47a4`  
		Last Modified: Thu, 23 Mar 2017 21:51:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.1-alpine`

```console
$ docker pull kapacitor@sha256:649437c21edbc9b7369ec94274098fcb45ca1fd86b3aed054b90a1671a809a86
```

-	Platforms:
	-	linux; amd64

### `kapacitor:1.1-alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8889771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1358fb8de06ed425cc3c1f47efd85bc8a31798e866afe75a425f222981aa53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Wed, 12 Apr 2017 18:58:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 12 Apr 2017 19:05:20 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 12 Apr 2017 19:05:20 GMT
ENV KAPACITOR_VERSION=1.1.1
# Wed, 12 Apr 2017 19:05:28 GMT
RUN apk add --no-cache --virtual .build-deps wget gnupg tar &&     gpg --keyserver hkp://ha.pool.sks-keyservers.net         --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 12 Apr 2017 19:05:29 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Wed, 12 Apr 2017 19:05:30 GMT
EXPOSE 9092/tcp
# Wed, 12 Apr 2017 19:05:32 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 12 Apr 2017 19:05:33 GMT
COPY file:440a837280df72a19ed72b91fab9bdcfd268250b241bbc22509699f880fe0d17 in /entrypoint.sh 
# Wed, 12 Apr 2017 19:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Apr 2017 19:05:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827570184fa82dc6defc05bcf5838dba590096d8add32bb847191bd7232cfcba`  
		Last Modified: Wed, 12 Apr 2017 19:02:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a07567aee09be1af1aec1476fe3261b0b717c05954d31456c578c63429e532`  
		Last Modified: Wed, 12 Apr 2017 19:06:54 GMT  
		Size: 352.8 KB (352777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43a7185b91dea5a5cd94b8f17215c263a56b4d641c9ee879e26025ec2280c7d`  
		Last Modified: Wed, 12 Apr 2017 19:06:55 GMT  
		Size: 6.6 MB (6631118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ddf6645d02a6ce55bd99b0ff6fa3aaabc9be160a201cb92a0e19db12e3f985`  
		Last Modified: Wed, 12 Apr 2017 19:06:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6515d5960374870533ae99a7fff005b612a1e83c9e4c8733e0bc826d8cbb6cd`  
		Last Modified: Wed, 12 Apr 2017 19:06:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.1.1-alpine`

```console
$ docker pull kapacitor@sha256:649437c21edbc9b7369ec94274098fcb45ca1fd86b3aed054b90a1671a809a86
```

-	Platforms:
	-	linux; amd64

### `kapacitor:1.1.1-alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8889771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1358fb8de06ed425cc3c1f47efd85bc8a31798e866afe75a425f222981aa53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Wed, 12 Apr 2017 18:58:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 12 Apr 2017 19:05:20 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 12 Apr 2017 19:05:20 GMT
ENV KAPACITOR_VERSION=1.1.1
# Wed, 12 Apr 2017 19:05:28 GMT
RUN apk add --no-cache --virtual .build-deps wget gnupg tar &&     gpg --keyserver hkp://ha.pool.sks-keyservers.net         --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 12 Apr 2017 19:05:29 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Wed, 12 Apr 2017 19:05:30 GMT
EXPOSE 9092/tcp
# Wed, 12 Apr 2017 19:05:32 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 12 Apr 2017 19:05:33 GMT
COPY file:440a837280df72a19ed72b91fab9bdcfd268250b241bbc22509699f880fe0d17 in /entrypoint.sh 
# Wed, 12 Apr 2017 19:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Apr 2017 19:05:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827570184fa82dc6defc05bcf5838dba590096d8add32bb847191bd7232cfcba`  
		Last Modified: Wed, 12 Apr 2017 19:02:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a07567aee09be1af1aec1476fe3261b0b717c05954d31456c578c63429e532`  
		Last Modified: Wed, 12 Apr 2017 19:06:54 GMT  
		Size: 352.8 KB (352777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43a7185b91dea5a5cd94b8f17215c263a56b4d641c9ee879e26025ec2280c7d`  
		Last Modified: Wed, 12 Apr 2017 19:06:55 GMT  
		Size: 6.6 MB (6631118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ddf6645d02a6ce55bd99b0ff6fa3aaabc9be160a201cb92a0e19db12e3f985`  
		Last Modified: Wed, 12 Apr 2017 19:06:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6515d5960374870533ae99a7fff005b612a1e83c9e4c8733e0bc826d8cbb6cd`  
		Last Modified: Wed, 12 Apr 2017 19:06:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.2`

```console
$ docker pull kapacitor@sha256:6f2c529d00057e3b491694756ae4f90cb4cff73930a7e6687c40f618f939cab8
```

-	Platforms:
	-	linux; amd64

### `kapacitor:1.2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80125249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371ef4328e26517e69b91aabc825fd6fedb5e12cd5c4bdae2a0c0cb7431cc4ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:14:51 GMT
RUN gpg     --keyserver hkp://ha.pool.sks-keyservers.net     --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5
# Tue, 21 Mar 2017 20:55:21 GMT
ENV KAPACITOR_VERSION=1.2.0
# Tue, 21 Mar 2017 20:55:26 GMT
RUN wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_amd64.deb*
# Tue, 21 Mar 2017 20:55:27 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Tue, 21 Mar 2017 20:55:27 GMT
EXPOSE 9092/tcp
# Tue, 21 Mar 2017 20:55:27 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 21 Mar 2017 20:55:28 GMT
COPY file:e5d90b0779cb7845ca3a7981c04a97fd959fea211a2ce19c8da8b949f9d9d04c in /entrypoint.sh 
# Tue, 21 Mar 2017 20:55:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2017 20:55:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726297beaf19be957416750338c095ae15b94adc0e8c1306cebbf113f8b9a5c`  
		Last Modified: Tue, 21 Mar 2017 19:58:58 GMT  
		Size: 18.6 MB (18606479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d75e2f3672c90fad945d048bb41578640b801cc97c2ca3dd9642e60de13ffd`  
		Last Modified: Thu, 23 Mar 2017 17:26:57 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c1f510ac9b560b9242c89dc72d6e3f8a1cfad19917716cdd7de3e203dd0d14`  
		Last Modified: Thu, 23 Mar 2017 21:52:20 GMT  
		Size: 10.1 MB (10073089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa85a348dd00d5a0e391054a58f944bdde70d65c265bc7f8ea4a349993bfedb`  
		Last Modified: Thu, 23 Mar 2017 21:52:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72c5f8f2f56e85f82537c58ea9d3b629f919c74a8d6e3b7e0ed782be008768`  
		Last Modified: Thu, 23 Mar 2017 21:52:16 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.2.0`

```console
$ docker pull kapacitor@sha256:6f2c529d00057e3b491694756ae4f90cb4cff73930a7e6687c40f618f939cab8
```

-	Platforms:
	-	linux; amd64

### `kapacitor:1.2.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80125249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371ef4328e26517e69b91aabc825fd6fedb5e12cd5c4bdae2a0c0cb7431cc4ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:14:51 GMT
RUN gpg     --keyserver hkp://ha.pool.sks-keyservers.net     --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5
# Tue, 21 Mar 2017 20:55:21 GMT
ENV KAPACITOR_VERSION=1.2.0
# Tue, 21 Mar 2017 20:55:26 GMT
RUN wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_amd64.deb*
# Tue, 21 Mar 2017 20:55:27 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Tue, 21 Mar 2017 20:55:27 GMT
EXPOSE 9092/tcp
# Tue, 21 Mar 2017 20:55:27 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 21 Mar 2017 20:55:28 GMT
COPY file:e5d90b0779cb7845ca3a7981c04a97fd959fea211a2ce19c8da8b949f9d9d04c in /entrypoint.sh 
# Tue, 21 Mar 2017 20:55:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2017 20:55:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726297beaf19be957416750338c095ae15b94adc0e8c1306cebbf113f8b9a5c`  
		Last Modified: Tue, 21 Mar 2017 19:58:58 GMT  
		Size: 18.6 MB (18606479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d75e2f3672c90fad945d048bb41578640b801cc97c2ca3dd9642e60de13ffd`  
		Last Modified: Thu, 23 Mar 2017 17:26:57 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c1f510ac9b560b9242c89dc72d6e3f8a1cfad19917716cdd7de3e203dd0d14`  
		Last Modified: Thu, 23 Mar 2017 21:52:20 GMT  
		Size: 10.1 MB (10073089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa85a348dd00d5a0e391054a58f944bdde70d65c265bc7f8ea4a349993bfedb`  
		Last Modified: Thu, 23 Mar 2017 21:52:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72c5f8f2f56e85f82537c58ea9d3b629f919c74a8d6e3b7e0ed782be008768`  
		Last Modified: Thu, 23 Mar 2017 21:52:16 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:6f2c529d00057e3b491694756ae4f90cb4cff73930a7e6687c40f618f939cab8
```

-	Platforms:
	-	linux; amd64

### `kapacitor:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80125249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371ef4328e26517e69b91aabc825fd6fedb5e12cd5c4bdae2a0c0cb7431cc4ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:14:51 GMT
RUN gpg     --keyserver hkp://ha.pool.sks-keyservers.net     --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5
# Tue, 21 Mar 2017 20:55:21 GMT
ENV KAPACITOR_VERSION=1.2.0
# Tue, 21 Mar 2017 20:55:26 GMT
RUN wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_amd64.deb*
# Tue, 21 Mar 2017 20:55:27 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Tue, 21 Mar 2017 20:55:27 GMT
EXPOSE 9092/tcp
# Tue, 21 Mar 2017 20:55:27 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 21 Mar 2017 20:55:28 GMT
COPY file:e5d90b0779cb7845ca3a7981c04a97fd959fea211a2ce19c8da8b949f9d9d04c in /entrypoint.sh 
# Tue, 21 Mar 2017 20:55:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2017 20:55:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726297beaf19be957416750338c095ae15b94adc0e8c1306cebbf113f8b9a5c`  
		Last Modified: Tue, 21 Mar 2017 19:58:58 GMT  
		Size: 18.6 MB (18606479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d75e2f3672c90fad945d048bb41578640b801cc97c2ca3dd9642e60de13ffd`  
		Last Modified: Thu, 23 Mar 2017 17:26:57 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c1f510ac9b560b9242c89dc72d6e3f8a1cfad19917716cdd7de3e203dd0d14`  
		Last Modified: Thu, 23 Mar 2017 21:52:20 GMT  
		Size: 10.1 MB (10073089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa85a348dd00d5a0e391054a58f944bdde70d65c265bc7f8ea4a349993bfedb`  
		Last Modified: Thu, 23 Mar 2017 21:52:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72c5f8f2f56e85f82537c58ea9d3b629f919c74a8d6e3b7e0ed782be008768`  
		Last Modified: Thu, 23 Mar 2017 21:52:16 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.2-alpine`

```console
$ docker pull kapacitor@sha256:02fd3f5049a9314f37dba4d9490740c2e4cef275c0d610fa0fc00d7cc0d86939
```

-	Platforms:
	-	linux; amd64

### `kapacitor:1.2-alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444a7a74ca1d5f7c2e5aaf0d3bcb30c885ecb62f3b4f9b8dad5d07de266c4eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Wed, 12 Apr 2017 18:58:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 12 Apr 2017 19:05:20 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 12 Apr 2017 19:05:36 GMT
ENV KAPACITOR_VERSION=1.2.0
# Wed, 12 Apr 2017 19:05:43 GMT
RUN apk add --no-cache --virtual .build-deps wget gnupg tar &&     gpg --keyserver hkp://ha.pool.sks-keyservers.net         --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 12 Apr 2017 19:05:44 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Wed, 12 Apr 2017 19:05:45 GMT
EXPOSE 9092/tcp
# Wed, 12 Apr 2017 19:05:46 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 12 Apr 2017 19:05:47 GMT
COPY file:440a837280df72a19ed72b91fab9bdcfd268250b241bbc22509699f880fe0d17 in /entrypoint.sh 
# Wed, 12 Apr 2017 19:05:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Apr 2017 19:05:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827570184fa82dc6defc05bcf5838dba590096d8add32bb847191bd7232cfcba`  
		Last Modified: Wed, 12 Apr 2017 19:02:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a07567aee09be1af1aec1476fe3261b0b717c05954d31456c578c63429e532`  
		Last Modified: Wed, 12 Apr 2017 19:06:54 GMT  
		Size: 352.8 KB (352777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628cbe9044eaaf81aec82c9f6850ad571553d6fdfa7385b14ae3ec2af712c93f`  
		Last Modified: Wed, 12 Apr 2017 19:08:47 GMT  
		Size: 7.0 MB (6965173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d790bb33714ae68b1c1a7fd00cdbf2972f9a1d564651f1880a7caf330edfb05`  
		Last Modified: Wed, 12 Apr 2017 19:08:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c519489147d06c28fcd9ac8638eea05d1f062ad041141d81c3fe4f6b946d744`  
		Last Modified: Wed, 12 Apr 2017 19:08:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.2.0-alpine`

```console
$ docker pull kapacitor@sha256:02fd3f5049a9314f37dba4d9490740c2e4cef275c0d610fa0fc00d7cc0d86939
```

-	Platforms:
	-	linux; amd64

### `kapacitor:1.2.0-alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444a7a74ca1d5f7c2e5aaf0d3bcb30c885ecb62f3b4f9b8dad5d07de266c4eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Wed, 12 Apr 2017 18:58:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 12 Apr 2017 19:05:20 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 12 Apr 2017 19:05:36 GMT
ENV KAPACITOR_VERSION=1.2.0
# Wed, 12 Apr 2017 19:05:43 GMT
RUN apk add --no-cache --virtual .build-deps wget gnupg tar &&     gpg --keyserver hkp://ha.pool.sks-keyservers.net         --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 12 Apr 2017 19:05:44 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Wed, 12 Apr 2017 19:05:45 GMT
EXPOSE 9092/tcp
# Wed, 12 Apr 2017 19:05:46 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 12 Apr 2017 19:05:47 GMT
COPY file:440a837280df72a19ed72b91fab9bdcfd268250b241bbc22509699f880fe0d17 in /entrypoint.sh 
# Wed, 12 Apr 2017 19:05:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Apr 2017 19:05:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827570184fa82dc6defc05bcf5838dba590096d8add32bb847191bd7232cfcba`  
		Last Modified: Wed, 12 Apr 2017 19:02:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a07567aee09be1af1aec1476fe3261b0b717c05954d31456c578c63429e532`  
		Last Modified: Wed, 12 Apr 2017 19:06:54 GMT  
		Size: 352.8 KB (352777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628cbe9044eaaf81aec82c9f6850ad571553d6fdfa7385b14ae3ec2af712c93f`  
		Last Modified: Wed, 12 Apr 2017 19:08:47 GMT  
		Size: 7.0 MB (6965173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d790bb33714ae68b1c1a7fd00cdbf2972f9a1d564651f1880a7caf330edfb05`  
		Last Modified: Wed, 12 Apr 2017 19:08:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c519489147d06c28fcd9ac8638eea05d1f062ad041141d81c3fe4f6b946d744`  
		Last Modified: Wed, 12 Apr 2017 19:08:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:02fd3f5049a9314f37dba4d9490740c2e4cef275c0d610fa0fc00d7cc0d86939
```

-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444a7a74ca1d5f7c2e5aaf0d3bcb30c885ecb62f3b4f9b8dad5d07de266c4eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Wed, 12 Apr 2017 18:58:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 12 Apr 2017 19:05:20 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 12 Apr 2017 19:05:36 GMT
ENV KAPACITOR_VERSION=1.2.0
# Wed, 12 Apr 2017 19:05:43 GMT
RUN apk add --no-cache --virtual .build-deps wget gnupg tar &&     gpg --keyserver hkp://ha.pool.sks-keyservers.net         --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 12 Apr 2017 19:05:44 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Wed, 12 Apr 2017 19:05:45 GMT
EXPOSE 9092/tcp
# Wed, 12 Apr 2017 19:05:46 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 12 Apr 2017 19:05:47 GMT
COPY file:440a837280df72a19ed72b91fab9bdcfd268250b241bbc22509699f880fe0d17 in /entrypoint.sh 
# Wed, 12 Apr 2017 19:05:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Apr 2017 19:05:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827570184fa82dc6defc05bcf5838dba590096d8add32bb847191bd7232cfcba`  
		Last Modified: Wed, 12 Apr 2017 19:02:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a07567aee09be1af1aec1476fe3261b0b717c05954d31456c578c63429e532`  
		Last Modified: Wed, 12 Apr 2017 19:06:54 GMT  
		Size: 352.8 KB (352777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628cbe9044eaaf81aec82c9f6850ad571553d6fdfa7385b14ae3ec2af712c93f`  
		Last Modified: Wed, 12 Apr 2017 19:08:47 GMT  
		Size: 7.0 MB (6965173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d790bb33714ae68b1c1a7fd00cdbf2972f9a1d564651f1880a7caf330edfb05`  
		Last Modified: Wed, 12 Apr 2017 19:08:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c519489147d06c28fcd9ac8638eea05d1f062ad041141d81c3fe4f6b946d744`  
		Last Modified: Wed, 12 Apr 2017 19:08:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
