<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:0.52.0`](#rocketchat0520)
-	[`rocket.chat:0.52`](#rocketchat052)
-	[`rocket.chat:0`](#rocketchat0)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:0.52.0`

**does not exist** (yet?)

## `rocket.chat:0.52`

**does not exist** (yet?)

## `rocket.chat:0`

```console
$ docker pull rocket.chat@sha256:fb84ed7f453ce780da0c6b0a89836d26e2060ee5cc3f471672a6affa443dd294
```

-	Platforms:
	-	linux; amd64

### `rocket.chat:0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171210753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60593facc5ff6a58a1261aa0cd1374e3184b9f49c416dd79666129294da07f4e`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 00:00:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 18:40:18 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 17 Jan 2017 18:40:21 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     0034A06D9D9B0064CE8ADF6BF1747F4AD2306D93     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done
# Tue, 17 Jan 2017 18:40:22 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 01 Feb 2017 17:33:23 GMT
ENV NODE_VERSION=4.7.3
# Wed, 01 Feb 2017 17:33:32 GMT
RUN buildDeps='xz-utils'     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 01 Feb 2017 17:33:32 GMT
CMD ["node"]
# Wed, 01 Feb 2017 18:02:56 GMT
MAINTAINER buildmaster@rocket.chat
# Wed, 01 Feb 2017 18:02:57 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat
# Wed, 01 Feb 2017 18:02:58 GMT
VOLUME [/app/uploads]
# Wed, 01 Feb 2017 18:02:59 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Wed, 08 Feb 2017 21:51:53 GMT
ENV RC_VERSION=0.51.0
# Wed, 08 Feb 2017 21:51:54 GMT
WORKDIR /app
# Wed, 08 Feb 2017 21:52:25 GMT
RUN curl -fSL "https://rocket.chat/releases/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://rocket.chat/releases/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install
# Wed, 08 Feb 2017 21:52:27 GMT
USER [rocketchat]
# Wed, 08 Feb 2017 21:52:27 GMT
WORKDIR /app/bundle
# Wed, 08 Feb 2017 21:52:28 GMT
ENV MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 08 Feb 2017 21:52:28 GMT
EXPOSE 3000/tcp
# Wed, 08 Feb 2017 21:52:29 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce5728aad85a763fe3c419db16885eb6f7a670a42824ea618414b8fb309ccde`  
		Last Modified: Tue, 17 Jan 2017 00:19:41 GMT  
		Size: 18.5 MB (18535441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b82ee2770671a783ceea13aa8e9aa8afa8a06918b59e3e3f19d78c962366cc`  
		Last Modified: Wed, 18 Jan 2017 05:32:21 GMT  
		Size: 4.3 KB (4342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16843b1a499ad849e8b50ec678d73ae4acd46758b9b3beb7a68dfc553e5d6a5`  
		Last Modified: Wed, 18 Jan 2017 05:32:22 GMT  
		Size: 97.2 KB (97215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff1a933f493b1ab353ba1f52e973e29b9e20629350edd628e309b9adee3a09`  
		Last Modified: Wed, 01 Feb 2017 17:48:48 GMT  
		Size: 12.3 MB (12264659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d912c781ed446a0aa5c856ef5e5482bf0b0e9f0f414b33428913440415375bc`  
		Last Modified: Wed, 01 Feb 2017 18:03:53 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1ca6a071142ab785837d524e6dcb05c4d68caaf136663997dca8d58f3ab30f`  
		Last Modified: Wed, 01 Feb 2017 18:03:53 GMT  
		Size: 94.7 KB (94663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fceaf748e640506bb3a0da0ee697ff13ca551fe76435e565f7505dad439eaa2a`  
		Last Modified: Wed, 08 Feb 2017 21:53:11 GMT  
		Size: 88.9 MB (88851134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:fb84ed7f453ce780da0c6b0a89836d26e2060ee5cc3f471672a6affa443dd294
```

-	Platforms:
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171210753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60593facc5ff6a58a1261aa0cd1374e3184b9f49c416dd79666129294da07f4e`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 16 Jan 2017 20:35:09 GMT
ADD file:89ecb642d662ee7edbb868340551106d51336c7e589fdaca4111725ec64da957 in / 
# Mon, 16 Jan 2017 20:35:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2017 00:00:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jan 2017 18:40:18 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 17 Jan 2017 18:40:21 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     0034A06D9D9B0064CE8ADF6BF1747F4AD2306D93     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done
# Tue, 17 Jan 2017 18:40:22 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 01 Feb 2017 17:33:23 GMT
ENV NODE_VERSION=4.7.3
# Wed, 01 Feb 2017 17:33:32 GMT
RUN buildDeps='xz-utils'     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 01 Feb 2017 17:33:32 GMT
CMD ["node"]
# Wed, 01 Feb 2017 18:02:56 GMT
MAINTAINER buildmaster@rocket.chat
# Wed, 01 Feb 2017 18:02:57 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat
# Wed, 01 Feb 2017 18:02:58 GMT
VOLUME [/app/uploads]
# Wed, 01 Feb 2017 18:02:59 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Wed, 08 Feb 2017 21:51:53 GMT
ENV RC_VERSION=0.51.0
# Wed, 08 Feb 2017 21:51:54 GMT
WORKDIR /app
# Wed, 08 Feb 2017 21:52:25 GMT
RUN curl -fSL "https://rocket.chat/releases/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://rocket.chat/releases/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install
# Wed, 08 Feb 2017 21:52:27 GMT
USER [rocketchat]
# Wed, 08 Feb 2017 21:52:27 GMT
WORKDIR /app/bundle
# Wed, 08 Feb 2017 21:52:28 GMT
ENV MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 08 Feb 2017 21:52:28 GMT
EXPOSE 3000/tcp
# Wed, 08 Feb 2017 21:52:29 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:5040bd2983909aa8896b9932438c3f1479d25ae837a5f6220242a264d0221f2d`  
		Last Modified: Mon, 16 Jan 2017 20:43:26 GMT  
		Size: 51.4 MB (51361210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce5728aad85a763fe3c419db16885eb6f7a670a42824ea618414b8fb309ccde`  
		Last Modified: Tue, 17 Jan 2017 00:19:41 GMT  
		Size: 18.5 MB (18535441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b82ee2770671a783ceea13aa8e9aa8afa8a06918b59e3e3f19d78c962366cc`  
		Last Modified: Wed, 18 Jan 2017 05:32:21 GMT  
		Size: 4.3 KB (4342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16843b1a499ad849e8b50ec678d73ae4acd46758b9b3beb7a68dfc553e5d6a5`  
		Last Modified: Wed, 18 Jan 2017 05:32:22 GMT  
		Size: 97.2 KB (97215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff1a933f493b1ab353ba1f52e973e29b9e20629350edd628e309b9adee3a09`  
		Last Modified: Wed, 01 Feb 2017 17:48:48 GMT  
		Size: 12.3 MB (12264659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d912c781ed446a0aa5c856ef5e5482bf0b0e9f0f414b33428913440415375bc`  
		Last Modified: Wed, 01 Feb 2017 18:03:53 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1ca6a071142ab785837d524e6dcb05c4d68caaf136663997dca8d58f3ab30f`  
		Last Modified: Wed, 01 Feb 2017 18:03:53 GMT  
		Size: 94.7 KB (94663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fceaf748e640506bb3a0da0ee697ff13ca551fe76435e565f7505dad439eaa2a`  
		Last Modified: Wed, 08 Feb 2017 21:53:11 GMT  
		Size: 88.9 MB (88851134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
