## `mongo:unstable-windowsservercore-1803`

```console
$ docker pull mongo@sha256:35b2c762a6b1d57412e33a17deb0907aa27ec4cf0b8a20970eac9e1d99e4e988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.165; amd64

### `mongo:unstable-windowsservercore-1803` - windows version 10.0.17134.165; amd64

```console
$ docker pull mongo@sha256:752370b41b3f2aa7a00c3a182020f936eda1623425caf6a0830e9fcea137f17f
```

-	Docker Version: 17.06.2-ee-13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2683457150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92472d373c617255fa0920fc222842af0246ecf01954c9ef1df89106b2983ab2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 10.0.17134.1
# Sat, 07 Jul 2018 22:48:41 GMT
RUN Install update 10.0.17134.165
# Tue, 17 Jul 2018 20:48:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Jul 2018 20:48:01 GMT
ENV MONGO_VERSION=4.1.1
# Tue, 17 Jul 2018 20:48:02 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.1.1-signed.msi
# Tue, 17 Jul 2018 20:48:03 GMT
ENV MONGO_DOWNLOAD_SHA256=ff14a5e670543a966500d562195dcdd9738b3dd76cb0122b4b3648215e6cf47d
# Tue, 17 Jul 2018 21:02:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 17 Jul 2018 21:02:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 17 Jul 2018 21:02:48 GMT
EXPOSE 27017/tcp
# Tue, 17 Jul 2018 21:02:49 GMT
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
	-	`sha256:225f5baa4bea3646d6eb92581981516f830ce95ed09dd27b404f9d06076a742e`  
		Last Modified: Sat, 21 Jul 2018 10:00:13 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22330611b43dd8c7d64953fb0ef4ce8d4c612d0d18a7f0e5ccfed4e02cfd4c73`  
		Last Modified: Sat, 21 Jul 2018 10:00:13 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0e0e9d1547ee53f65c41888a0ba896c9771a95866bfb9437ea85087f144cc`  
		Last Modified: Sat, 21 Jul 2018 10:00:10 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cb21a7cd20bcf7acb906264e448c9ff3b7abb4a031f34b8015dbb1ddd8d594`  
		Last Modified: Sat, 21 Jul 2018 10:01:08 GMT  
		Size: 530.2 MB (530239288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f141d03c57f485de0d016024f3ab1855ba51835c5811d4487353c2a5a127f5be`  
		Last Modified: Sat, 21 Jul 2018 10:00:11 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7fe94ab99e315642a5f16ab83c1489bb0125ac4fcb47224de17683f0f7a771`  
		Last Modified: Sat, 21 Jul 2018 10:00:10 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0806f892642c07ecaef8c0cc7af5eec5cd5a5a9ad6fd6bf006784a86c15eaa1e`  
		Last Modified: Sat, 21 Jul 2018 10:00:10 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
