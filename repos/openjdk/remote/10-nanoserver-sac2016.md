## `openjdk:10-nanoserver-sac2016`

```console
$ docker pull openjdk@sha256:f940eef9915b052e2b94cc7e9170f72f0d7c4b36cb56e5c240bb45bfa1ef2cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2363; amd64

### `openjdk:10-nanoserver-sac2016` - windows version 10.0.14393.2363; amd64

```console
$ docker pull openjdk@sha256:786fa7e74599ef091ae41e78e49cc21f0c50a3445ac6510a126d5b9f2fcaaec2
```

-	Docker Version: 17.06.2-ee-13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.5 MB (699469434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2190540dd38007d9eeb129cf51462c156686a91c68b00843fd570f34c1c482ca`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:47:17 GMT
RUN Apply image 10.0.14393.0
# Tue, 10 Jul 2018 21:16:01 GMT
RUN Install update 10.0.14393.2363
# Wed, 11 Jul 2018 09:44:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Jul 2018 09:45:40 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Jul 2018 09:45:41 GMT
ENV JAVA_HOME=C:\ojdkbuild
# Wed, 11 Jul 2018 09:46:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath;
# Sat, 28 Jul 2018 09:39:52 GMT
ENV JAVA_VERSION=10.0.2
# Sat, 28 Jul 2018 09:39:53 GMT
ENV JAVA_OJDKBUILD_VERSION=10.0.2-1
# Sat, 28 Jul 2018 09:39:54 GMT
ENV JAVA_OJDKBUILD_ZIP=java-10-openjdk-10.0.2-1.b13.ojdkbuild.windows.x86_64.zip
# Sat, 28 Jul 2018 09:39:55 GMT
ENV JAVA_OJDKBUILD_SHA256=39801db76f04b9f1491b0d0a64258535f14e319a3cd08d3e161b18a6af7a842d
# Sat, 28 Jul 2018 09:42:31 GMT
RUN $url = ('https://github.com/ojdkbuild/ojdkbuild/releases/download/{0}/{1}' -f $env:JAVA_OJDKBUILD_VERSION, $env:JAVA_OJDKBUILD_ZIP); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'ojdkbuild.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_OJDKBUILD_SHA256); 	if ((Get-FileHash ojdkbuild.zip -Algorithm sha256).Hash -ne $env:JAVA_OJDKBUILD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive ojdkbuild.zip -DestinationPath C:\; 		Write-Host 'Renaming ...'; 	Move-Item 		-Path ('C:\{0}' -f ($env:JAVA_OJDKBUILD_ZIP -Replace '.zip$', '')) 		-Destination $env:JAVA_HOME 	; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 	Write-Host '  javac -version'; javac -version; 		Write-Host 'Removing ...'; 	Remove-Item ojdkbuild.zip -Force; 		Write-Host 'Complete.';
# Sat, 28 Jul 2018 09:42:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bce2fbc256ea437a87dadac2f69aabd25bed4f56255549090056c1131fad0277`  
		Last Modified: Tue, 13 Dec 2016 10:47:17 GMT  
		Size: 252.7 MB (252691002 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d4a9b16fd154d065649f42ee7ac674690d46dbe6ad2398a58166c37c85ca64ed`  
		Last Modified: Tue, 10 Jul 2018 21:16:01 GMT  
		Size: 166.8 MB (166830055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c00083f7064e157d9aa12ed2cde81fc21da017ab3b1d2d05cf45ee282d465ddd`  
		Last Modified: Wed, 11 Jul 2018 09:56:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d7a6645036c8c0f4a1d6d442c92a0d6214d2cb7d46da2abc9bcd951455fa57`  
		Last Modified: Wed, 11 Jul 2018 09:56:06 GMT  
		Size: 930.8 KB (930778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd0ad8d0a8d35c51bbd7a4f1ac2990362b3b6d022d308e7612624b35b34470c`  
		Last Modified: Wed, 11 Jul 2018 09:56:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcae2d73248ed8cb8b131362bdf56cf33e83e1a65bcc40aa7a11c8c87a8452b`  
		Last Modified: Wed, 11 Jul 2018 09:56:06 GMT  
		Size: 846.2 KB (846242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc1381f0b0067d8e26363533d7ce8992aefc172edf1bfec7c7a40162357135d`  
		Last Modified: Sat, 28 Jul 2018 09:51:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34305378074e384d3eeefdaed73baef6174544d010538bc94fc10fa90cf228cd`  
		Last Modified: Sat, 28 Jul 2018 09:51:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd88672ee31c5094d83c4e5789a1eeb4fccc7c7ca64c63a52360a4c9c0f5b10`  
		Last Modified: Sat, 28 Jul 2018 09:51:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe03cb1e8de1e114bed5f77ae954876422bc9b3002e8ced350d5c021c9de32`  
		Last Modified: Sat, 28 Jul 2018 09:52:00 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49aedf97d18a8e1856db87158cd63399ae31eaaf4807b55c47f4516d90482fe`  
		Last Modified: Sat, 28 Jul 2018 09:52:31 GMT  
		Size: 278.2 MB (278164701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b606a4731a27ac5298c252eafd3c9b1910a034c61a04bff58bae06d3bc74fd85`  
		Last Modified: Sat, 28 Jul 2018 09:51:57 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
