## `nats:nanoserver`

```console
$ docker pull nats@sha256:b9b6f112e5c8e70d18bc5bd3e5a7d8a0ea5d4cf18a4b8a761d3414291a57fcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2312; amd64

### `nats:nanoserver` - windows version 10.0.14393.2312; amd64

```console
$ docker pull nats@sha256:0e03a92e8257155eb878b6fada4b11c9049d0aec79167493ab78a442b6cfad64
```

-	Docker Version: 17.06.2-ee-13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (421004165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004f5bc5214f8713d8fba2f0b8e8b9b52210012eead418c17a6505d23363b9a3`
-	Entrypoint: `["gnatsd"]`
-	Default Command: `["-c","gnatsd.conf"]`

```dockerfile
# Tue, 13 Dec 2016 10:47:17 GMT
RUN Apply image 10.0.14393.0
# Wed, 13 Jun 2018 00:36:03 GMT
RUN Install update 10.0.14393.2312
# Wed, 04 Jul 2018 09:46:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 06 Jul 2018 09:41:17 GMT
RUN cmd /S /C #(nop) WORKDIR C:\gnatsd
# Fri, 06 Jul 2018 09:41:19 GMT
RUN cmd /S /C #(nop) COPY file:6ed5bb76c8a5f2c4b0c291249c9295e7a5f5e0688654335aa44e0b36cc55227a in gnatsd.exe 
# Fri, 06 Jul 2018 09:41:21 GMT
RUN cmd /S /C #(nop) COPY file:8fad70d15db71db30b9945fba2b3d29035a631ee4fe410e797aef6981c2a1879 in gnatsd.conf 
# Fri, 06 Jul 2018 09:41:21 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222/tcp 6222/tcp 8222/tcp
# Fri, 06 Jul 2018 09:41:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["gnatsd"]
# Fri, 06 Jul 2018 09:41:26 GMT
RUN cmd /S /C #(nop)  CMD ["-c" "gnatsd.conf"]
```

-	Layers:
	-	`sha256:bce2fbc256ea437a87dadac2f69aabd25bed4f56255549090056c1131fad0277`  
		Last Modified: Tue, 13 Dec 2016 10:47:17 GMT  
		Size: 252.7 MB (252691002 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e7a598ed389ee13dc16cb56bd512d2eecc9597d79797803ef538a02b1e12351f`  
		Last Modified: Wed, 13 Jun 2018 00:36:03 GMT  
		Size: 165.7 MB (165749131 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a9b8eb83c4be00aa333cea97cdf6ceaf95035481bde902ce5e8f1490185df8ac`  
		Last Modified: Wed, 04 Jul 2018 09:46:26 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff745c8ded4f28bd94acebfca95d79b7ebda60d227df9f25287f143ae3074b38`  
		Last Modified: Fri, 06 Jul 2018 09:41:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f46c5f116d0ba090b824d08fbe1932dbc9cf6368b07d5707c8c3f53b11f251`  
		Last Modified: Fri, 06 Jul 2018 09:41:50 GMT  
		Size: 2.6 MB (2557368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5e645f7f069a02c3af0ea7fd9a0d3136e2476a6738c2a2bbc5a3e8ab9c6870`  
		Last Modified: Fri, 06 Jul 2018 09:41:49 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b5ac2d242bae56cf5a5b5eb461bb9c636e4a5050b9475ebd4e5a7862786564`  
		Last Modified: Fri, 06 Jul 2018 09:41:49 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77792766f137e837e95f2c7ba3bf8d5504b9200f2280e4ead05a9fc017aa59`  
		Last Modified: Fri, 06 Jul 2018 09:41:49 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc91f57abfa02b7ccf6c1f7046021e8f69f4f834366406400c12fe7c4701858`  
		Last Modified: Fri, 06 Jul 2018 09:41:49 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
