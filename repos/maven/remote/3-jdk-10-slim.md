## `maven:3-jdk-10-slim`

```console
$ docker pull maven@sha256:697d65f843739ea0ded8f354ec55f08da05c42d51f4efb5efb5be166d1566dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `maven:3-jdk-10-slim` - linux; amd64

```console
$ docker pull maven@sha256:2f93afddfeb3e9cced80f7cede8f0be1608b245092263b990311a970fcc4f437
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293549761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a9ab0e82d2635594a066d6ea7b6d120fa41b2a5a095cb7fe95ca87ef6df09f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 12 Dec 2017 01:43:25 GMT
ADD file:f105fa3aa445df54e1e78b4ba607c2724f1dc586b1e060c482c798966d97c635 in / 
# Tue, 12 Dec 2017 01:43:25 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 05:39:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 18 Jan 2018 20:24:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Thu, 18 Jan 2018 20:24:13 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2018 20:24:14 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 18 Jan 2018 20:24:15 GMT
RUN ln -svT "/usr/lib/jvm/java-10-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 18 Jan 2018 20:24:16 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 18 Jan 2018 20:24:16 GMT
ENV JAVA_VERSION=10-ea+32
# Thu, 18 Jan 2018 20:24:16 GMT
ENV JAVA_DEBIAN_VERSION=10~32-1
# Thu, 18 Jan 2018 20:37:24 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y 		openjdk-10-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 18 Jan 2018 20:39:04 GMT
CMD ["jshell"]
# Tue, 13 Feb 2018 19:11:10 GMT
ARG MAVEN_VERSION=3.5.2
# Tue, 13 Feb 2018 19:11:11 GMT
ARG USER_HOME_DIR=/root
# Tue, 13 Feb 2018 19:11:11 GMT
ARG SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff
# Tue, 13 Feb 2018 19:11:11 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries
# Tue, 13 Feb 2018 19:11:26 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries MAVEN_VERSION=3.5.2 SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl   && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2018 19:11:27 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries MAVEN_VERSION=3.5.2 SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff USER_HOME_DIR=/root
RUN ln -s /etc/java-10-openjdk /usr/lib/jvm/java-10-openjdk-$(dpkg --print-architecture)/conf
# Tue, 13 Feb 2018 19:11:30 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.2/binaries MAVEN_VERSION=3.5.2 SHA=707b1f6e390a65bde4af4cdaf2a24d45fc19a6ded00fff02e91626e3e42ceaff USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 13 Feb 2018 19:11:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 13 Feb 2018 19:11:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 13 Feb 2018 19:11:31 GMT
COPY file:fb726a12bbbf8ff54c8d9fceef4fa3018c11a435bfa04ee5f73156c544907861 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 13 Feb 2018 19:11:31 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 13 Feb 2018 19:11:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 13 Feb 2018 19:11:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7dadf3208611439968d74844a1c976f4664c77dbe43c9e5b63a825002a5cd02f`  
		Last Modified: Tue, 12 Dec 2017 01:51:57 GMT  
		Size: 25.2 MB (25200134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349fcab9b82f6a693cf54bf9000507a4d7f9156532a75463f72361a998cf0067`  
		Last Modified: Tue, 12 Dec 2017 05:56:46 GMT  
		Size: 461.4 KB (461353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701eb131c0fa109136fbeb16463be04da3eb927af807bf1e8ef59dd7845cfa2a`  
		Last Modified: Thu, 18 Jan 2018 20:54:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0d59c5136e482909a148e9f903702243e76483db269f5f8467c67b1d6bd7e`  
		Last Modified: Thu, 18 Jan 2018 20:54:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348cf3a40bd34f3548984028ade1190d13604c41bee3dbd03208f25e2dccd1f7`  
		Last Modified: Thu, 18 Jan 2018 20:54:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416c2c6b52f759937294ff6dcf12aa999f24f86dddcd43628cc7069158ef5662`  
		Last Modified: Thu, 18 Jan 2018 21:04:17 GMT  
		Size: 255.8 MB (255834050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7b4934d650d07374e1fdc17e6baf50bba6ac1705af7241899c6e593347b006`  
		Last Modified: Tue, 13 Feb 2018 19:12:26 GMT  
		Size: 3.2 MB (3168435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f270dc46114b5a14fa5d3669f03e26a7ded915e89e366561da4440389a0217`  
		Last Modified: Tue, 13 Feb 2018 19:12:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c721ac9f05fbd6b0790aee14aad7e23f9a266acf0603f6e6f8a9284eff23a77c`  
		Last Modified: Tue, 13 Feb 2018 19:12:30 GMT  
		Size: 8.9 MB (8883842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c87030316d606ec309f0e71e821ad74163975dc344a93dd0141548417ed6b65`  
		Last Modified: Tue, 13 Feb 2018 19:12:25 GMT  
		Size: 752.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ceef44366eeb7b4defc6054a19af2cada2998445fb2a7a40b23a9f447cac46`  
		Last Modified: Tue, 13 Feb 2018 19:12:26 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip