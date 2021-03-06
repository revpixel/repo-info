## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:47d6d40b34d5e49d99716585a127672d7ba8d6efcfbabd575d77d9452556f4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2a5a9f991ed2e58ce245978afc1802d29ac8a2c27d4299e1ef82dbd8abe3ea5e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26843007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384100e79398ac0fee6267e9ba437e9f110e7e2f7e32ca3143259311a3e5f20c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Jul 2018 14:13:25 GMT
ADD file:eceadb32d029164d23db918d14c88df7186b6ee9645fa2f0c0a7e3e046a6a129 in / 
# Fri, 06 Jul 2018 14:13:25 GMT
CMD ["/bin/sh"]
# Fri, 06 Jul 2018 15:20:56 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 06 Jul 2018 15:26:04 GMT
RUN apk add --no-cache tzdata bash
# Fri, 06 Jul 2018 23:23:38 GMT
ENV INFLUXDB_VERSION=1.6.0
# Fri, 06 Jul 2018 23:23:48 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar ca-certificates &&     update-ca-certificates &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 06 Jul 2018 23:23:49 GMT
COPY file:3ee2bc0321c2aa2451df7a508649c3a54f0eebc1ef9b8a24967c58105b4d3160 in /etc/influxdb/influxdb.conf 
# Fri, 06 Jul 2018 23:23:49 GMT
EXPOSE 8086/tcp
# Fri, 06 Jul 2018 23:23:49 GMT
VOLUME [/var/lib/influxdb]
# Fri, 06 Jul 2018 23:23:50 GMT
COPY file:098affa3d1b749dacb263ddacfd86a5de1f598d6ba1f7c789ce482c66ee9c80b in /entrypoint.sh 
# Fri, 06 Jul 2018 23:23:50 GMT
COPY file:44e0050f3b04248a6900eace944c581b13b4ad9af1e5cfb91d837cb5e24356e6 in /init-influxdb.sh 
# Fri, 06 Jul 2018 23:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jul 2018 23:23:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a073c86ecf9e0f29180e80e9638d4c741970695851ea48247276c32c57e40282`  
		Last Modified: Fri, 06 Jul 2018 14:16:26 GMT  
		Size: 2.0 MB (2014658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fc09cd3173af0ccd136f8de7a9f2352e1e8d0fa0c7df8233c7c0092ff4faa`  
		Last Modified: Fri, 06 Jul 2018 15:23:05 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae3f16138c53432f86cf6073c068547f7d1de7bff552326d0033ffad158bd8b`  
		Last Modified: Fri, 06 Jul 2018 15:29:36 GMT  
		Size: 1.5 MB (1507834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32b2c99fd3a7edb735583c01cf1eed841940882aca182f4d1800387a8bf1dd0`  
		Last Modified: Fri, 06 Jul 2018 23:27:35 GMT  
		Size: 23.3 MB (23318759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ae730bbb82be965e9368c4a648ded8ef34a5203a19b44f2e7de8423a3552a4`  
		Last Modified: Fri, 06 Jul 2018 23:27:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4086b3024cf20c5384ee3eb02657b242d09e6b785f419990be6db025301210`  
		Last Modified: Fri, 06 Jul 2018 23:27:24 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d7982dda23803d401ba00f40d706c407cdce3cdeed2a16a142f4ae91fcb6f8`  
		Last Modified: Fri, 06 Jul 2018 23:27:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
