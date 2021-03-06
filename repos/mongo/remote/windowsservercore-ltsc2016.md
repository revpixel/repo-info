## `mongo:windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:d05e9d74a53caf1710dc075ec9b6b146326c4e49e4c4c1f45c4a454cfa9f948b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2363; amd64

### `mongo:windowsservercore-ltsc2016` - windows version 10.0.14393.2363; amd64

```console
$ docker pull mongo@sha256:6b3684c7ae5b418966790362872149c788e55b8ec91edac6cd844fe56bb083a2
```

-	Docker Version: 17.06.2-ee-13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 GB (5553704870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff4f2608846eb180e0e3afc4b0bd07ef949978498851ab793f22aab0c62f95`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Tue, 10 Jul 2018 21:16:33 GMT
RUN Install update 10.0.14393.2363
# Tue, 17 Jul 2018 09:16:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 19 Jul 2018 16:08:00 GMT
ENV MONGO_VERSION=4.0.0
# Thu, 19 Jul 2018 16:08:01 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.0-signed.msi
# Thu, 19 Jul 2018 16:08:02 GMT
ENV MONGO_DOWNLOAD_SHA256=bf370d32e956eb5849cf92f3d092739a930531378091ea8f9237bd902368ae69
# Thu, 19 Jul 2018 16:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 19 Jul 2018 16:17:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 19 Jul 2018 16:17:18 GMT
EXPOSE 27017/tcp
# Thu, 19 Jul 2018 16:17:21 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:331fd417053dd4f3ba6c8293909f00c1104bf81840c35fa27cf2047a7c124804`  
		Last Modified: Tue, 17 Jul 2018 09:47:17 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fb50e6bb98a5800f7cf962d75ccbbd197bcf25919d9f21fe6e3f4f3f0c8f37`  
		Last Modified: Sat, 21 Jul 2018 09:54:21 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868590eb12c9f4e610329b31ed775eec3ca23ddd8632e19b890e51d0fdf4bc0d`  
		Last Modified: Sat, 21 Jul 2018 09:54:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9e7f8a9b48bb35a6d8cea81f3576471d11af5c6ad490d945d869df052c6272`  
		Last Modified: Sat, 21 Jul 2018 09:54:19 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c1f52fba0beeb7256de70778915a25e3c61a65cec8738fb8c0565b13ce7b`  
		Last Modified: Sat, 21 Jul 2018 09:54:33 GMT  
		Size: 64.4 MB (64412347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57fca283fb5d3bce683e6af5714366871e31ac7428f7e05a13eb5862f4c730`  
		Last Modified: Sat, 21 Jul 2018 09:54:18 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d1dad23dac2fc2934bf7334f47012e715ea7c7127177a63964f4c629ebd335`  
		Last Modified: Sat, 21 Jul 2018 09:54:18 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55aa2e77f0b9f13f665f8bb116084dcc9830b2decf18fd26ff971820f072c95`  
		Last Modified: Sat, 21 Jul 2018 09:54:18 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
