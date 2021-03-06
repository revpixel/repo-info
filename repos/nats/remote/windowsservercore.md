## `nats:windowsservercore`

```console
$ docker pull nats@sha256:2cc4bdf4deaa6b2f301ba639fa33bd793e929ed21994e7757b480ed6812aac3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2312; amd64

### `nats:windowsservercore` - windows version 10.0.14393.2312; amd64

```console
$ docker pull nats@sha256:ef9ea4edcdfacd691c955d14ca84d001aded324bd0ba300ed024e457f3dfe90b
```

-	Docker Version: 17.06.2-ee-13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 GB (5486870872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01479ffcda681037cb4ad315783dcd76f59456e41d569b1543ed57d991aad44`
-	Entrypoint: `["gnatsd"]`
-	Default Command: `["-c","gnatsd.conf"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Wed, 13 Jun 2018 00:36:30 GMT
RUN Install update 10.0.14393.2312
# Wed, 04 Jul 2018 09:46:11 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 06 Jul 2018 09:41:31 GMT
RUN cmd /S /C #(nop) WORKDIR C:\gnatsd
# Fri, 06 Jul 2018 09:41:33 GMT
RUN cmd /S /C #(nop) COPY file:6ed5bb76c8a5f2c4b0c291249c9295e7a5f5e0688654335aa44e0b36cc55227a in gnatsd.exe 
# Fri, 06 Jul 2018 09:41:34 GMT
RUN cmd /S /C #(nop) COPY file:8fad70d15db71db30b9945fba2b3d29035a631ee4fe410e797aef6981c2a1879 in gnatsd.conf 
# Fri, 06 Jul 2018 09:41:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222/tcp 6222/tcp 8222/tcp
# Fri, 06 Jul 2018 09:41:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["gnatsd"]
# Fri, 06 Jul 2018 09:41:37 GMT
RUN cmd /S /C #(nop)  CMD ["-c" "gnatsd.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 13 Dec 2016 10:53:31 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8e9da9bbe3af2118a0b5eef7a3d649367557d0d3992ed0213c79857b23b4140e`  
		Last Modified: Wed, 13 Jun 2018 00:36:30 GMT  
		Size: 1.4 GB (1414319443 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3b7e3c3262d1eec41ddb2082c87ab48069452f2426f7f24241d54787f9e0c9d`  
		Last Modified: Wed, 04 Jul 2018 09:46:36 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27792fc09fda2b68ac5c731dc3319876cf9b58d1f97243a23ce64bdbbbe048e`  
		Last Modified: Fri, 06 Jul 2018 09:42:08 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ac32b609be49cf0ece0811085b446e325c8cf728149fec03d8c53c0979e15`  
		Last Modified: Fri, 06 Jul 2018 09:42:06 GMT  
		Size: 2.6 MB (2557517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ea51234e4672f79de29ce60f90e58ca16aa299a64d46ed42f98be13c7ddaa6`  
		Last Modified: Fri, 06 Jul 2018 09:42:06 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3fd11f2797c537e085cbd4fae7e6b27624a3f4b1803a8aced7638a614cc53`  
		Last Modified: Fri, 06 Jul 2018 09:42:06 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491a4d11a6632d898dd83a5d698aa2c57815d343c3df2e66cd2aad96c7a9df62`  
		Last Modified: Fri, 06 Jul 2018 09:42:06 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24392c6e1ed7b7232e100fefe82710c8431feddb3b5d3e2f529ac76492dd1ce8`  
		Last Modified: Fri, 06 Jul 2018 09:42:06 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
