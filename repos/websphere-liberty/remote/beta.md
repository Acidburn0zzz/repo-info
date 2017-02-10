## `websphere-liberty:beta`

```console
$ docker pull websphere-liberty@sha256:46c63130e81dcb6dcb881325e560d2eab26fce0a40d9cc71432cb4c39bd10068
```

-	Platforms:
	-	linux; amd64

### `websphere-liberty:beta` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239801129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc03452a7420f0a49f080ef00aa64f7a55549dfa5aaffeb5f6918752b9e1c3b7`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 20 Jan 2017 21:43:23 GMT
ADD file:68f83d996c38a09c0ffbfd8b5b49c87fd39ec085992a00de3a27a820eb5d9383 in / 
# Fri, 20 Jan 2017 21:43:38 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Jan 2017 21:43:40 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 20 Jan 2017 21:43:54 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Fri, 20 Jan 2017 21:43:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Jan 2017 21:44:07 GMT
CMD ["/bin/bash"]
# Sat, 21 Jan 2017 00:31:26 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Sat, 21 Jan 2017 00:31:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Sat, 21 Jan 2017 00:31:40 GMT
ENV JAVA_VERSION=1.8.0_sr3fp22
# Sat, 21 Jan 2017 00:32:20 GMT
RUN ESUM="ec96d978612fd3981bae382a745669544280cdd7eaaa55fadfbd7a26aa447b25"     && BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/"     && YML_FILE="jre/linux/x86_64/index.yml"     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml $BASE_URL/$YML_FILE     && JAVA_URL=$(cat /tmp/index.yml | sed -n '/'$JAVA_VERSION'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r')     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin $JAVA_URL     && echo "$ESUM  /tmp/ibm-java.bin" | sha256sum -c -     && echo "INSTALLER_UI=silent" > /tmp/response.properties     && echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties     && echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties     && mkdir -p /opt/ibm     && chmod +x /tmp/ibm-java.bin     && /tmp/ibm-java.bin -i silent -f /tmp/response.properties     && rm -f /tmp/response.properties     && rm -f /tmp/index.yml     && rm -f /tmp/ibm-java.bin
# Sat, 21 Jan 2017 00:32:20 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Jan 2017 02:09:12 GMT
MAINTAINER David Currie <david_currie@uk.ibm.com> (@dcurrie)
# Sat, 21 Jan 2017 02:09:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Jan 2017 18:36:49 GMT
ENV LIBERTY_VERSION=2017.1.0_0
# Mon, 23 Jan 2017 18:37:04 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip
# Mon, 23 Jan 2017 18:37:05 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jan 2017 18:37:05 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Mon, 23 Jan 2017 18:37:06 GMT
RUN mkdir /logs     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config
# Mon, 23 Jan 2017 18:37:10 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 23 Jan 2017 18:37:11 GMT
COPY file:889efe2fa762acb1292377f98c0f0fb54c169e3f4bbab602322ba3b63ff3b3ca in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Mon, 23 Jan 2017 18:37:12 GMT
EXPOSE 9080/tcp 9443/tcp
# Mon, 23 Jan 2017 18:37:12 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:8aec416115fdbd74102c9090bcfe03bfe8926876642d8846c8b917959ea9b552`  
		Last Modified: Fri, 20 Jan 2017 21:50:34 GMT  
		Size: 50.3 MB (50308178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695f074e24e392178d364af5ea2405dda7ab0035284001b49939afac5106c187`  
		Last Modified: Fri, 20 Jan 2017 21:50:19 GMT  
		Size: 820.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946d6c48c2a7d60cb2f4d1c4d3a8131086b412d11a9def59d0bcc0892428dde9`  
		Last Modified: Fri, 20 Jan 2017 21:50:19 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7277e579f03a13476b4d2dc6607124f7e67341dbd58f9d1cd6555bec086c04`  
		Last Modified: Fri, 20 Jan 2017 21:50:19 GMT  
		Size: 680.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2508cbcde94b50cd53356e8730bb508ddb43c76664a35dc29e69bb8b56a0f531`  
		Last Modified: Fri, 20 Jan 2017 21:50:19 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7bfb3f7b2880a0cb349f17978b056d4c4c0a75d6ddf008d014074681e7fc16`  
		Last Modified: Sat, 21 Jan 2017 00:33:59 GMT  
		Size: 3.1 MB (3078063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f4a7cad0d65d61ed00b6cf3057598d35363956162abf16c4cca88b1573172`  
		Last Modified: Sat, 21 Jan 2017 00:34:10 GMT  
		Size: 110.3 MB (110252944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954fd32941334b0235d86e742ba58963d2661b370d99775ecb1bf1d7490f3bf4`  
		Last Modified: Sat, 21 Jan 2017 02:14:33 GMT  
		Size: 266.3 KB (266288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2967eb4fc0b251b8fea0593b62ecc20ed129d77e85f369d99bb05bf5d62f30ea`  
		Last Modified: Mon, 23 Jan 2017 18:39:13 GMT  
		Size: 75.9 MB (75891187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2cf7442f77e6bf4dab10aba38fdc7999717d73a530b220d55ffecad7d4af2d`  
		Last Modified: Mon, 23 Jan 2017 18:39:05 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffed8e30c6711aa16e7fa7505cb99c81868a82b27a7321410214186adf82d203`  
		Last Modified: Mon, 23 Jan 2017 18:39:05 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388b91de3d6113920a07240f4ddea77d0d618ff2b97c301783a95d9d7f7fafb3`  
		Last Modified: Mon, 23 Jan 2017 18:39:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
