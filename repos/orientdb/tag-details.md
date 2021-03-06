<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:2.0.18`](#orientdb2018)
-	[`orientdb:2.1.25`](#orientdb2125)
-	[`orientdb:2.2.36`](#orientdb2236)
-	[`orientdb:2.2.36-spatial`](#orientdb2236-spatial)
-	[`orientdb:3.0.4`](#orientdb304)
-	[`orientdb:3.0.4-tp3`](#orientdb304-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:2.0.18`

```console
$ docker pull orientdb@sha256:a0bc1ce0ba9e03d2e0de3fa33ea8f1d5cd2b959a3e47128c1fbd5cf20dfc669c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:2.0.18` - linux; amd64

```console
$ docker pull orientdb@sha256:12a817863348d6a62bfa2b1370ebb48e7585613243f5fc830b12580f1304941e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292121735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6dd56c2dd92aa588b90879e0b032618f2f5b4c811b3a760de4c33a317ec700`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 17 Jul 2018 00:27:24 GMT
ADD file:370028dca6e8ca9ed228549d52231cf8139515cc3a14c00aaed75a60b679775f in / 
# Tue, 17 Jul 2018 00:27:24 GMT
CMD ["bash"]
# Tue, 17 Jul 2018 03:12:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jul 2018 03:13:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Jul 2018 03:13:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jul 2018 06:16:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Jul 2018 06:16:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Jul 2018 06:16:57 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 17 Jul 2018 06:16:58 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 17 Jul 2018 06:16:58 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 17 Jul 2018 06:16:58 GMT
ENV JAVA_VERSION=8u171
# Tue, 17 Jul 2018 06:16:58 GMT
ENV JAVA_DEBIAN_VERSION=8u171-b11-1~deb9u1
# Tue, 17 Jul 2018 06:16:59 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 17 Jul 2018 06:18:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 17 Jul 2018 06:18:07 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 17 Jul 2018 17:45:19 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 17 Jul 2018 17:45:19 GMT
ENV ORIENTDB_VERSION=2.0.18
# Tue, 17 Jul 2018 17:45:19 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9e7b7e7b6d95795b188adb4e5898a1b8
# Tue, 17 Jul 2018 17:45:20 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f562794536bbf8ae2145f96153e58b1e5d9211b3
# Tue, 17 Jul 2018 17:45:28 GMT
RUN mkdir /orientdb &&   wget  "http://central.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 17 Jul 2018 17:45:40 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jul 2018 17:45:40 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 17 Jul 2018 17:45:41 GMT
WORKDIR /orientdb
# Tue, 17 Jul 2018 17:45:41 GMT
EXPOSE 2424/tcp
# Tue, 17 Jul 2018 17:45:42 GMT
EXPOSE 2480/tcp
# Tue, 17 Jul 2018 17:45:42 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:55cbf04beb7001d222c71bfdeae780bda19d5cb37b8dbd65ff0d3e6a0b9b74e6`  
		Last Modified: Tue, 17 Jul 2018 00:42:31 GMT  
		Size: 45.3 MB (45310044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1607093a898cc241de8712e4361dcd907898fff35b945adca42db3963f3827b3`  
		Last Modified: Tue, 17 Jul 2018 03:53:34 GMT  
		Size: 10.7 MB (10740168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8ea045c9261c180a34df19cfc9bb3c3f28f29b279bf964ee801536e8244f2f`  
		Last Modified: Tue, 17 Jul 2018 03:53:32 GMT  
		Size: 4.3 MB (4336107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4eee24d4dacb41c21411e0477a741655303cdc48b18a948632c31f0f3a70bb8`  
		Last Modified: Tue, 17 Jul 2018 03:54:59 GMT  
		Size: 50.1 MB (50064642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58988e753d7a34080c68b53f7c27229d8f8fa80b9940c34d5cf77a9a2df10a0`  
		Last Modified: Tue, 17 Jul 2018 06:55:01 GMT  
		Size: 892.4 KB (892350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794a04897db9ebf95b1f6430cd4d4051bd227a5f0698b18404ccd4c59e43273d`  
		Last Modified: Tue, 17 Jul 2018 06:55:00 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fcfa476f730980d7a89f5ea34dd29c0c58e7cfe62652584e3adc38106e30ee`  
		Last Modified: Tue, 17 Jul 2018 06:54:59 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0539c80a02be3183761cc42f94a4f9cd5e3bc455f4ac3f4ecaab6d476b7fe330`  
		Last Modified: Tue, 17 Jul 2018 06:55:33 GMT  
		Size: 133.9 MB (133944795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fefc6dcf80a7be81ef627ec6ba8449a8ee7958a026ef947f99cac250af8f53`  
		Last Modified: Tue, 17 Jul 2018 06:54:59 GMT  
		Size: 246.7 KB (246694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859f31acdea5601d1c1149da1e78606ad6448187eb2cd448501e57b67f01b531`  
		Last Modified: Tue, 17 Jul 2018 17:46:21 GMT  
		Size: 46.6 MB (46586558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.1.25`

```console
$ docker pull orientdb@sha256:4fb192e0aee47ef9f14bc0a1f17fd82184a2fe85f3428fd06147b299c766338c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:2.1.25` - linux; amd64

```console
$ docker pull orientdb@sha256:41f942cc7f8fe6838c743e7bd1f05b84274ccffb6d2b89a6955b12ab333c65d1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104155793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c7f83ea73ae6cf1085f9d96b9bb13521e329de4d959fae5cc3023eb4d92f7d`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 06 Jul 2018 14:14:06 GMT
ADD file:25f61d70254b9807a40cd3e8d820f6a5ec0e1e596de04e325f6a33810393e95a in / 
# Fri, 06 Jul 2018 14:14:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Jul 2018 00:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 11 Jul 2018 00:34:54 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Wed, 11 Jul 2018 00:34:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_VERSION=8u171
# Wed, 11 Jul 2018 00:34:55 GMT
ENV JAVA_ALPINE_VERSION=8.171.11-r0
# Wed, 11 Jul 2018 00:35:00 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 11 Jul 2018 02:09:35 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 11 Jul 2018 02:09:35 GMT
ENV ORIENTDB_VERSION=2.1.25
# Wed, 11 Jul 2018 02:09:35 GMT
ENV ORIENTDB_DOWNLOAD_MD5=054da3fb7c56e7822b2af116966576ce
# Wed, 11 Jul 2018 02:09:35 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=b7b08242b40117ac8eb9a201f8704bde839dfcb8
# Wed, 11 Jul 2018 02:09:37 GMT
RUN apk add --update tar     && rm -rf /var/cache/apk/*
# Wed, 11 Jul 2018 02:09:46 GMT
RUN mkdir /orientdb &&   wget  "http://central.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 11 Jul 2018 02:09:46 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Wed, 11 Jul 2018 02:09:46 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 11 Jul 2018 02:09:47 GMT
WORKDIR /orientdb
# Wed, 11 Jul 2018 02:09:47 GMT
EXPOSE 2424/tcp
# Wed, 11 Jul 2018 02:09:47 GMT
EXPOSE 2480/tcp
# Wed, 11 Jul 2018 02:09:48 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:8e3ba11ec2a2b39ab372c60c16b421536e50e5ce64a0bc81765c2e38381bcff6`  
		Last Modified: Fri, 06 Jul 2018 04:15:58 GMT  
		Size: 2.2 MB (2206542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311ad0da45338842480bf25c6e6b7bb133b7b8cf709c3470db171ec370da5539`  
		Last Modified: Wed, 11 Jul 2018 00:37:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df312c74ce16f20eeb87b5640db9b1579a53534bd3e9f3de1e916fc62744bcf4`  
		Last Modified: Wed, 11 Jul 2018 00:38:02 GMT  
		Size: 70.6 MB (70581383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad644bdd33b77bd242bee8330b882a92a186c35c7b1ebf0b88cedb4a4a531d9`  
		Last Modified: Wed, 11 Jul 2018 02:12:06 GMT  
		Size: 279.7 KB (279663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e182054f4ca15021e166f9a555defaba9edd787c9848b4d45e965cd84db7a`  
		Last Modified: Wed, 11 Jul 2018 02:12:10 GMT  
		Size: 31.1 MB (31087966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.36`

```console
$ docker pull orientdb@sha256:45255ace6c5f1edd61b0168bd32fca7b2c6ea7f12f89d7ccffd708e5e2520aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:2.2.36` - linux; amd64

```console
$ docker pull orientdb@sha256:1759ec09da15cbba7c8380cddfbb2c25a5e2d4f3f32f728d6879d83671e7a7df
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120027511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82787e68d9b0830c9f0abb26cef85578e81e7b3d116ace0c576b6227843e1355`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 06 Jul 2018 14:14:06 GMT
ADD file:25f61d70254b9807a40cd3e8d820f6a5ec0e1e596de04e325f6a33810393e95a in / 
# Fri, 06 Jul 2018 14:14:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Jul 2018 00:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 11 Jul 2018 00:34:54 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Wed, 11 Jul 2018 00:34:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_VERSION=8u171
# Wed, 11 Jul 2018 00:34:55 GMT
ENV JAVA_ALPINE_VERSION=8.171.11-r0
# Wed, 11 Jul 2018 00:35:00 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 11 Jul 2018 02:09:35 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 11 Jul 2018 02:10:01 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 13 Jul 2018 18:20:15 GMT
ENV ORIENTDB_VERSION=2.2.36
# Fri, 13 Jul 2018 18:20:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0db280d733a000b75adb1e52c819497b
# Fri, 13 Jul 2018 18:20:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ce5527f027d40cb32af5537130316d5ea81588db
# Fri, 13 Jul 2018 18:20:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.36/orientdb-community-2.2.36.tar.gz
# Fri, 13 Jul 2018 18:20:17 GMT
RUN apk add --update tar curl     && rm -rf /var/cache/apk/*
# Fri, 13 Jul 2018 18:20:21 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 13 Jul 2018 18:20:21 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Fri, 13 Jul 2018 18:20:22 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 13 Jul 2018 18:20:22 GMT
WORKDIR /orientdb
# Fri, 13 Jul 2018 18:20:23 GMT
EXPOSE 2424/tcp
# Fri, 13 Jul 2018 18:20:23 GMT
EXPOSE 2480/tcp
# Fri, 13 Jul 2018 18:20:23 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:8e3ba11ec2a2b39ab372c60c16b421536e50e5ce64a0bc81765c2e38381bcff6`  
		Last Modified: Fri, 06 Jul 2018 04:15:58 GMT  
		Size: 2.2 MB (2206542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311ad0da45338842480bf25c6e6b7bb133b7b8cf709c3470db171ec370da5539`  
		Last Modified: Wed, 11 Jul 2018 00:37:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df312c74ce16f20eeb87b5640db9b1579a53534bd3e9f3de1e916fc62744bcf4`  
		Last Modified: Wed, 11 Jul 2018 00:38:02 GMT  
		Size: 70.6 MB (70581383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f24a3fc68869abdb6c85c5091ee13c964c5dc83eb34678aa27cb9916cec9d7`  
		Last Modified: Fri, 13 Jul 2018 18:22:16 GMT  
		Size: 766.0 KB (765975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271f35ad3bda372ba9b99e7b0b2c280ead9de0ad6eb5a47bfb1ee001662cd894`  
		Last Modified: Fri, 13 Jul 2018 18:22:22 GMT  
		Size: 46.5 MB (46473372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.36-spatial`

```console
$ docker pull orientdb@sha256:2364e7a79252d02ad26a785bafb1f0b1fb0003f37b7851d126ff3f0b9680e558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:2.2.36-spatial` - linux; amd64

```console
$ docker pull orientdb@sha256:100834e84e19ee4a4dc744443bb789030e4b6df2111727e628c4ca18fbf0ae3e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121230107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f66cf73f4f1c65cdecb54971e0300e4474c45f8ba27f79fc24191874c8caca6`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 06 Jul 2018 14:14:06 GMT
ADD file:25f61d70254b9807a40cd3e8d820f6a5ec0e1e596de04e325f6a33810393e95a in / 
# Fri, 06 Jul 2018 14:14:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Jul 2018 00:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 11 Jul 2018 00:34:54 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Wed, 11 Jul 2018 00:34:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_VERSION=8u171
# Wed, 11 Jul 2018 00:34:55 GMT
ENV JAVA_ALPINE_VERSION=8.171.11-r0
# Wed, 11 Jul 2018 00:35:00 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 11 Jul 2018 02:09:35 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 11 Jul 2018 02:10:01 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 13 Jul 2018 18:20:15 GMT
ENV ORIENTDB_VERSION=2.2.36
# Fri, 13 Jul 2018 18:20:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0db280d733a000b75adb1e52c819497b
# Fri, 13 Jul 2018 18:20:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ce5527f027d40cb32af5537130316d5ea81588db
# Fri, 13 Jul 2018 18:20:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.36/orientdb-community-2.2.36.tar.gz
# Fri, 13 Jul 2018 18:20:17 GMT
RUN apk add --update tar curl     && rm -rf /var/cache/apk/*
# Fri, 13 Jul 2018 18:20:21 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 13 Jul 2018 18:20:21 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Fri, 13 Jul 2018 18:20:22 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 13 Jul 2018 18:20:22 GMT
WORKDIR /orientdb
# Fri, 13 Jul 2018 18:20:23 GMT
EXPOSE 2424/tcp
# Fri, 13 Jul 2018 18:20:23 GMT
EXPOSE 2480/tcp
# Fri, 13 Jul 2018 18:20:23 GMT
CMD ["server.sh"]
# Fri, 13 Jul 2018 18:20:37 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_MD5=0b027f68e3dac4f03357d5f3064ec0f3
# Fri, 13 Jul 2018 18:20:38 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_SHA1=8f3adeddbad4d7f5436f4e2cdd418294135cd824
# Fri, 13 Jul 2018 18:20:38 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-spatial/2.2.36/orientdb-spatial-2.2.36-dist.jar
# Fri, 13 Jul 2018 18:20:39 GMT
RUN wget $ORIENTDB_DOWNLOAD_SPATIAL_URL     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_MD5 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | md5sum -c -     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_SHA1 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | sha1sum -c -     && mv orientdb-spatial-*-dist.jar /orientdb/lib/
```

-	Layers:
	-	`sha256:8e3ba11ec2a2b39ab372c60c16b421536e50e5ce64a0bc81765c2e38381bcff6`  
		Last Modified: Fri, 06 Jul 2018 04:15:58 GMT  
		Size: 2.2 MB (2206542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311ad0da45338842480bf25c6e6b7bb133b7b8cf709c3470db171ec370da5539`  
		Last Modified: Wed, 11 Jul 2018 00:37:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df312c74ce16f20eeb87b5640db9b1579a53534bd3e9f3de1e916fc62744bcf4`  
		Last Modified: Wed, 11 Jul 2018 00:38:02 GMT  
		Size: 70.6 MB (70581383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f24a3fc68869abdb6c85c5091ee13c964c5dc83eb34678aa27cb9916cec9d7`  
		Last Modified: Fri, 13 Jul 2018 18:22:16 GMT  
		Size: 766.0 KB (765975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271f35ad3bda372ba9b99e7b0b2c280ead9de0ad6eb5a47bfb1ee001662cd894`  
		Last Modified: Fri, 13 Jul 2018 18:22:22 GMT  
		Size: 46.5 MB (46473372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7b192473976bfbc97c661bce404aba994e83aff1a633d170b942bd374c3cd9`  
		Last Modified: Fri, 13 Jul 2018 18:22:43 GMT  
		Size: 1.2 MB (1202596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.4`

```console
$ docker pull orientdb@sha256:bf76789332b52767232c63eefa4114fbc43c094d72fb88e369df6a29fc5603d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:3.0.4` - linux; amd64

```console
$ docker pull orientdb@sha256:d2aa32c1655a56ceed4b6a9b696dba517a2822205fdfad43cd714f8d1841a0cb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109943868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35aa23fd750416c2736370508bc13243df20790f2b14f10f24d478a0ab051220`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 06 Jul 2018 14:14:06 GMT
ADD file:25f61d70254b9807a40cd3e8d820f6a5ec0e1e596de04e325f6a33810393e95a in / 
# Fri, 06 Jul 2018 14:14:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Jul 2018 00:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 11 Jul 2018 00:34:54 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Wed, 11 Jul 2018 00:34:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_VERSION=8u171
# Wed, 11 Jul 2018 00:34:55 GMT
ENV JAVA_ALPINE_VERSION=8.171.11-r0
# Wed, 11 Jul 2018 00:35:00 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 11 Jul 2018 02:09:35 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 11 Jul 2018 02:10:01 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 13 Jul 2018 18:21:05 GMT
ENV ORIENTDB_VERSION=3.0.4
# Fri, 13 Jul 2018 18:21:05 GMT
ENV ORIENTDB_DOWNLOAD_MD5=e33e7462d2883f962f30e073418d91e0
# Fri, 13 Jul 2018 18:21:05 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9449906df999ff45c8f561383d1dd573b1e4ae4c
# Fri, 13 Jul 2018 18:21:05 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.4/orientdb-community-3.0.4.tar.gz
# Fri, 13 Jul 2018 18:21:07 GMT
RUN apk add --update tar curl     && rm -rf /var/cache/apk/*
# Fri, 13 Jul 2018 18:21:13 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 13 Jul 2018 18:21:14 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Fri, 13 Jul 2018 18:21:14 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 13 Jul 2018 18:21:14 GMT
WORKDIR /orientdb
# Fri, 13 Jul 2018 18:21:15 GMT
EXPOSE 2424/tcp
# Fri, 13 Jul 2018 18:21:15 GMT
EXPOSE 2480/tcp
# Fri, 13 Jul 2018 18:21:15 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:8e3ba11ec2a2b39ab372c60c16b421536e50e5ce64a0bc81765c2e38381bcff6`  
		Last Modified: Fri, 06 Jul 2018 04:15:58 GMT  
		Size: 2.2 MB (2206542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311ad0da45338842480bf25c6e6b7bb133b7b8cf709c3470db171ec370da5539`  
		Last Modified: Wed, 11 Jul 2018 00:37:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df312c74ce16f20eeb87b5640db9b1579a53534bd3e9f3de1e916fc62744bcf4`  
		Last Modified: Wed, 11 Jul 2018 00:38:02 GMT  
		Size: 70.6 MB (70581383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae738f4536d5a8565562ec8b5250727e4cbe134f8d7a1b5d1cfa4ada9e30695`  
		Last Modified: Fri, 13 Jul 2018 18:23:02 GMT  
		Size: 766.0 KB (765977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0f5884d84ee0b810e628efe9c64a2dcb9c3e23a66728c4305562d87fc84349`  
		Last Modified: Fri, 13 Jul 2018 18:23:07 GMT  
		Size: 36.4 MB (36389727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.4-tp3`

```console
$ docker pull orientdb@sha256:a47ec14bb32b234f9262ab1599088fa53f0825db4cce625334f0174f1b5a389f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:3.0.4-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:0fb38268b7ac730d0e28bf7d89ad22c3bcdb12491ab1e326706309e2e86af9fd
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137224554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490bbc6d33fb7043fffdc8db6fb3e4e7656d37610e03aa826aecac2ebe601305`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 06 Jul 2018 14:14:06 GMT
ADD file:25f61d70254b9807a40cd3e8d820f6a5ec0e1e596de04e325f6a33810393e95a in / 
# Fri, 06 Jul 2018 14:14:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Jul 2018 00:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 11 Jul 2018 00:34:54 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Wed, 11 Jul 2018 00:34:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_VERSION=8u171
# Wed, 11 Jul 2018 00:34:55 GMT
ENV JAVA_ALPINE_VERSION=8.171.11-r0
# Wed, 11 Jul 2018 00:35:00 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 11 Jul 2018 02:09:35 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 11 Jul 2018 02:10:01 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 13 Jul 2018 18:21:05 GMT
ENV ORIENTDB_VERSION=3.0.4
# Fri, 13 Jul 2018 18:21:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=c9448b3786c443d9753d22a1a24153e7
# Fri, 13 Jul 2018 18:21:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1ce49f03033a40354207d4ae1fb7dec6de70ea02
# Fri, 13 Jul 2018 18:21:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.4/orientdb-tp3-3.0.4.tar.gz
# Fri, 13 Jul 2018 18:21:31 GMT
RUN apk add --update tar curl     && rm -rf /var/cache/apk/*
# Fri, 13 Jul 2018 18:21:52 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 13 Jul 2018 18:21:53 GMT
ADD file:99b7a1625594810d4a6ad850d8e45ce20c6e5e95127b6a7316cae65e7aa03c13 in /orientdb/config 
# Fri, 13 Jul 2018 18:21:53 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Fri, 13 Jul 2018 18:21:53 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 13 Jul 2018 18:21:53 GMT
WORKDIR /orientdb
# Fri, 13 Jul 2018 18:21:54 GMT
EXPOSE 2424/tcp
# Fri, 13 Jul 2018 18:21:54 GMT
EXPOSE 2480/tcp
# Fri, 13 Jul 2018 18:21:55 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:8e3ba11ec2a2b39ab372c60c16b421536e50e5ce64a0bc81765c2e38381bcff6`  
		Last Modified: Fri, 06 Jul 2018 04:15:58 GMT  
		Size: 2.2 MB (2206542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311ad0da45338842480bf25c6e6b7bb133b7b8cf709c3470db171ec370da5539`  
		Last Modified: Wed, 11 Jul 2018 00:37:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df312c74ce16f20eeb87b5640db9b1579a53534bd3e9f3de1e916fc62744bcf4`  
		Last Modified: Wed, 11 Jul 2018 00:38:02 GMT  
		Size: 70.6 MB (70581383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ebf520993f1e9382ea56f13edb8774e95ab5db9a7732e186e245236111235a`  
		Last Modified: Fri, 13 Jul 2018 18:23:40 GMT  
		Size: 766.0 KB (765979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a25a68b3bc26d6d56dc99783396f1292778294b29d0a4c3a96bafb7d256517e`  
		Last Modified: Fri, 13 Jul 2018 18:23:48 GMT  
		Size: 63.7 MB (63669034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebead9c8f815657fe788d239b6f708f6f0e57502bacf5ba08e4600c366b0e8a0`  
		Last Modified: Fri, 13 Jul 2018 18:23:39 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:bf76789332b52767232c63eefa4114fbc43c094d72fb88e369df6a29fc5603d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:d2aa32c1655a56ceed4b6a9b696dba517a2822205fdfad43cd714f8d1841a0cb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109943868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35aa23fd750416c2736370508bc13243df20790f2b14f10f24d478a0ab051220`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 06 Jul 2018 14:14:06 GMT
ADD file:25f61d70254b9807a40cd3e8d820f6a5ec0e1e596de04e325f6a33810393e95a in / 
# Fri, 06 Jul 2018 14:14:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Jul 2018 00:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 11 Jul 2018 00:34:54 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Wed, 11 Jul 2018 00:34:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Wed, 11 Jul 2018 00:34:54 GMT
ENV JAVA_VERSION=8u171
# Wed, 11 Jul 2018 00:34:55 GMT
ENV JAVA_ALPINE_VERSION=8.171.11-r0
# Wed, 11 Jul 2018 00:35:00 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 11 Jul 2018 02:09:35 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 11 Jul 2018 02:10:01 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 13 Jul 2018 18:21:05 GMT
ENV ORIENTDB_VERSION=3.0.4
# Fri, 13 Jul 2018 18:21:05 GMT
ENV ORIENTDB_DOWNLOAD_MD5=e33e7462d2883f962f30e073418d91e0
# Fri, 13 Jul 2018 18:21:05 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9449906df999ff45c8f561383d1dd573b1e4ae4c
# Fri, 13 Jul 2018 18:21:05 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.4/orientdb-community-3.0.4.tar.gz
# Fri, 13 Jul 2018 18:21:07 GMT
RUN apk add --update tar curl     && rm -rf /var/cache/apk/*
# Fri, 13 Jul 2018 18:21:13 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 13 Jul 2018 18:21:14 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Fri, 13 Jul 2018 18:21:14 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 13 Jul 2018 18:21:14 GMT
WORKDIR /orientdb
# Fri, 13 Jul 2018 18:21:15 GMT
EXPOSE 2424/tcp
# Fri, 13 Jul 2018 18:21:15 GMT
EXPOSE 2480/tcp
# Fri, 13 Jul 2018 18:21:15 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:8e3ba11ec2a2b39ab372c60c16b421536e50e5ce64a0bc81765c2e38381bcff6`  
		Last Modified: Fri, 06 Jul 2018 04:15:58 GMT  
		Size: 2.2 MB (2206542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311ad0da45338842480bf25c6e6b7bb133b7b8cf709c3470db171ec370da5539`  
		Last Modified: Wed, 11 Jul 2018 00:37:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df312c74ce16f20eeb87b5640db9b1579a53534bd3e9f3de1e916fc62744bcf4`  
		Last Modified: Wed, 11 Jul 2018 00:38:02 GMT  
		Size: 70.6 MB (70581383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae738f4536d5a8565562ec8b5250727e4cbe134f8d7a1b5d1cfa4ada9e30695`  
		Last Modified: Fri, 13 Jul 2018 18:23:02 GMT  
		Size: 766.0 KB (765977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0f5884d84ee0b810e628efe9c64a2dcb9c3e23a66728c4305562d87fc84349`  
		Last Modified: Fri, 13 Jul 2018 18:23:07 GMT  
		Size: 36.4 MB (36389727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
