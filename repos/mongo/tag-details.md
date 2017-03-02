<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo`

-	[`mongo:3.0.14`](#mongo3014)
-	[`mongo:3.0`](#mongo30)
-	[`mongo:3.0.14-windowsservercore`](#mongo3014-windowsservercore)
-	[`mongo:3.0-windowsservercore`](#mongo30-windowsservercore)
-	[`mongo:3.2.12`](#mongo3212)
-	[`mongo:3.2`](#mongo32)
-	[`mongo:3.2.12-windowsservercore`](#mongo3212-windowsservercore)
-	[`mongo:3.2-windowsservercore`](#mongo32-windowsservercore)
-	[`mongo:3.4.2`](#mongo342)
-	[`mongo:3.4`](#mongo34)
-	[`mongo:3`](#mongo3)
-	[`mongo:latest`](#mongolatest)
-	[`mongo:3.4.2-windowsservercore`](#mongo342-windowsservercore)
-	[`mongo:3.4-windowsservercore`](#mongo34-windowsservercore)
-	[`mongo:3-windowsservercore`](#mongo3-windowsservercore)
-	[`mongo:windowsservercore`](#mongowindowsservercore)

## `mongo:3.0.14`

```console
$ docker pull mongo@sha256:af50b7f4ab823382f8eb66068727a184c61e3251932c2a807267b49933756d6c
```

-	Platforms:
	-	linux; amd64

### `mongo:3.0.14` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101041729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134dce136e2efa9dfe888d6b8c381185251ca92a0646a5da10d796f7c83398bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Feb 2017 20:39:24 GMT
ADD file:ddbcd17149470ca923569d3112a7955f842a00bf8eee92781c6eb13af64b5b82 in / 
# Mon, 27 Feb 2017 20:39:25 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 06:04:47 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 28 Feb 2017 06:04:52 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 06:05:10 GMT
ENV GOSU_VERSION=1.7
# Tue, 28 Feb 2017 06:05:32 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 28 Feb 2017 06:05:32 GMT
ENV GPG_KEYS=492EAFE8CD016A07919F1D2B9ECBEC467F0CEB10
# Tue, 28 Feb 2017 06:05:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 28 Feb 2017 06:05:34 GMT
ENV MONGO_MAJOR=3.0
# Tue, 28 Feb 2017 06:05:34 GMT
ENV MONGO_VERSION=3.0.14
# Tue, 28 Feb 2017 06:05:35 GMT
ENV MONGO_PACKAGE=mongodb-org
# Tue, 28 Feb 2017 06:05:36 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian wheezy/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Tue, 28 Feb 2017 06:05:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 28 Feb 2017 06:06:00 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 28 Feb 2017 06:06:00 GMT
VOLUME [/data/db /data/configdb]
# Tue, 28 Feb 2017 06:06:01 GMT
COPY file:31c99192d9c1648c6f48dc5557de182c76080376f32685657130407fda705b3b in /entrypoint.sh 
# Tue, 28 Feb 2017 06:06:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Feb 2017 06:06:02 GMT
EXPOSE 27017/tcp
# Tue, 28 Feb 2017 06:06:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c3e97b7a4c20461eb05807e795f449cc8826084be5e3c4766fa9cc49b4df3551`  
		Last Modified: Mon, 27 Feb 2017 20:50:15 GMT  
		Size: 37.3 MB (37284709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5008d27fc0377788ddcaa66ec073a180f671d2e423330dbe6ef3c462671700c3`  
		Last Modified: Thu, 02 Mar 2017 01:27:41 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977b0bd68dcda77d12ecd069376d05480ab0f6ffbbe27d60311c7af38670b78f`  
		Last Modified: Thu, 02 Mar 2017 01:27:41 GMT  
		Size: 146.5 KB (146490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4206759036ede340ef3fcdb8f9261b4a98f0fa29cc7b20b10973daf25a15005e`  
		Last Modified: Thu, 02 Mar 2017 01:27:40 GMT  
		Size: 1.2 MB (1245876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f1d8358c4f618e5c74e32ce896b9488864ba3ac699a8ad10a37ecabd787fdd`  
		Last Modified: Thu, 02 Mar 2017 01:27:38 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f39d522b3e794c5a2c9f4f030ccaab17c6592b7a2ae01886bbededca6c39776`  
		Last Modified: Thu, 02 Mar 2017 01:27:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964698b1aade11795ffc97f975eb2953ea0018728361dea1a7604c9525ae391a`  
		Last Modified: Thu, 02 Mar 2017 01:28:02 GMT  
		Size: 62.4 MB (62360100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db724fba041399b94de8a00796f8f164786f1f841f9278ba9e0f74e5e8e9babe`  
		Last Modified: Thu, 02 Mar 2017 01:27:37 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442e54945fdb95df1dd3e1f549e533d47d18df594867e8235397bea652975ab9`  
		Last Modified: Thu, 02 Mar 2017 01:27:38 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.0`

```console
$ docker pull mongo@sha256:af50b7f4ab823382f8eb66068727a184c61e3251932c2a807267b49933756d6c
```

-	Platforms:
	-	linux; amd64

### `mongo:3.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101041729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134dce136e2efa9dfe888d6b8c381185251ca92a0646a5da10d796f7c83398bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Feb 2017 20:39:24 GMT
ADD file:ddbcd17149470ca923569d3112a7955f842a00bf8eee92781c6eb13af64b5b82 in / 
# Mon, 27 Feb 2017 20:39:25 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 06:04:47 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 28 Feb 2017 06:04:52 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 06:05:10 GMT
ENV GOSU_VERSION=1.7
# Tue, 28 Feb 2017 06:05:32 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 28 Feb 2017 06:05:32 GMT
ENV GPG_KEYS=492EAFE8CD016A07919F1D2B9ECBEC467F0CEB10
# Tue, 28 Feb 2017 06:05:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 28 Feb 2017 06:05:34 GMT
ENV MONGO_MAJOR=3.0
# Tue, 28 Feb 2017 06:05:34 GMT
ENV MONGO_VERSION=3.0.14
# Tue, 28 Feb 2017 06:05:35 GMT
ENV MONGO_PACKAGE=mongodb-org
# Tue, 28 Feb 2017 06:05:36 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian wheezy/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Tue, 28 Feb 2017 06:05:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 28 Feb 2017 06:06:00 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 28 Feb 2017 06:06:00 GMT
VOLUME [/data/db /data/configdb]
# Tue, 28 Feb 2017 06:06:01 GMT
COPY file:31c99192d9c1648c6f48dc5557de182c76080376f32685657130407fda705b3b in /entrypoint.sh 
# Tue, 28 Feb 2017 06:06:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Feb 2017 06:06:02 GMT
EXPOSE 27017/tcp
# Tue, 28 Feb 2017 06:06:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c3e97b7a4c20461eb05807e795f449cc8826084be5e3c4766fa9cc49b4df3551`  
		Last Modified: Mon, 27 Feb 2017 20:50:15 GMT  
		Size: 37.3 MB (37284709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5008d27fc0377788ddcaa66ec073a180f671d2e423330dbe6ef3c462671700c3`  
		Last Modified: Thu, 02 Mar 2017 01:27:41 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977b0bd68dcda77d12ecd069376d05480ab0f6ffbbe27d60311c7af38670b78f`  
		Last Modified: Thu, 02 Mar 2017 01:27:41 GMT  
		Size: 146.5 KB (146490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4206759036ede340ef3fcdb8f9261b4a98f0fa29cc7b20b10973daf25a15005e`  
		Last Modified: Thu, 02 Mar 2017 01:27:40 GMT  
		Size: 1.2 MB (1245876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f1d8358c4f618e5c74e32ce896b9488864ba3ac699a8ad10a37ecabd787fdd`  
		Last Modified: Thu, 02 Mar 2017 01:27:38 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f39d522b3e794c5a2c9f4f030ccaab17c6592b7a2ae01886bbededca6c39776`  
		Last Modified: Thu, 02 Mar 2017 01:27:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964698b1aade11795ffc97f975eb2953ea0018728361dea1a7604c9525ae391a`  
		Last Modified: Thu, 02 Mar 2017 01:28:02 GMT  
		Size: 62.4 MB (62360100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db724fba041399b94de8a00796f8f164786f1f841f9278ba9e0f74e5e8e9babe`  
		Last Modified: Thu, 02 Mar 2017 01:27:37 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442e54945fdb95df1dd3e1f549e533d47d18df594867e8235397bea652975ab9`  
		Last Modified: Thu, 02 Mar 2017 01:27:38 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.0.14-windowsservercore`

```console
$ docker pull mongo@sha256:df73e9d0c559923a2030d6abd7c594533eca66e0bc0719e39e5a9a70a4a51725
```

-	Platforms:
	-	windows; amd64

### `mongo:3.0.14-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 GB (5029884495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4606a0a76ea86f59076239b287c8b2985dd04fbee6741da586097cb39c45baba`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 20 Jan 2017 21:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 01 Feb 2017 19:34:52 GMT
ENV MONGO_VERSION=3.0.14
# Wed, 01 Feb 2017 19:34:55 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.0.14-signed.msi
# Wed, 01 Feb 2017 19:34:59 GMT
ENV MONGO_DOWNLOAD_SHA256=5a081722c42c79f23d9201c97500be6ddc8741b66ce707d88dad058bf84165f1
# Wed, 01 Feb 2017 19:36:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 01 Feb 2017 19:36:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 01 Feb 2017 19:36:37 GMT
EXPOSE 27017/tcp
# Wed, 01 Feb 2017 19:36:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3430754e4d171ead00cf6766797a28abf3caf236f6c92c5c346ea2ad3955a129`  
		Size: 913.1 MB (913145061 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d9d048a108290b40b03a1a415360fe78a4038bfb48be71f6a1e05e92092624`  
		Last Modified: Fri, 20 Jan 2017 22:10:22 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21493703e68eb511ab660b4dfe2431032a7781b1a9a8162b84b74b7ab6515d2b`  
		Last Modified: Wed, 01 Feb 2017 19:39:52 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d31d33b3157ecfbb8c5970dbe37cfb648d0863bba82ba558521b79f65196734`  
		Last Modified: Wed, 01 Feb 2017 19:39:52 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a09d687b6001ff1fe64e8e142aec05215de44db454385bf18653182e5e985b4`  
		Last Modified: Wed, 01 Feb 2017 19:39:45 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6220cc336a9f51640133f7b3c89811a6b19ab1016ff7861cde5b00d6c5682ed1`  
		Last Modified: Wed, 01 Feb 2017 19:39:53 GMT  
		Size: 46.7 MB (46745005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b9027e210807d0156126a62098495c3e2a1accd08a1332bc997764a477250c`  
		Last Modified: Wed, 01 Feb 2017 19:39:43 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41996cdc4228fb8610c89abb3e40b10e873833e3dfc975b5203f21cf5ddd2b41`  
		Last Modified: Wed, 01 Feb 2017 19:39:43 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f1ad10ba5ea30a8e6657101b96984e3db3dc8a4896bb040d0f0703236944aa`  
		Last Modified: Wed, 01 Feb 2017 19:39:43 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.0-windowsservercore`

```console
$ docker pull mongo@sha256:df73e9d0c559923a2030d6abd7c594533eca66e0bc0719e39e5a9a70a4a51725
```

-	Platforms:
	-	windows; amd64

### `mongo:3.0-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 GB (5029884495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4606a0a76ea86f59076239b287c8b2985dd04fbee6741da586097cb39c45baba`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 20 Jan 2017 21:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 01 Feb 2017 19:34:52 GMT
ENV MONGO_VERSION=3.0.14
# Wed, 01 Feb 2017 19:34:55 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.0.14-signed.msi
# Wed, 01 Feb 2017 19:34:59 GMT
ENV MONGO_DOWNLOAD_SHA256=5a081722c42c79f23d9201c97500be6ddc8741b66ce707d88dad058bf84165f1
# Wed, 01 Feb 2017 19:36:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 01 Feb 2017 19:36:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 01 Feb 2017 19:36:37 GMT
EXPOSE 27017/tcp
# Wed, 01 Feb 2017 19:36:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3430754e4d171ead00cf6766797a28abf3caf236f6c92c5c346ea2ad3955a129`  
		Size: 913.1 MB (913145061 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d9d048a108290b40b03a1a415360fe78a4038bfb48be71f6a1e05e92092624`  
		Last Modified: Fri, 20 Jan 2017 22:10:22 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21493703e68eb511ab660b4dfe2431032a7781b1a9a8162b84b74b7ab6515d2b`  
		Last Modified: Wed, 01 Feb 2017 19:39:52 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d31d33b3157ecfbb8c5970dbe37cfb648d0863bba82ba558521b79f65196734`  
		Last Modified: Wed, 01 Feb 2017 19:39:52 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a09d687b6001ff1fe64e8e142aec05215de44db454385bf18653182e5e985b4`  
		Last Modified: Wed, 01 Feb 2017 19:39:45 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6220cc336a9f51640133f7b3c89811a6b19ab1016ff7861cde5b00d6c5682ed1`  
		Last Modified: Wed, 01 Feb 2017 19:39:53 GMT  
		Size: 46.7 MB (46745005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b9027e210807d0156126a62098495c3e2a1accd08a1332bc997764a477250c`  
		Last Modified: Wed, 01 Feb 2017 19:39:43 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41996cdc4228fb8610c89abb3e40b10e873833e3dfc975b5203f21cf5ddd2b41`  
		Last Modified: Wed, 01 Feb 2017 19:39:43 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f1ad10ba5ea30a8e6657101b96984e3db3dc8a4896bb040d0f0703236944aa`  
		Last Modified: Wed, 01 Feb 2017 19:39:43 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2.12`

```console
$ docker pull mongo@sha256:47d11ca2e0e2d4fec3fdca1d96c8934cc2150b4e49463ef8c4a115db81242545
```

-	Platforms:
	-	linux; amd64

### `mongo:3.2.12` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123550861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf21c7fe12fd2586f6220b0e8648a8e826f548a74da51627d0b3ffc9e97a5145`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 06:02:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 28 Feb 2017 06:02:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 06:02:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 28 Feb 2017 06:03:31 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 28 Feb 2017 06:06:03 GMT
ENV GPG_KEYS=DFFA3DCF326E302C4787673A01C4E7FAAAB2461C 	42F3E95A2C4F08279C4960ADD68FA50FEA312927
# Tue, 28 Feb 2017 06:06:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 28 Feb 2017 06:06:22 GMT
ENV MONGO_MAJOR=3.2
# Tue, 28 Feb 2017 06:06:22 GMT
ENV MONGO_VERSION=3.2.12
# Tue, 28 Feb 2017 06:06:22 GMT
ENV MONGO_PACKAGE=mongodb-org
# Tue, 28 Feb 2017 06:06:23 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian jessie/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Tue, 28 Feb 2017 06:06:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 28 Feb 2017 06:06:53 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 28 Feb 2017 06:06:53 GMT
VOLUME [/data/db /data/configdb]
# Tue, 28 Feb 2017 06:07:09 GMT
COPY file:31c99192d9c1648c6f48dc5557de182c76080376f32685657130407fda705b3b in /entrypoint.sh 
# Tue, 28 Feb 2017 06:07:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Feb 2017 06:07:10 GMT
EXPOSE 27017/tcp
# Tue, 28 Feb 2017 06:07:10 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a29f630b22ecb9060e541038d275645574312de47421df2f8031621acb25d2f`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328ac2c79d69324cb76eb09114330606aaadbe073e6f6409e7cb131bcf287e5e`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 134.4 KB (134448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d628f74e0e9702828e26ab68da68fefaf2fe69942556c90360c55c057b82fdc6`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 1.2 MB (1217784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972791822007ac3a89ad6013f144e1d92828c04064e06aa7e71e95519b5e8cb1`  
		Last Modified: Thu, 02 Mar 2017 01:28:44 GMT  
		Size: 3.1 KB (3067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd209b3e4b4e5e4c34dcd550ce5e96bfa45d0968155e54beb428bd588d4e43a`  
		Last Modified: Thu, 02 Mar 2017 01:28:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef30c45a832ac634d3bde725c16941708214df654683545b19e65dfc1c11d9e`  
		Last Modified: Thu, 02 Mar 2017 01:29:09 GMT  
		Size: 70.8 MB (70829273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7882b56fb2dc29955e9e142af9390797a826ef41d97ee77302f38744838449aa`  
		Last Modified: Thu, 02 Mar 2017 01:28:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b0f679b7aa902ef9a3b4cfd20c9170bba02715325b81b4e77d99d6508154ac`  
		Last Modified: Thu, 02 Mar 2017 01:28:44 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2`

```console
$ docker pull mongo@sha256:47d11ca2e0e2d4fec3fdca1d96c8934cc2150b4e49463ef8c4a115db81242545
```

-	Platforms:
	-	linux; amd64

### `mongo:3.2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123550861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf21c7fe12fd2586f6220b0e8648a8e826f548a74da51627d0b3ffc9e97a5145`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 06:02:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 28 Feb 2017 06:02:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 06:02:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 28 Feb 2017 06:03:31 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 28 Feb 2017 06:06:03 GMT
ENV GPG_KEYS=DFFA3DCF326E302C4787673A01C4E7FAAAB2461C 	42F3E95A2C4F08279C4960ADD68FA50FEA312927
# Tue, 28 Feb 2017 06:06:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 28 Feb 2017 06:06:22 GMT
ENV MONGO_MAJOR=3.2
# Tue, 28 Feb 2017 06:06:22 GMT
ENV MONGO_VERSION=3.2.12
# Tue, 28 Feb 2017 06:06:22 GMT
ENV MONGO_PACKAGE=mongodb-org
# Tue, 28 Feb 2017 06:06:23 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian jessie/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Tue, 28 Feb 2017 06:06:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 28 Feb 2017 06:06:53 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 28 Feb 2017 06:06:53 GMT
VOLUME [/data/db /data/configdb]
# Tue, 28 Feb 2017 06:07:09 GMT
COPY file:31c99192d9c1648c6f48dc5557de182c76080376f32685657130407fda705b3b in /entrypoint.sh 
# Tue, 28 Feb 2017 06:07:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Feb 2017 06:07:10 GMT
EXPOSE 27017/tcp
# Tue, 28 Feb 2017 06:07:10 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a29f630b22ecb9060e541038d275645574312de47421df2f8031621acb25d2f`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328ac2c79d69324cb76eb09114330606aaadbe073e6f6409e7cb131bcf287e5e`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 134.4 KB (134448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d628f74e0e9702828e26ab68da68fefaf2fe69942556c90360c55c057b82fdc6`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 1.2 MB (1217784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972791822007ac3a89ad6013f144e1d92828c04064e06aa7e71e95519b5e8cb1`  
		Last Modified: Thu, 02 Mar 2017 01:28:44 GMT  
		Size: 3.1 KB (3067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd209b3e4b4e5e4c34dcd550ce5e96bfa45d0968155e54beb428bd588d4e43a`  
		Last Modified: Thu, 02 Mar 2017 01:28:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef30c45a832ac634d3bde725c16941708214df654683545b19e65dfc1c11d9e`  
		Last Modified: Thu, 02 Mar 2017 01:29:09 GMT  
		Size: 70.8 MB (70829273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7882b56fb2dc29955e9e142af9390797a826ef41d97ee77302f38744838449aa`  
		Last Modified: Thu, 02 Mar 2017 01:28:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b0f679b7aa902ef9a3b4cfd20c9170bba02715325b81b4e77d99d6508154ac`  
		Last Modified: Thu, 02 Mar 2017 01:28:44 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2.12-windowsservercore`

```console
$ docker pull mongo@sha256:fe8c68819c15e26f6f3a628a608eefd11d115fc471a08227011c9fd8db15a572
```

-	Platforms:
	-	windows; amd64

### `mongo:3.2.12-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 GB (5040300320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f7991a11ceb588523f050060a51011110ffb3a35d442a67d572c5460c4f0b1`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 20 Jan 2017 21:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 01 Feb 2017 19:36:46 GMT
ENV MONGO_VERSION=3.2.12
# Wed, 01 Feb 2017 19:36:49 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.2.12-signed.msi
# Wed, 01 Feb 2017 19:36:53 GMT
ENV MONGO_DOWNLOAD_SHA256=9b8312e067c076808b6c8fd91e327b13caa0286ae21c1221cf29076ad110b116
# Wed, 01 Feb 2017 19:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 01 Feb 2017 19:37:53 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 01 Feb 2017 19:37:58 GMT
EXPOSE 27017/tcp
# Wed, 01 Feb 2017 19:38:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3430754e4d171ead00cf6766797a28abf3caf236f6c92c5c346ea2ad3955a129`  
		Size: 913.1 MB (913145061 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d9d048a108290b40b03a1a415360fe78a4038bfb48be71f6a1e05e92092624`  
		Last Modified: Fri, 20 Jan 2017 22:10:22 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac9ce96d25e022b03036646d272993aae859b5266a54ea827d454e840abc6c8`  
		Last Modified: Wed, 01 Feb 2017 19:40:15 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8f9c8d4637660ff7ff31dad0927cf8c867f30ccb8d5117e39cae94a6a48b4`  
		Last Modified: Wed, 01 Feb 2017 19:40:15 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae4ea3da5ff34f3f3c85de1d8dae17827be663af7085b5562a31675f9f6e6cc`  
		Last Modified: Wed, 01 Feb 2017 19:40:07 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e4814c0513dc2bd42e3e3712d6c60518e38e6099e40049df536c602492c040`  
		Last Modified: Wed, 01 Feb 2017 19:40:19 GMT  
		Size: 57.2 MB (57160798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738be2717156fa1a1d576a42a8ebfc1b1785cb7144b8ec1efe382dad0ad571c`  
		Last Modified: Wed, 01 Feb 2017 19:40:07 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa53397516cdd625e308057ebea682074269d43a7dad8d217d53a5e30119617`  
		Last Modified: Wed, 01 Feb 2017 19:40:07 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb2d266914b97af00046c4b9f0f93be2ef153f5802123e4a812887cec4020de`  
		Last Modified: Wed, 01 Feb 2017 19:40:06 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2-windowsservercore`

```console
$ docker pull mongo@sha256:fe8c68819c15e26f6f3a628a608eefd11d115fc471a08227011c9fd8db15a572
```

-	Platforms:
	-	windows; amd64

### `mongo:3.2-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 GB (5040300320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f7991a11ceb588523f050060a51011110ffb3a35d442a67d572c5460c4f0b1`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 20 Jan 2017 21:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 01 Feb 2017 19:36:46 GMT
ENV MONGO_VERSION=3.2.12
# Wed, 01 Feb 2017 19:36:49 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.2.12-signed.msi
# Wed, 01 Feb 2017 19:36:53 GMT
ENV MONGO_DOWNLOAD_SHA256=9b8312e067c076808b6c8fd91e327b13caa0286ae21c1221cf29076ad110b116
# Wed, 01 Feb 2017 19:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 01 Feb 2017 19:37:53 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 01 Feb 2017 19:37:58 GMT
EXPOSE 27017/tcp
# Wed, 01 Feb 2017 19:38:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3430754e4d171ead00cf6766797a28abf3caf236f6c92c5c346ea2ad3955a129`  
		Size: 913.1 MB (913145061 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d9d048a108290b40b03a1a415360fe78a4038bfb48be71f6a1e05e92092624`  
		Last Modified: Fri, 20 Jan 2017 22:10:22 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac9ce96d25e022b03036646d272993aae859b5266a54ea827d454e840abc6c8`  
		Last Modified: Wed, 01 Feb 2017 19:40:15 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e8f9c8d4637660ff7ff31dad0927cf8c867f30ccb8d5117e39cae94a6a48b4`  
		Last Modified: Wed, 01 Feb 2017 19:40:15 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae4ea3da5ff34f3f3c85de1d8dae17827be663af7085b5562a31675f9f6e6cc`  
		Last Modified: Wed, 01 Feb 2017 19:40:07 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e4814c0513dc2bd42e3e3712d6c60518e38e6099e40049df536c602492c040`  
		Last Modified: Wed, 01 Feb 2017 19:40:19 GMT  
		Size: 57.2 MB (57160798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738be2717156fa1a1d576a42a8ebfc1b1785cb7144b8ec1efe382dad0ad571c`  
		Last Modified: Wed, 01 Feb 2017 19:40:07 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa53397516cdd625e308057ebea682074269d43a7dad8d217d53a5e30119617`  
		Last Modified: Wed, 01 Feb 2017 19:40:07 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb2d266914b97af00046c4b9f0f93be2ef153f5802123e4a812887cec4020de`  
		Last Modified: Wed, 01 Feb 2017 19:40:06 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4.2`

```console
$ docker pull mongo@sha256:3d4537f996bc28a6c6b694e22f46316c0629703420de60e8f46285ce1fe69260
```

-	Platforms:
	-	linux; amd64

### `mongo:3.4.2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150420569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686238c7a975c9dcb154be65a2ea761b79e4401990860ab11549281e92f2e442`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 06:02:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 28 Feb 2017 06:02:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 06:02:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 28 Feb 2017 06:03:31 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 28 Feb 2017 06:03:31 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Tue, 28 Feb 2017 06:03:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 28 Feb 2017 06:03:33 GMT
ENV MONGO_MAJOR=3.4
# Tue, 28 Feb 2017 06:03:33 GMT
ENV MONGO_VERSION=3.4.2
# Tue, 28 Feb 2017 06:03:34 GMT
ENV MONGO_PACKAGE=mongodb-org
# Tue, 28 Feb 2017 06:03:35 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian jessie/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Tue, 28 Feb 2017 06:04:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 28 Feb 2017 06:04:42 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 28 Feb 2017 06:04:43 GMT
VOLUME [/data/db /data/configdb]
# Tue, 28 Feb 2017 06:04:44 GMT
COPY file:31c99192d9c1648c6f48dc5557de182c76080376f32685657130407fda705b3b in /entrypoint.sh 
# Tue, 28 Feb 2017 06:04:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Feb 2017 06:04:45 GMT
EXPOSE 27017/tcp
# Tue, 28 Feb 2017 06:04:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a29f630b22ecb9060e541038d275645574312de47421df2f8031621acb25d2f`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328ac2c79d69324cb76eb09114330606aaadbe073e6f6409e7cb131bcf287e5e`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 134.4 KB (134448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d628f74e0e9702828e26ab68da68fefaf2fe69942556c90360c55c057b82fdc6`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 1.2 MB (1217784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50753de132e0a3f79a598d92b47f33832a3915da40ff5636633b59e7c0b2e1f7`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fee098631ba283944156b1743f8eec8fb695c8e4fe2758fca9ef631badbff0`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4c3bdc152539bddccffa8c1ac1f4aae8333eaecf265d539fe2cca0e4fb8b95`  
		Last Modified: Thu, 02 Mar 2017 01:30:19 GMT  
		Size: 97.7 MB (97700620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0970b86ae43a0dbed0174ea6ff638ec1f8073308a14ceb2af0cc2c4a180da`  
		Last Modified: Thu, 02 Mar 2017 01:29:49 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fbca93d3445d1b12330b3ea1b965aa0fd80383d67a0ccd682c035f99c545b2`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4`

```console
$ docker pull mongo@sha256:3d4537f996bc28a6c6b694e22f46316c0629703420de60e8f46285ce1fe69260
```

-	Platforms:
	-	linux; amd64

### `mongo:3.4` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150420569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686238c7a975c9dcb154be65a2ea761b79e4401990860ab11549281e92f2e442`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 06:02:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 28 Feb 2017 06:02:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 06:02:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 28 Feb 2017 06:03:31 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 28 Feb 2017 06:03:31 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Tue, 28 Feb 2017 06:03:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 28 Feb 2017 06:03:33 GMT
ENV MONGO_MAJOR=3.4
# Tue, 28 Feb 2017 06:03:33 GMT
ENV MONGO_VERSION=3.4.2
# Tue, 28 Feb 2017 06:03:34 GMT
ENV MONGO_PACKAGE=mongodb-org
# Tue, 28 Feb 2017 06:03:35 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian jessie/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Tue, 28 Feb 2017 06:04:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 28 Feb 2017 06:04:42 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 28 Feb 2017 06:04:43 GMT
VOLUME [/data/db /data/configdb]
# Tue, 28 Feb 2017 06:04:44 GMT
COPY file:31c99192d9c1648c6f48dc5557de182c76080376f32685657130407fda705b3b in /entrypoint.sh 
# Tue, 28 Feb 2017 06:04:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Feb 2017 06:04:45 GMT
EXPOSE 27017/tcp
# Tue, 28 Feb 2017 06:04:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a29f630b22ecb9060e541038d275645574312de47421df2f8031621acb25d2f`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328ac2c79d69324cb76eb09114330606aaadbe073e6f6409e7cb131bcf287e5e`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 134.4 KB (134448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d628f74e0e9702828e26ab68da68fefaf2fe69942556c90360c55c057b82fdc6`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 1.2 MB (1217784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50753de132e0a3f79a598d92b47f33832a3915da40ff5636633b59e7c0b2e1f7`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fee098631ba283944156b1743f8eec8fb695c8e4fe2758fca9ef631badbff0`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4c3bdc152539bddccffa8c1ac1f4aae8333eaecf265d539fe2cca0e4fb8b95`  
		Last Modified: Thu, 02 Mar 2017 01:30:19 GMT  
		Size: 97.7 MB (97700620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0970b86ae43a0dbed0174ea6ff638ec1f8073308a14ceb2af0cc2c4a180da`  
		Last Modified: Thu, 02 Mar 2017 01:29:49 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fbca93d3445d1b12330b3ea1b965aa0fd80383d67a0ccd682c035f99c545b2`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3`

```console
$ docker pull mongo@sha256:3d4537f996bc28a6c6b694e22f46316c0629703420de60e8f46285ce1fe69260
```

-	Platforms:
	-	linux; amd64

### `mongo:3` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150420569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686238c7a975c9dcb154be65a2ea761b79e4401990860ab11549281e92f2e442`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 06:02:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 28 Feb 2017 06:02:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 06:02:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 28 Feb 2017 06:03:31 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 28 Feb 2017 06:03:31 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Tue, 28 Feb 2017 06:03:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 28 Feb 2017 06:03:33 GMT
ENV MONGO_MAJOR=3.4
# Tue, 28 Feb 2017 06:03:33 GMT
ENV MONGO_VERSION=3.4.2
# Tue, 28 Feb 2017 06:03:34 GMT
ENV MONGO_PACKAGE=mongodb-org
# Tue, 28 Feb 2017 06:03:35 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian jessie/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Tue, 28 Feb 2017 06:04:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 28 Feb 2017 06:04:42 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 28 Feb 2017 06:04:43 GMT
VOLUME [/data/db /data/configdb]
# Tue, 28 Feb 2017 06:04:44 GMT
COPY file:31c99192d9c1648c6f48dc5557de182c76080376f32685657130407fda705b3b in /entrypoint.sh 
# Tue, 28 Feb 2017 06:04:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Feb 2017 06:04:45 GMT
EXPOSE 27017/tcp
# Tue, 28 Feb 2017 06:04:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a29f630b22ecb9060e541038d275645574312de47421df2f8031621acb25d2f`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328ac2c79d69324cb76eb09114330606aaadbe073e6f6409e7cb131bcf287e5e`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 134.4 KB (134448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d628f74e0e9702828e26ab68da68fefaf2fe69942556c90360c55c057b82fdc6`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 1.2 MB (1217784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50753de132e0a3f79a598d92b47f33832a3915da40ff5636633b59e7c0b2e1f7`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fee098631ba283944156b1743f8eec8fb695c8e4fe2758fca9ef631badbff0`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4c3bdc152539bddccffa8c1ac1f4aae8333eaecf265d539fe2cca0e4fb8b95`  
		Last Modified: Thu, 02 Mar 2017 01:30:19 GMT  
		Size: 97.7 MB (97700620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0970b86ae43a0dbed0174ea6ff638ec1f8073308a14ceb2af0cc2c4a180da`  
		Last Modified: Thu, 02 Mar 2017 01:29:49 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fbca93d3445d1b12330b3ea1b965aa0fd80383d67a0ccd682c035f99c545b2`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:latest`

```console
$ docker pull mongo@sha256:0d4453308cc7f0fff863df2ecb7aae226ee7fe0c5257f857fd892edf6d2d9057
```

-	Platforms:
	-	linux; amd64

### `mongo:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150417788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad974e767ec4f06945b1e7ffdfc57bd10e06baf66cdaf5a003e0e6a36924e30b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 17:20:09 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 17 Jan 2017 17:20:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 17:20:15 GMT
ENV GOSU_VERSION=1.7
# Tue, 17 Jan 2017 17:20:31 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 17 Jan 2017 17:20:31 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Tue, 17 Jan 2017 17:20:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 17 Jan 2017 17:20:33 GMT
ENV MONGO_MAJOR=3.4
# Tue, 07 Feb 2017 20:00:04 GMT
ENV MONGO_VERSION=3.4.2
# Tue, 07 Feb 2017 20:00:04 GMT
ENV MONGO_PACKAGE=mongodb-org
# Tue, 07 Feb 2017 20:00:06 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian jessie/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Tue, 07 Feb 2017 20:00:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 07 Feb 2017 20:00:25 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 07 Feb 2017 20:00:25 GMT
VOLUME [/data/db /data/configdb]
# Wed, 08 Feb 2017 21:41:43 GMT
COPY file:31c99192d9c1648c6f48dc5557de182c76080376f32685657130407fda705b3b in /entrypoint.sh 
# Wed, 08 Feb 2017 21:41:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Feb 2017 21:41:44 GMT
EXPOSE 27017/tcp
# Wed, 08 Feb 2017 21:41:44 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef697e8d464ed2ff23031d40459cb953f5307a56be72272f01ff697016906892`  
		Last Modified: Wed, 18 Jan 2017 04:35:10 GMT  
		Size: 2.0 KB (2041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d7bf010c406d7c7cc8da3f41de8343b5bac1247cae7e49ec5a54768601f18d`  
		Last Modified: Wed, 18 Jan 2017 04:35:10 GMT  
		Size: 134.3 KB (134269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0b4f23ca2d9a83defb4c2155e82fa003fa3107c316884c45a09e0631076298`  
		Last Modified: Wed, 18 Jan 2017 04:35:10 GMT  
		Size: 1.2 MB (1217552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efff42d23e56240211ded6a6409387dc94d2179772646ea3e9c6377686e9e09`  
		Last Modified: Wed, 18 Jan 2017 04:36:09 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df9f20d1d07a58a87910069f2d1a6e7d8e8a7759bc5b6ef993d8ecc26cfdea7`  
		Last Modified: Tue, 07 Feb 2017 20:01:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b43ac0a1517cc46ff535665db717c6f78119ca8f73ad70e785720b615a5d415`  
		Last Modified: Tue, 07 Feb 2017 20:02:15 GMT  
		Size: 97.7 MB (97700417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010dcda0f65b87511f4117fa7aa079112fbead7f093d6c2847f0c2dac3b6a773`  
		Last Modified: Tue, 07 Feb 2017 20:01:46 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec68d17240b358d84c580d79b72e71a9dd2cf84934752efd918f6fca6f90c6f7`  
		Last Modified: Wed, 08 Feb 2017 21:43:12 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4.2-windowsservercore`

**does not exist** (yet?)

## `mongo:3.4-windowsservercore`

```console
$ docker pull mongo@sha256:90d80c5fdc534118c476edf158ce1d814325b2e6300a8573d7e1c2c2a8ad8b4a
```

-	Platforms:
	-	windows; amd64

### `mongo:3.4-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 GB (5050080913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce615778458a1fc587ba51e920671cbacf7368a70d6104d549d8988fb1790070`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 20 Jan 2017 21:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 01 Feb 2017 19:38:07 GMT
ENV MONGO_VERSION=3.4.1
# Wed, 01 Feb 2017 19:38:11 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.1-signed.msi
# Wed, 01 Feb 2017 19:38:14 GMT
ENV MONGO_DOWNLOAD_SHA256=c530c16b35cbc455d85700991bf96978a3dd1bab89ba7a11ff360777334e006a
# Wed, 01 Feb 2017 19:39:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 01 Feb 2017 19:39:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 01 Feb 2017 19:39:25 GMT
EXPOSE 27017/tcp
# Wed, 01 Feb 2017 19:39:29 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3430754e4d171ead00cf6766797a28abf3caf236f6c92c5c346ea2ad3955a129`  
		Size: 913.1 MB (913145061 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d9d048a108290b40b03a1a415360fe78a4038bfb48be71f6a1e05e92092624`  
		Last Modified: Fri, 20 Jan 2017 22:10:22 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddb40b5653725df89a50de47b1181f20f363d95e5012e4f8ee7033fdcba94db`  
		Last Modified: Wed, 01 Feb 2017 19:40:40 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd302c5a9befab7bc71e4a6f5ea68e115f2f90b46a67120b83d88f32655ca2d8`  
		Last Modified: Wed, 01 Feb 2017 19:40:38 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7727ae324d45b653fe1327e9664eccae3f308ba105278c5e36f5af820eaae3c1`  
		Last Modified: Wed, 01 Feb 2017 19:40:32 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc790f6d18c6514292b9f5d1ff0dfc70a77273a4e5531ac89077f49748114b7`  
		Last Modified: Wed, 01 Feb 2017 19:40:45 GMT  
		Size: 66.9 MB (66941388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed22695a264e27b9ca99ea637a535f7593e8a18b59505e9e45450c2008e2fbc`  
		Last Modified: Wed, 01 Feb 2017 19:40:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0e773c199fee9064b9481355c51d6304640a9d95f2da5e2ec7beef22c36c47`  
		Last Modified: Wed, 01 Feb 2017 19:40:30 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadec33a31905ad4a88806b0c6cda7cb4eb6f749494b91281a8438c9aab48e87`  
		Last Modified: Wed, 01 Feb 2017 19:40:30 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:90d80c5fdc534118c476edf158ce1d814325b2e6300a8573d7e1c2c2a8ad8b4a
```

-	Platforms:
	-	windows; amd64

### `mongo:3-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 GB (5050080913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce615778458a1fc587ba51e920671cbacf7368a70d6104d549d8988fb1790070`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 20 Jan 2017 21:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 01 Feb 2017 19:38:07 GMT
ENV MONGO_VERSION=3.4.1
# Wed, 01 Feb 2017 19:38:11 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.1-signed.msi
# Wed, 01 Feb 2017 19:38:14 GMT
ENV MONGO_DOWNLOAD_SHA256=c530c16b35cbc455d85700991bf96978a3dd1bab89ba7a11ff360777334e006a
# Wed, 01 Feb 2017 19:39:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 01 Feb 2017 19:39:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 01 Feb 2017 19:39:25 GMT
EXPOSE 27017/tcp
# Wed, 01 Feb 2017 19:39:29 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3430754e4d171ead00cf6766797a28abf3caf236f6c92c5c346ea2ad3955a129`  
		Size: 913.1 MB (913145061 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d9d048a108290b40b03a1a415360fe78a4038bfb48be71f6a1e05e92092624`  
		Last Modified: Fri, 20 Jan 2017 22:10:22 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddb40b5653725df89a50de47b1181f20f363d95e5012e4f8ee7033fdcba94db`  
		Last Modified: Wed, 01 Feb 2017 19:40:40 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd302c5a9befab7bc71e4a6f5ea68e115f2f90b46a67120b83d88f32655ca2d8`  
		Last Modified: Wed, 01 Feb 2017 19:40:38 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7727ae324d45b653fe1327e9664eccae3f308ba105278c5e36f5af820eaae3c1`  
		Last Modified: Wed, 01 Feb 2017 19:40:32 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc790f6d18c6514292b9f5d1ff0dfc70a77273a4e5531ac89077f49748114b7`  
		Last Modified: Wed, 01 Feb 2017 19:40:45 GMT  
		Size: 66.9 MB (66941388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed22695a264e27b9ca99ea637a535f7593e8a18b59505e9e45450c2008e2fbc`  
		Last Modified: Wed, 01 Feb 2017 19:40:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0e773c199fee9064b9481355c51d6304640a9d95f2da5e2ec7beef22c36c47`  
		Last Modified: Wed, 01 Feb 2017 19:40:30 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadec33a31905ad4a88806b0c6cda7cb4eb6f749494b91281a8438c9aab48e87`  
		Last Modified: Wed, 01 Feb 2017 19:40:30 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:90d80c5fdc534118c476edf158ce1d814325b2e6300a8573d7e1c2c2a8ad8b4a
```

-	Platforms:
	-	windows; amd64

### `mongo:windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 GB (5050080913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce615778458a1fc587ba51e920671cbacf7368a70d6104d549d8988fb1790070`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 20 Jan 2017 21:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 01 Feb 2017 19:38:07 GMT
ENV MONGO_VERSION=3.4.1
# Wed, 01 Feb 2017 19:38:11 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.1-signed.msi
# Wed, 01 Feb 2017 19:38:14 GMT
ENV MONGO_DOWNLOAD_SHA256=c530c16b35cbc455d85700991bf96978a3dd1bab89ba7a11ff360777334e006a
# Wed, 01 Feb 2017 19:39:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 01 Feb 2017 19:39:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 01 Feb 2017 19:39:25 GMT
EXPOSE 27017/tcp
# Wed, 01 Feb 2017 19:39:29 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3430754e4d171ead00cf6766797a28abf3caf236f6c92c5c346ea2ad3955a129`  
		Size: 913.1 MB (913145061 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d9d048a108290b40b03a1a415360fe78a4038bfb48be71f6a1e05e92092624`  
		Last Modified: Fri, 20 Jan 2017 22:10:22 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddb40b5653725df89a50de47b1181f20f363d95e5012e4f8ee7033fdcba94db`  
		Last Modified: Wed, 01 Feb 2017 19:40:40 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd302c5a9befab7bc71e4a6f5ea68e115f2f90b46a67120b83d88f32655ca2d8`  
		Last Modified: Wed, 01 Feb 2017 19:40:38 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7727ae324d45b653fe1327e9664eccae3f308ba105278c5e36f5af820eaae3c1`  
		Last Modified: Wed, 01 Feb 2017 19:40:32 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc790f6d18c6514292b9f5d1ff0dfc70a77273a4e5531ac89077f49748114b7`  
		Last Modified: Wed, 01 Feb 2017 19:40:45 GMT  
		Size: 66.9 MB (66941388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed22695a264e27b9ca99ea637a535f7593e8a18b59505e9e45450c2008e2fbc`  
		Last Modified: Wed, 01 Feb 2017 19:40:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0e773c199fee9064b9481355c51d6304640a9d95f2da5e2ec7beef22c36c47`  
		Last Modified: Wed, 01 Feb 2017 19:40:30 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadec33a31905ad4a88806b0c6cda7cb4eb6f749494b91281a8438c9aab48e87`  
		Last Modified: Wed, 01 Feb 2017 19:40:30 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
