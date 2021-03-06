## `openjdk:10-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:b9acceb02afd7214483f96c7708b522d7073a100da772793620bc9b87c2616ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2363; amd64

### `openjdk:10-windowsservercore-ltsc2016` - windows version 10.0.14393.2363; amd64

```console
$ docker pull openjdk@sha256:2fc363390738ea3fdfa02609943670557fcc918fbf7b47f775354cdf663c8e7e
```

-	Docker Version: 17.06.2-ee-13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5778164357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af66eeb209f04eaa6b987e80cee0dc6370c8ee12f8442e8adcfe89df05ffda5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Tue, 10 Jul 2018 21:16:33 GMT
RUN Install update 10.0.14393.2363
# Wed, 11 Jul 2018 09:36:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Jul 2018 09:36:35 GMT
ENV JAVA_HOME=C:\ojdkbuild
# Wed, 11 Jul 2018 09:37:59 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath;
# Sat, 28 Jul 2018 09:33:11 GMT
ENV JAVA_VERSION=10.0.2
# Sat, 28 Jul 2018 09:33:12 GMT
ENV JAVA_OJDKBUILD_VERSION=10.0.2-1
# Sat, 28 Jul 2018 09:33:13 GMT
ENV JAVA_OJDKBUILD_ZIP=java-10-openjdk-10.0.2-1.b13.ojdkbuild.windows.x86_64.zip
# Sat, 28 Jul 2018 09:33:14 GMT
ENV JAVA_OJDKBUILD_SHA256=39801db76f04b9f1491b0d0a64258535f14e319a3cd08d3e161b18a6af7a842d
# Sat, 28 Jul 2018 09:36:30 GMT
RUN $url = ('https://github.com/ojdkbuild/ojdkbuild/releases/download/{0}/{1}' -f $env:JAVA_OJDKBUILD_VERSION, $env:JAVA_OJDKBUILD_ZIP); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'ojdkbuild.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_OJDKBUILD_SHA256); 	if ((Get-FileHash ojdkbuild.zip -Algorithm sha256).Hash -ne $env:JAVA_OJDKBUILD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive ojdkbuild.zip -DestinationPath C:\; 		Write-Host 'Renaming ...'; 	Move-Item 		-Path ('C:\{0}' -f ($env:JAVA_OJDKBUILD_ZIP -Replace '.zip$', '')) 		-Destination $env:JAVA_HOME 	; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 	Write-Host '  javac -version'; javac -version; 		Write-Host 'Removing ...'; 	Remove-Item ojdkbuild.zip -Force; 		Write-Host 'Complete.';
# Sat, 28 Jul 2018 09:36:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 13 Dec 2016 10:53:31 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fb1ebf2c42b6ac63b874d36a405b413fdf6c314131c3605d77e3cee6f485881f`  
		Last Modified: Tue, 10 Jul 2018 21:16:33 GMT  
		Size: 1.4 GB (1419298293 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b678e902d6e9a27ab4d61bef7b26997ea26fdec2575d1317c9eab3b31c61fd9b`  
		Last Modified: Wed, 11 Jul 2018 09:53:57 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df0b7da96ba2f6f9998af410e0e83095c74f65e14e44e196fa7ca34b34b20e7`  
		Last Modified: Wed, 11 Jul 2018 09:53:56 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43557e5ace1974f8b220d16ea7c7a0b225327d94c023252ebc95b6847a042201`  
		Last Modified: Wed, 11 Jul 2018 09:53:58 GMT  
		Size: 5.0 MB (5041524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e0e4852cb098ec12c53c7c9b032c7465d9dba1bfbd1fe0cb2e29934cc6c33`  
		Last Modified: Sat, 28 Jul 2018 09:49:38 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36e7dabd9d89bf8bd66b6340da3c7e41f2ac2c34da94eb0fd161c022f7a156d`  
		Last Modified: Sat, 28 Jul 2018 09:49:36 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654a087e403ae69032a73ee9b424a43c096487252802c89869c74544097eee78`  
		Last Modified: Sat, 28 Jul 2018 09:49:36 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c315d8c5722f6bab21c423b8711af936fe0a59310da1e6a832aaea25704d24bf`  
		Last Modified: Sat, 28 Jul 2018 09:49:36 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253b9f79508a827a81cf51d9701a609165d64a07dd5b4cf565edfdb4f5621a61`  
		Last Modified: Sat, 28 Jul 2018 09:50:13 GMT  
		Size: 283.8 MB (283830256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21229005efcab2b1b886a89c586f21334f74ce2e1ea3c0eb4b586e035e4ddbf4`  
		Last Modified: Sat, 28 Jul 2018 09:49:36 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
