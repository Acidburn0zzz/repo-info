## `groovy:jdk9`

```console
$ docker pull groovy@sha256:c476ba42c69cc3ed325c09db7aa2366345758c754ca2ff3c985ce2b2428b2e91
```

-	Platforms:
	-	linux; amd64

### `groovy:jdk9` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296965728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c28158f507976ed785a69398cb22c71275609069fcf7b7ce8e5445c051025b`
-	Default Command: `["groovysh"]`

```dockerfile
# Mon, 27 Feb 2017 20:36:00 GMT
ADD file:976136a811110184c7ff305b3354fc765d3d21ce0d7ce86eee8900a231e0e38a in / 
# Mon, 27 Feb 2017 20:36:01 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:17:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:18:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 15:25:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 15:25:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Tue, 28 Feb 2017 15:25:51 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 15:25:52 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 28 Feb 2017 15:25:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-9-openjdk-amd64
# Tue, 28 Feb 2017 15:25:53 GMT
ENV JAVA_VERSION=9~b158
# Tue, 28 Feb 2017 15:25:53 GMT
ENV JAVA_DEBIAN_VERSION=9~b158-1
# Tue, 28 Feb 2017 15:26:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 28 Feb 2017 18:28:48 GMT
CMD ["groovysh"]
# Tue, 28 Feb 2017 18:28:48 GMT
WORKDIR /opt
# Tue, 28 Feb 2017 18:28:48 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 28 Feb 2017 18:28:48 GMT
ENV PATH=/opt/groovy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 18:28:49 GMT
ENV GROOVY_VERSION=2.4.8
# Tue, 28 Feb 2017 18:29:14 GMT
RUN set -eu 	&& echo "Downloading Groovy" 	&& wget -nv -O groovy.zip "https://dist.apache.org/repos/dist/release/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip" 		&& echo "Installing build dependencies" 	&& apt-get update 	&& apt-get update && apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	&& rm -r /var/lib/apt/lists/* 		&& echo "Checking download signature" 	&& wget -nv -O groovy.zip.asc "https://dist.apache.org/repos/dist/release/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "0x41321490758AAD6F" "0x825C06C827AF6B66" "0x6A65176A0FB1CD0B" 	&& gpg --batch --verify groovy.zip.asc groovy.zip 	&& rm -rf "${GNUPGHOME}" 	&& rm groovy.zip.asc 		&& echo "Installing Groovy" 	&& unzip groovy.zip 	&& rm groovy.zip 	&& mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}" 		&& echo "Cleaning up build dependencies" 	&& echo $(apt-mark showauto) 	&& apt-get remove -y --purge 		dirmngr 		gnupg 	&& apt-get autoremove -y --purge 		&& groovy --version
```

-	Layers:
	-	`sha256:a40c9d226366db9384aa684e3d34913cdacf75282bdc70dff4ff186e130ee2c3`  
		Last Modified: Mon, 27 Feb 2017 20:44:12 GMT  
		Size: 44.3 MB (44250775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370d333d5093cd32956cf56f9aae4f0b66699bcae00e5dabfd442881776f9ce9`  
		Last Modified: Mon, 27 Feb 2017 21:58:16 GMT  
		Size: 21.1 MB (21146887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05576433df0ed43f1d775c55f43190e4f804b1a2125f0653f3aca0da5dc1b9eb`  
		Last Modified: Mon, 27 Feb 2017 21:58:55 GMT  
		Size: 40.0 MB (40048126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1074fc6a6eb725a42e59a4a152dbcce3c92ddd5b441c6c8dcb891d7a8c3ca7f`  
		Last Modified: Tue, 28 Feb 2017 22:10:27 GMT  
		Size: 651.7 KB (651691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a217b2041ecf93dcad732fcdf5e68fd6491537f89645a44c78738007039cbad`  
		Last Modified: Tue, 28 Feb 2017 22:10:27 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f50c71f32ae033ed06cc00bac252494e71cf49032d4bd8791c0ef172a93d2dd`  
		Last Modified: Tue, 28 Feb 2017 22:10:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24729d22759903a2b87105ec905a3b31064bef26300bb6688b698fd1073c135e`  
		Last Modified: Tue, 28 Feb 2017 22:11:03 GMT  
		Size: 154.3 MB (154348400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83985ad74dbfbd1bbe672962c56ca74c9901ec52a619b3ea92dcf6953460aa1`  
		Last Modified: Tue, 28 Feb 2017 22:10:34 GMT  
		Size: 36.5 MB (36519396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip