## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:6547b1177a4cc532aa6013001075089819eea30fb847f3ba945ff5da7be6c929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2363; amd64
	-	windows version 10.0.16299.547; amd64

### `mongo:3-windowsservercore` - windows version 10.0.14393.2363; amd64

```console
$ docker pull mongo@sha256:43a4aff85d89ee56132019469519d5536a13e4400b7d960c3881b6d28ea97e24
```

-	Docker Version: 17.06.2-ee-13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6027581671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee281c593599710bc0286f3d62e731d587a3346ef7787b7fa22160a03cf14542`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Tue, 10 Jul 2018 21:16:33 GMT
RUN Install update 10.0.14393.2363
# Tue, 17 Jul 2018 09:16:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 19 Jul 2018 15:15:12 GMT
ENV MONGO_VERSION=3.6.6
# Thu, 19 Jul 2018 15:15:13 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.6-signed.msi
# Thu, 19 Jul 2018 15:15:14 GMT
ENV MONGO_DOWNLOAD_SHA256=584bc98ce5755f419b7182c3abf1c632a4365e28577a4f498be2c291beeae7c2
# Thu, 19 Jul 2018 15:31:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 19 Jul 2018 15:31:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 19 Jul 2018 15:31:46 GMT
EXPOSE 27017/tcp
# Thu, 19 Jul 2018 15:31:48 GMT
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
	-	`sha256:f1f7c506c655758bc3c1229711675a929a1eef5253376c4dfd93a5902df5a985`  
		Last Modified: Sat, 21 Jul 2018 09:51:08 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8dfe512fb731ed8d79c03b93aa29a6f36f041508115e8d0a6edf607d2ee7e6`  
		Last Modified: Sat, 21 Jul 2018 09:51:07 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ede4d15341e7f7193b1b409d11ae75c74c1ad14b8a34064df243c833b720b1`  
		Last Modified: Sat, 21 Jul 2018 09:51:05 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49e6c1c55fd3c2a0c8c0b85bf23cf772c5671c7e9734177a2affbb66e01722`  
		Last Modified: Sat, 21 Jul 2018 09:52:02 GMT  
		Size: 538.3 MB (538289101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac80d277b3bd9ece884f44f372da8024d260580d26fcb564db79d2739d49dea`  
		Last Modified: Sat, 21 Jul 2018 09:51:07 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a189f1c72a2e51490afcd09d56cf06c1d7f83004a6258192979fc5b57bc93359`  
		Last Modified: Sat, 21 Jul 2018 09:51:05 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b941d73f5d206d0a38bff164943b157168c0e2ce23b89085f4ce3ad317f2ae8c`  
		Last Modified: Sat, 21 Jul 2018 09:51:05 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3-windowsservercore` - windows version 10.0.16299.547; amd64

```console
$ docker pull mongo@sha256:98b516a95b8fb75e7a14b7df1b4f5f556e35f36dafed50949f73479e86999f40
```

-	Docker Version: 17.06.2-ee-13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3643445971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a3f084626f5b0bcd887869909e6812a58fad19e1fe1930584da34fd28de36a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 29 Sep 2017 14:43:28 GMT
RUN Apply image 10.0.16299.15
# Mon, 02 Jul 2018 18:10:50 GMT
RUN Install update 10.0.16299.547
# Thu, 19 Jul 2018 14:48:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 19 Jul 2018 14:57:48 GMT
ENV MONGO_VERSION=3.6.6
# Thu, 19 Jul 2018 14:57:48 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.6-signed.msi
# Thu, 19 Jul 2018 14:57:49 GMT
ENV MONGO_DOWNLOAD_SHA256=584bc98ce5755f419b7182c3abf1c632a4365e28577a4f498be2c291beeae7c2
# Thu, 19 Jul 2018 15:15:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 19 Jul 2018 15:15:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 19 Jul 2018 15:15:08 GMT
EXPOSE 27017/tcp
# Thu, 19 Jul 2018 15:15:09 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:d0dc9d8f5ea2c4c020baad73aacc777702fac8821ec0901ea9f85ad3490d64a1`  
		Last Modified: Sat, 21 Jul 2018 09:49:52 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3840e69e78a024e722777c38915db1789f12b9a970daa2f5173bedead36694`  
		Last Modified: Sat, 21 Jul 2018 09:52:34 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa72df169228e99cdc58794c07b7d21964d85ee4b2136bf06b927a2a8e6277e`  
		Last Modified: Sat, 21 Jul 2018 09:52:34 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e1d36b3c46001f39a68a2f039875ae25668f3872d2903a0ee4c24fbef8eae5`  
		Last Modified: Sat, 21 Jul 2018 09:52:31 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a2dcd8c95f87465ea14a4cf4586e960c20f5a0a707ff4a70cb0f2916baeaf9`  
		Last Modified: Sat, 21 Jul 2018 09:53:27 GMT  
		Size: 538.0 MB (538017465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0176aa7ea35ce6527b3454b6e1153d81661b11f128e03e8f8e312f0852e72ae`  
		Last Modified: Sat, 21 Jul 2018 09:52:31 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ceb5164df328fa3029bd7a5d129496134cb5e1f6c9696e3c4e37ff011370bb`  
		Last Modified: Sat, 21 Jul 2018 09:52:32 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3872604e12d9db23ddb1bbd92d2111d7cb80c0843359112189687b39e08ed0d2`  
		Last Modified: Sat, 21 Jul 2018 09:52:31 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
