## `openjdk:10-windowsservercore-1709`

```console
$ docker pull openjdk@sha256:a48921f3f5c7c3ad6c9d6e11af6fc2b3d211ca1d72c72731ae8cbbe9a01f4438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.16299.547; amd64

### `openjdk:10-windowsservercore-1709` - windows version 10.0.16299.547; amd64

```console
$ docker pull openjdk@sha256:761583bcd84ea4d1c15c6efb66741815dc997ce462f9c4a6881a2183c4b9b358
```

-	Docker Version: 17.06.2-ee-13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3389156455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132e9dbeee8d04dc45a494ac556109646d1d155739f44e6cbcba9f1a1bc621f5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 29 Sep 2017 14:43:28 GMT
RUN Apply image 10.0.16299.15
# Mon, 02 Jul 2018 18:10:50 GMT
RUN Install update 10.0.16299.547
# Wed, 11 Jul 2018 09:41:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Jul 2018 09:41:03 GMT
ENV JAVA_HOME=C:\ojdkbuild
# Wed, 11 Jul 2018 09:42:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath;
# Sat, 28 Jul 2018 09:36:40 GMT
ENV JAVA_VERSION=10.0.2
# Sat, 28 Jul 2018 09:36:41 GMT
ENV JAVA_OJDKBUILD_VERSION=10.0.2-1
# Sat, 28 Jul 2018 09:36:42 GMT
ENV JAVA_OJDKBUILD_ZIP=java-10-openjdk-10.0.2-1.b13.ojdkbuild.windows.x86_64.zip
# Sat, 28 Jul 2018 09:36:43 GMT
ENV JAVA_OJDKBUILD_SHA256=39801db76f04b9f1491b0d0a64258535f14e319a3cd08d3e161b18a6af7a842d
# Sat, 28 Jul 2018 09:39:32 GMT
RUN $url = ('https://github.com/ojdkbuild/ojdkbuild/releases/download/{0}/{1}' -f $env:JAVA_OJDKBUILD_VERSION, $env:JAVA_OJDKBUILD_ZIP); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'ojdkbuild.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_OJDKBUILD_SHA256); 	if ((Get-FileHash ojdkbuild.zip -Algorithm sha256).Hash -ne $env:JAVA_OJDKBUILD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive ojdkbuild.zip -DestinationPath C:\; 		Write-Host 'Renaming ...'; 	Move-Item 		-Path ('C:\{0}' -f ($env:JAVA_OJDKBUILD_ZIP -Replace '.zip$', '')) 		-Destination $env:JAVA_HOME 	; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 	Write-Host '  javac -version'; javac -version; 		Write-Host 'Removing ...'; 	Remove-Item ojdkbuild.zip -Force; 		Write-Host 'Complete.';
# Sat, 28 Jul 2018 09:39:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5847a47b8593f7c39aa5e3db09e50b76d42aa8898c0440c70cc9c69747d4c479`  
		Last Modified: Tue, 17 Oct 2017 15:51:05 GMT  
		Size: 2.3 GB (2274300585 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a01c2a39b5bdf158508b424626efbcede4aa9da21f2d4f6ffbd5bff4deb0fb01`  
		Last Modified: Tue, 10 Jul 2018 23:36:17 GMT  
		Size: 831.1 MB (831119569 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5c935a79e71d79bf144e02b94352e10d483d43e5c3f4a3491874c5d6d72deda3`  
		Last Modified: Wed, 11 Jul 2018 09:55:02 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9870e044256cc823af3ec08f6614064337e131de31190bd064a24f8f36eac8`  
		Last Modified: Wed, 11 Jul 2018 09:55:00 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11eff0de8d29d6adc1d8e38a13440933cc7dee6ba24035353c0a39ea4a6a1f2`  
		Last Modified: Wed, 11 Jul 2018 09:55:01 GMT  
		Size: 4.7 MB (4721452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4649807c342b094159119fc266b6f15ed46ef655d882d9bb2cd451ab4724b3`  
		Last Modified: Sat, 28 Jul 2018 09:50:49 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b1b9cb78adee1373b0ca5c2dabd5f6be30ab1349f3caba3328a093db29198d`  
		Last Modified: Sat, 28 Jul 2018 09:50:47 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c206f67e740192f4f427f7eeffdf6854ac55eb6eed7047b8b48d7269044c655`  
		Last Modified: Sat, 28 Jul 2018 09:50:47 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ecf2b72da13aaf86d209acab18400b196234a446acb0c0292f637b23044a41`  
		Last Modified: Sat, 28 Jul 2018 09:50:47 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e41e181f16b57545083e64f14688f7714e0329596d3cf7163f533019fe08fb`  
		Last Modified: Sat, 28 Jul 2018 09:51:22 GMT  
		Size: 279.0 MB (279006481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb4ed0b0b7c265347044fe9048618194c495ba7ad2711fa2b378511c799a0a2`  
		Last Modified: Sat, 28 Jul 2018 09:50:47 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
