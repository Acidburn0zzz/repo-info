## `haproxy:latest`

```console
$ docker pull haproxy@sha256:24266f42f90f12565de7e5f54535f5a910d01906261aa1c782638e7b5ac8e29f
```

-	Platforms:
	-	linux; amd64

### `haproxy:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56356935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa0a1d3cadacd0beb89221178c1ce73e274dcde2b512ed699f1a9e83e2e4191`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 18:29:42 GMT
RUN awk '$1 ~ "^deb" { $3 = $3 "-backports"; print; exit }' /etc/apt/sources.list > /etc/apt/sources.list.d/backports.list
# Tue, 21 Mar 2017 20:37:09 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		liblua5.3-0 		libpcre3 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:37:09 GMT
ENV HAPROXY_MAJOR=1.7
# Mon, 03 Apr 2017 19:06:52 GMT
ENV HAPROXY_VERSION=1.7.5
# Mon, 03 Apr 2017 19:06:52 GMT
ENV HAPROXY_MD5=ed84c80cb97852d2aa3161ed16c48a1c
# Mon, 03 Apr 2017 19:08:30 GMT
RUN set -x 		&& buildDeps=' 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre3-dev 		libssl-dev 		make 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O haproxy.tar.gz "http://www.haproxy.org/download/${HAPROXY_MAJOR}/src/haproxy-${HAPROXY_VERSION}.tar.gz" 	&& echo "$HAPROXY_MD5 *haproxy.tar.gz" | md5sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE=1 PCREDIR= 		USE_ZLIB=1 	' 	&& make -C /usr/src/haproxy -j "$(nproc)" all $makeOpts 	&& make -C /usr/src/haproxy install-bin $makeOpts 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& apt-get purge -y --auto-remove $buildDeps
# Mon, 03 Apr 2017 19:08:31 GMT
COPY file:b1cb7b827dc9fcd27909f9c233ac2faa2d7534c25992fa5f3402d22503666d6d in / 
# Mon, 03 Apr 2017 19:08:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Apr 2017 19:08:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40da44b9cf65c4d0abb9ac001635a4f403b998afc222553452635bba9b4e2f9`  
		Last Modified: Tue, 21 Mar 2017 18:41:23 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b1fddea0c6f2b67c92740400fc04cc1f920b5a9693faf0f29b0a7bac4bcd88`  
		Last Modified: Thu, 23 Mar 2017 18:26:43 GMT  
		Size: 2.0 MB (1973734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb22d2f6886055d897aaa4655a88bb173d3306fb3185d50a59cbfae9e8f8d4d1`  
		Last Modified: Mon, 03 Apr 2017 19:14:24 GMT  
		Size: 2.9 MB (2944166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99613a28a85ca04593949138c3d50f8525041baeb1f641207a42d6b78c68b07f`  
		Last Modified: Mon, 03 Apr 2017 19:14:23 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
