## `mongo:windowsservercore-1803`

```console
$ docker pull mongo@sha256:737ff529ed2de5c28f9f5a8ab9729ed72c18be81db5805bfb2efcbfb0e8404d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.165; amd64

### `mongo:windowsservercore-1803` - windows version 10.0.17134.165; amd64

```console
$ docker pull mongo@sha256:fe66b5d49b8177f14775cd1c5a43f09f3802526feee7b74ddf55eabe553e6dd6
```

-	Docker Version: 17.06.2-ee-13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2683666366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f256d9e293d92e7e86fb6a560fd82b0ba5dd338fd81e115731ef98f6fb7bf8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 10.0.17134.1
# Sat, 07 Jul 2018 22:48:41 GMT
RUN Install update 10.0.17134.165
# Tue, 17 Jul 2018 20:48:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 19 Jul 2018 15:50:07 GMT
ENV MONGO_VERSION=4.0.0
# Thu, 19 Jul 2018 15:50:08 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.0-signed.msi
# Thu, 19 Jul 2018 15:50:09 GMT
ENV MONGO_DOWNLOAD_SHA256=bf370d32e956eb5849cf92f3d092739a930531378091ea8f9237bd902368ae69
# Thu, 19 Jul 2018 16:07:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 19 Jul 2018 16:07:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 19 Jul 2018 16:07:55 GMT
EXPOSE 27017/tcp
# Thu, 19 Jul 2018 16:07:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Mon, 07 May 2018 21:18:35 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e30fefc566f71c5dd5786e4783ff4ae3ad98804d5279c14dcf806c813fdf8f66`  
		Last Modified: Tue, 10 Jul 2018 21:54:14 GMT  
		Size: 493.5 MB (493521205 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:24d7aea33bc8c516e9df1805b8a1a30efaf719325f3117e896a5f2eb3972e54a`  
		Last Modified: Sat, 21 Jul 2018 09:56:49 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13c4a01802b5ced5aee8776795d940bf23a1180df0069b0829f3df9c75636cf`  
		Last Modified: Sat, 21 Jul 2018 09:56:47 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00c50727a978dec62bfa165314f78388127a03c7eb2c6c4bd3648e4a3ea0673`  
		Last Modified: Sat, 21 Jul 2018 09:56:46 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665ad3a1d60167cc812aff1f2315b7080007d5ec7a73d4457830d13155dcfce3`  
		Last Modified: Sat, 21 Jul 2018 09:56:44 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653c8ca5b6c72a72357d80f64e5aa86d716756f9c6e38c519a4c4a1368183f8f`  
		Last Modified: Sat, 21 Jul 2018 09:57:41 GMT  
		Size: 530.4 MB (530448518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c6bfbdb796413bbf8f85d2bfd0dc191585370add91f587d7bd644681988f7d`  
		Last Modified: Sat, 21 Jul 2018 09:56:44 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937489ca712e634a876233084d40fdeafa37b1985280242c025eb07f39cfea5d`  
		Last Modified: Sat, 21 Jul 2018 09:56:44 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f776d762f8be89ac94007fa1f13c1c64835cb3dc8d5d80c5e314a463eeffae1`  
		Last Modified: Sat, 21 Jul 2018 09:56:44 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
