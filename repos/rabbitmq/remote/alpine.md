## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:cf00b2410e0d548d2bda21528f2123327ea998ab4df63ba0d08e1032d50c4be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `rabbitmq:alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:e0ac8dac87078102886911c68a317f4e6752865a356ef73170de2104001438d9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31786728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce0da9a95ef5ef46a2106db6be54069e9fd5f16ab9a46610487cc4083def67a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Jul 2018 14:14:06 GMT
ADD file:25f61d70254b9807a40cd3e8d820f6a5ec0e1e596de04e325f6a33810393e95a in / 
# Fri, 06 Jul 2018 14:14:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Jul 2018 00:49:52 GMT
RUN addgroup -S rabbitmq && adduser -S -h /var/lib/rabbitmq -G rabbitmq rabbitmq
# Wed, 11 Jul 2018 00:49:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 11 Jul 2018 00:50:00 GMT
RUN apk add --no-cache 		bash 		procps 		erlang-asn1 		erlang-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang 		erlang-os-mon 		erlang-public-key 		erlang-sasl 		erlang-ssl 		erlang-syntax-tools 		erlang-xmerl
# Wed, 11 Jul 2018 00:50:00 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Wed, 11 Jul 2018 00:50:00 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Jul 2018 00:50:01 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jul 2018 00:50:01 GMT
ENV RABBITMQ_GPG_KEY=0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Jul 2018 00:50:01 GMT
ENV RABBITMQ_VERSION=3.7.7
# Wed, 11 Jul 2018 00:50:01 GMT
ENV RABBITMQ_GITHUB_TAG=v3.7.7
# Tue, 31 Jul 2018 17:30:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gnupg 		libressl 		wget 		xz 	; 		wget -O rabbitmq-server.tar.xz.asc "https://github.com/rabbitmq/rabbitmq-server/releases/download/$RABBITMQ_GITHUB_TAG/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz.asc"; 	wget -O rabbitmq-server.tar.xz     "https://github.com/rabbitmq/rabbitmq-server/releases/download/$RABBITMQ_GITHUB_TAG/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$RABBITMQ_GPG_KEY"; 	gpg --batch --verify rabbitmq-server.tar.xz.asc rabbitmq-server.tar.xz; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar 		--extract 		--verbose 		--file rabbitmq-server.tar.xz 		--directory "$RABBITMQ_HOME" 		--strip-components 1 	; 	rm -f rabbitmq-server.tar.xz*; 		grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -ri 's!^(SYS_PREFIX=).*$!\1!g' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 		apk del .build-deps
# Tue, 31 Jul 2018 17:30:13 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 31 Jul 2018 17:30:14 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq
# Tue, 31 Jul 2018 17:30:14 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 31 Jul 2018 17:30:15 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Tue, 31 Jul 2018 17:30:16 GMT
RUN ln -sf "$RABBITMQ_HOME/plugins" /plugins
# Tue, 31 Jul 2018 17:30:17 GMT
COPY file:03f4165e1aefa09a8d97a5e402638f735384652cec9e89f399f563063d59ab58 in /usr/local/bin/ 
# Tue, 31 Jul 2018 17:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Jul 2018 17:30:17 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Tue, 31 Jul 2018 17:30:18 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8e3ba11ec2a2b39ab372c60c16b421536e50e5ce64a0bc81765c2e38381bcff6`  
		Last Modified: Fri, 06 Jul 2018 04:15:58 GMT  
		Size: 2.2 MB (2206542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10f44428f6e6a5afdef8fe54204cfd125324a97d48dcc47f7d95b77f5af6861`  
		Last Modified: Wed, 11 Jul 2018 00:52:17 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5244a7ea21b9ecd309ffe64ba8c7ae45eb532168c7ba2f7611f599a1c98f3416`  
		Last Modified: Wed, 11 Jul 2018 00:52:17 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7bc339e1a4e2711bfc192c5a61f1632a180d3d0cda8ce1fd7d8f43973f2618`  
		Last Modified: Wed, 11 Jul 2018 00:52:21 GMT  
		Size: 18.7 MB (18707335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db797b68314f993a3a4ab363fb3afb9ca3fe9d6b59d3b6ae4e9b46688e118e9`  
		Last Modified: Tue, 31 Jul 2018 17:37:43 GMT  
		Size: 10.9 MB (10857863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96af1dfb2182fb48b46f775ce3895ada9bd021eee88ce2da4870ef70832910`  
		Last Modified: Tue, 31 Jul 2018 17:37:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54e40bd6595913e170dafa4900a8a65590aefa16f8c51309c12f44e1b209f33`  
		Last Modified: Tue, 31 Jul 2018 17:37:41 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394d42da5b7402dabd80ec9c6f6fcfc28116d810373d2f24933af9eb73fd20a6`  
		Last Modified: Tue, 31 Jul 2018 17:37:41 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd4da0f7b2c70a1c7a4fe258532821aeec5f466d381158a63fd18fe5b3881c5`  
		Last Modified: Tue, 31 Jul 2018 17:37:41 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:9de88dff341d71a5d7b573936484f776a1211e54b013387b4bc43a08ba2689e1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29221878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03fe901b1d2300ddd7f946f44267d1e38d69582139cb763bf8c2e637c0e0500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Jul 2018 08:41:03 GMT
ADD file:199a5a48bddabaf1f649f58f3b17c323a1aa1a50e939dfdea3542e4041e91b7b in / 
# Fri, 06 Jul 2018 08:41:03 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 06 Jul 2018 08:41:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Jul 2018 09:31:21 GMT
RUN addgroup -S rabbitmq && adduser -S -h /var/lib/rabbitmq -G rabbitmq rabbitmq
# Wed, 11 Jul 2018 09:31:24 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 11 Jul 2018 09:31:32 GMT
RUN apk add --no-cache 		bash 		procps 		erlang-asn1 		erlang-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang 		erlang-os-mon 		erlang-public-key 		erlang-sasl 		erlang-ssl 		erlang-syntax-tools 		erlang-xmerl
# Wed, 11 Jul 2018 09:31:33 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Wed, 11 Jul 2018 09:31:33 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Jul 2018 09:31:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jul 2018 09:31:35 GMT
ENV RABBITMQ_GPG_KEY=0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Jul 2018 09:31:35 GMT
ENV RABBITMQ_VERSION=3.7.7
# Wed, 11 Jul 2018 09:31:36 GMT
ENV RABBITMQ_GITHUB_TAG=v3.7.7
# Wed, 01 Aug 2018 10:29:22 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gnupg 		libressl 		wget 		xz 	; 		wget -O rabbitmq-server.tar.xz.asc "https://github.com/rabbitmq/rabbitmq-server/releases/download/$RABBITMQ_GITHUB_TAG/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz.asc"; 	wget -O rabbitmq-server.tar.xz     "https://github.com/rabbitmq/rabbitmq-server/releases/download/$RABBITMQ_GITHUB_TAG/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$RABBITMQ_GPG_KEY"; 	gpg --batch --verify rabbitmq-server.tar.xz.asc rabbitmq-server.tar.xz; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar 		--extract 		--verbose 		--file rabbitmq-server.tar.xz 		--directory "$RABBITMQ_HOME" 		--strip-components 1 	; 	rm -f rabbitmq-server.tar.xz*; 		grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -ri 's!^(SYS_PREFIX=).*$!\1!g' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 		apk del .build-deps
# Wed, 01 Aug 2018 10:29:23 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 01 Aug 2018 10:29:28 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq
# Wed, 01 Aug 2018 10:29:30 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 01 Aug 2018 10:29:34 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Wed, 01 Aug 2018 10:29:40 GMT
RUN ln -sf "$RABBITMQ_HOME/plugins" /plugins
# Wed, 01 Aug 2018 10:29:44 GMT
COPY file:03f4165e1aefa09a8d97a5e402638f735384652cec9e89f399f563063d59ab58 in /usr/local/bin/ 
# Wed, 01 Aug 2018 10:29:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Aug 2018 10:29:49 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Wed, 01 Aug 2018 10:29:52 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:47e04371c99027fae42871b720fdc6cdddcb65062bfa05f0c3bb0a594cb5bbbd`  
		Last Modified: Wed, 27 Jun 2018 19:15:35 GMT  
		Size: 2.1 MB (2099514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4103359e1ecd9a7253d8b8a041d4e81db1ff4a5e1950bc0e02305d221c9e6c2`  
		Last Modified: Fri, 06 Jul 2018 08:42:09 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5badc5e7d94ed765385fefc3b0ff46d21dd49d4b8a83637dcb18e9e5ec98b613`  
		Last Modified: Wed, 11 Jul 2018 09:34:17 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4a3ab275eff3f1a137597336d806ec46342bffee98de57a67271be528aacba`  
		Last Modified: Wed, 11 Jul 2018 09:34:16 GMT  
		Size: 8.9 KB (8930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18487c8cbd0ff1ab4a3e46d12e4368678e8d62975f056200c7fbe6e2f61a19b1`  
		Last Modified: Wed, 11 Jul 2018 09:34:21 GMT  
		Size: 16.3 MB (16283983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d1565b13afbe225eb5e034bf0be386d470cfa98676ae4ffecd7e4b5f92ec8a`  
		Last Modified: Wed, 01 Aug 2018 10:40:20 GMT  
		Size: 10.8 MB (10823364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c524421bee203068f78fa64621e5d89ac80c2031c105dcd5ed3ede41071202`  
		Last Modified: Wed, 01 Aug 2018 10:40:18 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05e30819d7ab53061536120c856c57e2de29a9577347c31dc20dbeebeb12244`  
		Last Modified: Wed, 01 Aug 2018 10:40:18 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ba7de4be1ed39a3e26a6e611fe6201be0319af37b596bc64a18e3723772671`  
		Last Modified: Wed, 01 Aug 2018 10:40:18 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c66700c4a9c4e3487eaeb598eb6fa3fbab2e16a3cb2d49a683919830e01e6f2`  
		Last Modified: Wed, 01 Aug 2018 10:40:18 GMT  
		Size: 4.2 KB (4177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:c2477d53be0d4ea1a694644311d09d43b7956a742a72bf9159d4954cd73683fc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31989482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c93bdfff0a5744d174460d00dbe1c95f6448b7828c84f70862b6df044136153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Jul 2018 15:02:06 GMT
ADD file:ebd40cda2f6087daf4d14e6dc1ee0b4a0fb5dc96c70129be8e07de0e5c628312 in / 
# Fri, 06 Jul 2018 15:02:07 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 06 Jul 2018 15:02:07 GMT
CMD ["/bin/sh"]
# Wed, 11 Jul 2018 10:53:45 GMT
RUN addgroup -S rabbitmq && adduser -S -h /var/lib/rabbitmq -G rabbitmq rabbitmq
# Wed, 11 Jul 2018 10:53:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 11 Jul 2018 10:53:54 GMT
RUN apk add --no-cache 		bash 		procps 		erlang-asn1 		erlang-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang 		erlang-os-mon 		erlang-public-key 		erlang-sasl 		erlang-ssl 		erlang-syntax-tools 		erlang-xmerl
# Wed, 11 Jul 2018 10:53:55 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Wed, 11 Jul 2018 10:53:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Jul 2018 10:53:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jul 2018 10:53:55 GMT
ENV RABBITMQ_GPG_KEY=0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Jul 2018 10:53:55 GMT
ENV RABBITMQ_VERSION=3.7.7
# Wed, 11 Jul 2018 10:53:56 GMT
ENV RABBITMQ_GITHUB_TAG=v3.7.7
# Wed, 01 Aug 2018 11:46:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gnupg 		libressl 		wget 		xz 	; 		wget -O rabbitmq-server.tar.xz.asc "https://github.com/rabbitmq/rabbitmq-server/releases/download/$RABBITMQ_GITHUB_TAG/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz.asc"; 	wget -O rabbitmq-server.tar.xz     "https://github.com/rabbitmq/rabbitmq-server/releases/download/$RABBITMQ_GITHUB_TAG/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$RABBITMQ_GPG_KEY"; 	gpg --batch --verify rabbitmq-server.tar.xz.asc rabbitmq-server.tar.xz; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar 		--extract 		--verbose 		--file rabbitmq-server.tar.xz 		--directory "$RABBITMQ_HOME" 		--strip-components 1 	; 	rm -f rabbitmq-server.tar.xz*; 		grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -ri 's!^(SYS_PREFIX=).*$!\1!g' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 		apk del .build-deps
# Wed, 01 Aug 2018 11:46:12 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 01 Aug 2018 11:46:13 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq
# Wed, 01 Aug 2018 11:46:13 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 01 Aug 2018 11:46:14 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Wed, 01 Aug 2018 11:46:15 GMT
RUN ln -sf "$RABBITMQ_HOME/plugins" /plugins
# Wed, 01 Aug 2018 11:46:15 GMT
COPY file:03f4165e1aefa09a8d97a5e402638f735384652cec9e89f399f563063d59ab58 in /usr/local/bin/ 
# Wed, 01 Aug 2018 11:46:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Aug 2018 11:46:16 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Wed, 01 Aug 2018 11:46:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:ef15772113129a5330876ce10683bbf6509a4c4c99b3a99894dcbc7560975052`  
		Last Modified: Fri, 06 Jul 2018 15:02:46 GMT  
		Size: 2.3 MB (2270920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df692b84cf35e6038d677f9ab7de2a3c671c57671043da1d20d99252e0d9c42`  
		Last Modified: Fri, 06 Jul 2018 15:02:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae68ec2c4b66a1ddd95998f177dbfeb1442c6ce1411916b3801221abd105c6f`  
		Last Modified: Wed, 11 Jul 2018 10:55:47 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48a5fb3e649e78c97521547e4aebccc3781f46cb89541c266f04e2999b43078`  
		Last Modified: Wed, 11 Jul 2018 10:55:47 GMT  
		Size: 9.1 KB (9127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d2158a94acaad710b72d22111260734c66c6215029b2e0b9ffcc8b6bd9565a`  
		Last Modified: Wed, 11 Jul 2018 10:55:50 GMT  
		Size: 18.9 MB (18866924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e744a031c58134ddd277eddcc4eac27b743671568f3808bc025dcafa9b0ce42`  
		Last Modified: Wed, 01 Aug 2018 11:53:00 GMT  
		Size: 10.8 MB (10836419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff96bc76a49e8814bc8f475e744db30939d5632fea72d4c92aa6069da0c944f7`  
		Last Modified: Wed, 01 Aug 2018 11:52:59 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9cb02acfea4eafd98c3055810bbb63f908b69af7c5ee496526cbe39d4c121c`  
		Last Modified: Wed, 01 Aug 2018 11:52:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902e5051db26a81052e8faad02b369d2891c3f5e9fc658ab8c7175fb28891cd4`  
		Last Modified: Wed, 01 Aug 2018 11:52:59 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edda6eb163d592be40e00addd727889135132d7dee173ee707bd2faec74a6567`  
		Last Modified: Wed, 01 Aug 2018 11:52:59 GMT  
		Size: 4.2 KB (4177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:b2fecba2a4466698f92267674d51fef4a6d79a39728c23277f6016c1997d2308
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29523374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70af53d70c91a2eac191b44f7fa72723659d948aba73c79308249d076b3d2871`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Jul 2018 08:18:09 GMT
ADD file:4ff20d593b16518d45b1b1d6efdab141199316dba7a53ce7459249f5de690dfd in / 
# Fri, 06 Jul 2018 08:18:10 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 06 Jul 2018 08:18:11 GMT
CMD ["/bin/sh"]
# Wed, 11 Jul 2018 10:25:59 GMT
RUN addgroup -S rabbitmq && adduser -S -h /var/lib/rabbitmq -G rabbitmq rabbitmq
# Wed, 11 Jul 2018 10:26:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 11 Jul 2018 10:26:18 GMT
RUN apk add --no-cache 		bash 		procps 		erlang-asn1 		erlang-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang 		erlang-os-mon 		erlang-public-key 		erlang-sasl 		erlang-ssl 		erlang-syntax-tools 		erlang-xmerl
# Wed, 11 Jul 2018 10:26:19 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Wed, 11 Jul 2018 10:26:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Jul 2018 10:26:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jul 2018 10:26:21 GMT
ENV RABBITMQ_GPG_KEY=0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Jul 2018 10:26:22 GMT
ENV RABBITMQ_VERSION=3.7.7
# Wed, 11 Jul 2018 10:26:23 GMT
ENV RABBITMQ_GITHUB_TAG=v3.7.7
# Wed, 11 Jul 2018 10:26:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gnupg 		libressl 		wget 		xz 	; 		wget -O rabbitmq-server.tar.xz.asc "https://github.com/rabbitmq/rabbitmq-server/releases/download/$RABBITMQ_GITHUB_TAG/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz.asc"; 	wget -O rabbitmq-server.tar.xz     "https://github.com/rabbitmq/rabbitmq-server/releases/download/$RABBITMQ_GITHUB_TAG/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$RABBITMQ_GPG_KEY"; 	gpg --batch --verify rabbitmq-server.tar.xz.asc rabbitmq-server.tar.xz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar 		--extract 		--verbose 		--file rabbitmq-server.tar.xz 		--directory "$RABBITMQ_HOME" 		--strip-components 1 	; 	rm -f rabbitmq-server.tar.xz*; 		grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -ri 's!^(SYS_PREFIX=).*$!\1!g' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 		apk del .build-deps
# Wed, 11 Jul 2018 10:26:41 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 11 Jul 2018 10:26:43 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq
# Wed, 11 Jul 2018 10:26:50 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 11 Jul 2018 10:26:53 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Wed, 11 Jul 2018 10:27:03 GMT
RUN ln -sf "$RABBITMQ_HOME/plugins" /plugins
# Wed, 11 Jul 2018 10:27:06 GMT
COPY file:03f4165e1aefa09a8d97a5e402638f735384652cec9e89f399f563063d59ab58 in /usr/local/bin/ 
# Wed, 11 Jul 2018 10:27:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Jul 2018 10:27:07 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Wed, 11 Jul 2018 10:27:08 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e642bcb5b1890a07dd2fc8be2bc35edf5e2b651d4993e71caef03b4b43ace970`  
		Last Modified: Fri, 06 Jul 2018 08:18:44 GMT  
		Size: 2.2 MB (2194861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09410b1fce4c4630b3bc57c6ee158ee9821ec415d0acaa1607b9e0bcf76d91`  
		Last Modified: Fri, 06 Jul 2018 08:18:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f021abfdb3c8f50ac16e1860d55daec37d1d07cb9ddf0f8e4e4bf4509c99a5d6`  
		Last Modified: Wed, 11 Jul 2018 10:30:10 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2453f665d51ab7728b0d24b10dc671e8e45ce097be5516dc629fefafd187a428`  
		Last Modified: Wed, 11 Jul 2018 10:30:09 GMT  
		Size: 9.5 KB (9510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3800d611831cf7d9849a4365b299670544c785575502ef9f5ac3ee7ef89ee786`  
		Last Modified: Wed, 11 Jul 2018 10:30:12 GMT  
		Size: 16.5 MB (16484955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21faf245e0dde139e696d709073722cbcb45afff0e7d8902ba7fedf58d7ad52f`  
		Last Modified: Wed, 11 Jul 2018 10:30:09 GMT  
		Size: 10.8 MB (10827884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc74fc0ada1e8f3505935daf5379a23e3c68470a7c8d78aee4f30f818e7d9a2a`  
		Last Modified: Wed, 11 Jul 2018 10:30:06 GMT  
		Size: 253.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdb9d6a7adfa0ecb0d83385a29c7b4ff5e274cc4a36dbab5011113e29862504`  
		Last Modified: Wed, 11 Jul 2018 10:30:06 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcd1d0cff2ff2bb2761a8efd68ffd87a9008b1b4794d260dc909fde7e54262d`  
		Last Modified: Wed, 11 Jul 2018 10:30:06 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f22f7b2d4b59118fc85be17c27100df4a5f3d60de43649311dab03c6fe59ad`  
		Last Modified: Wed, 11 Jul 2018 10:30:06 GMT  
		Size: 4.2 KB (4180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:b3e0dcbc546026e978b93ee32f5eea2326d7d21c3a28dd59306d2cb84b0fc811
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29656940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb73aa3d52cee6d57a2147f69465958172b9344725dae17f637c3121e2a1138d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 06 Jul 2018 11:41:42 GMT
ADD file:376dd7fc34ad39570d2e20f3704305e788ae613c589445b3e8fb880147c3eb59 in / 
# Fri, 06 Jul 2018 11:41:43 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 06 Jul 2018 11:41:43 GMT
CMD ["/bin/sh"]
# Wed, 11 Jul 2018 11:52:52 GMT
RUN addgroup -S rabbitmq && adduser -S -h /var/lib/rabbitmq -G rabbitmq rabbitmq
# Wed, 11 Jul 2018 11:52:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 11 Jul 2018 11:52:55 GMT
RUN apk add --no-cache 		bash 		procps 		erlang-asn1 		erlang-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang 		erlang-os-mon 		erlang-public-key 		erlang-sasl 		erlang-ssl 		erlang-syntax-tools 		erlang-xmerl
# Wed, 11 Jul 2018 11:52:55 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Wed, 11 Jul 2018 11:52:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 11 Jul 2018 11:52:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jul 2018 11:52:55 GMT
ENV RABBITMQ_GPG_KEY=0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 11 Jul 2018 11:52:56 GMT
ENV RABBITMQ_VERSION=3.7.7
# Wed, 11 Jul 2018 11:52:56 GMT
ENV RABBITMQ_GITHUB_TAG=v3.7.7
# Wed, 01 Aug 2018 12:13:23 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gnupg 		libressl 		wget 		xz 	; 		wget -O rabbitmq-server.tar.xz.asc "https://github.com/rabbitmq/rabbitmq-server/releases/download/$RABBITMQ_GITHUB_TAG/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz.asc"; 	wget -O rabbitmq-server.tar.xz     "https://github.com/rabbitmq/rabbitmq-server/releases/download/$RABBITMQ_GITHUB_TAG/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$RABBITMQ_GPG_KEY"; 	gpg --batch --verify rabbitmq-server.tar.xz.asc rabbitmq-server.tar.xz; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar 		--extract 		--verbose 		--file rabbitmq-server.tar.xz 		--directory "$RABBITMQ_HOME" 		--strip-components 1 	; 	rm -f rabbitmq-server.tar.xz*; 		grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -ri 's!^(SYS_PREFIX=).*$!\1!g' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 		apk del .build-deps
# Wed, 01 Aug 2018 12:13:23 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 01 Aug 2018 12:13:24 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq /var/log/rabbitmq
# Wed, 01 Aug 2018 12:13:24 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 01 Aug 2018 12:13:25 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Wed, 01 Aug 2018 12:13:25 GMT
RUN ln -sf "$RABBITMQ_HOME/plugins" /plugins
# Wed, 01 Aug 2018 12:13:25 GMT
COPY file:03f4165e1aefa09a8d97a5e402638f735384652cec9e89f399f563063d59ab58 in /usr/local/bin/ 
# Wed, 01 Aug 2018 12:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Aug 2018 12:13:26 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Wed, 01 Aug 2018 12:13:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cdf21ace94188d512903eea53ea8559677e0e6ffd5d6a180a1d88c118abc96fc`  
		Last Modified: Fri, 06 Jul 2018 11:42:01 GMT  
		Size: 2.3 MB (2307471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea178433f2f09080fbbf77f09da1b16d588b7ced380d495a2f2ad00d28468338`  
		Last Modified: Fri, 06 Jul 2018 11:42:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9740b6c9196071c7dceba27788d6b59e1f399f52aad064f330c173ecfa251a66`  
		Last Modified: Wed, 11 Jul 2018 11:54:03 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee41179588205bf61b0b48a7907be29fc6fc69f043dd4f6b5524e611717e362`  
		Last Modified: Wed, 11 Jul 2018 11:54:03 GMT  
		Size: 9.2 KB (9235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2309c2ed29930b8f07f3a0c22158aff74c27869f8d753ebba9a1ae1f4df4221`  
		Last Modified: Wed, 11 Jul 2018 11:54:05 GMT  
		Size: 16.5 MB (16545572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ea45009f6446a3f31fbbb22580828e336f86944c805b2bf7c47a017892905e`  
		Last Modified: Wed, 01 Aug 2018 12:17:19 GMT  
		Size: 10.8 MB (10788579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc25baf3b7e9464d77347affcc1d0acb704a0a94b83aad71727c9b69ae715060`  
		Last Modified: Wed, 01 Aug 2018 12:17:18 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc525b9fd9b1f03c3e8a3704fd0dea46294552d49169324b2a64832783bc9ea`  
		Last Modified: Wed, 01 Aug 2018 12:17:18 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87930e1e051256cfc4b17254495cefdca42fec70cf882b7e2bb6d65be2c8c448`  
		Last Modified: Wed, 01 Aug 2018 12:17:18 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04a72e30d2636061eb99b459795c75f97dc38c03d14c28743596c68750c50f1`  
		Last Modified: Wed, 01 Aug 2018 12:17:18 GMT  
		Size: 4.2 KB (4179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
