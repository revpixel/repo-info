## `golang:rc-windowsservercore-1803`

```console
$ docker pull golang@sha256:6c0948e97f97fac62dbf38162b85813d3b412a4c9afc27419c0824a07dd37b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.165; amd64

### `golang:rc-windowsservercore-1803` - windows version 10.0.17134.165; amd64

```console
$ docker pull golang@sha256:6e8c088f2347b07f84c9d1850c3f54399ded18d99f40508c94df1f052dabedd5
```

-	Docker Version: 17.06.2-ee-13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363650061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e51b431a72a61cae70252399885da3a41662a36effc9a0e109c9324ac739b5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 10.0.17134.1
# Sat, 07 Jul 2018 22:48:41 GMT
RUN Install update 10.0.17134.165
# Fri, 13 Jul 2018 10:07:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Jul 2018 10:07:26 GMT
ENV GIT_VERSION=2.11.1
# Fri, 13 Jul 2018 10:07:27 GMT
ENV GIT_TAG=v2.11.1.windows.1
# Fri, 13 Jul 2018 10:07:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.11.1.windows.1/MinGit-2.11.1-64-bit.zip
# Fri, 13 Jul 2018 10:07:28 GMT
ENV GIT_DOWNLOAD_SHA256=668d16a799dd721ed126cc91bed49eb2c072ba1b25b50048280a4e2c5ed56e59
# Fri, 13 Jul 2018 10:08:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  git --version'; git --version; 		Write-Host 'Complete.';
# Fri, 13 Jul 2018 10:08:56 GMT
ENV GOPATH=C:\gopath
# Fri, 13 Jul 2018 10:09:39 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 21 Jul 2018 09:28:07 GMT
ENV GOLANG_VERSION=1.11beta2
# Sat, 21 Jul 2018 09:33:55 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '91072cdc2cbf7b0e94c5706aea86e09d4a044aa6b60f4db4c0869ca29a8befa4'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Complete.';
# Sat, 21 Jul 2018 09:33:56 GMT
WORKDIR C:\gopath
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
	-	`sha256:5e25b1252e9b6c8bdfcec66e75be65af2baf4bcf1a67dc96422fef339cc4912c`  
		Last Modified: Fri, 13 Jul 2018 11:07:53 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb8204d8ec55cb4f90f7d714268cc09d8ba91ea9367280e6ad469af2d402586`  
		Last Modified: Fri, 13 Jul 2018 11:07:53 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259348c7b912e7c7ec2419f712b8308df80b66b627c4de2676c4cc03d26c7bf4`  
		Last Modified: Fri, 13 Jul 2018 11:07:50 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cea0dfd17e7231f41619c84a6bfde0dd7a121a3d839651ca0566be9ec2c9ea4`  
		Last Modified: Fri, 13 Jul 2018 11:07:49 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b833d9bde7c5fb916270d56937979e5585ece9145afcad775c8861c15a240ad`  
		Last Modified: Fri, 13 Jul 2018 11:07:49 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5d404de536327f6e5736ad2f9ee6a2186c5ca4975f143da218f8015d66bc43`  
		Last Modified: Fri, 13 Jul 2018 11:08:00 GMT  
		Size: 29.0 MB (28959589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f17e2bb7e96c2294d7e1e57f7b0e50b57bbbe1b6324a8778cf21a0d66b8ffa`  
		Last Modified: Fri, 13 Jul 2018 11:07:45 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ad9df6429f66007fe2647b7190df00610952251ce56d5dfc48fa7ca5fffd9d`  
		Last Modified: Fri, 13 Jul 2018 11:07:46 GMT  
		Size: 296.8 KB (296800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a59f18f9ff844f56f27dad3772269b21a12a5dfbfa237700babdca810955c4a`  
		Last Modified: Sat, 21 Jul 2018 09:43:55 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95a221ad47273f282a6f803881fb50a181e9b56e4e1e36d44f57dd975bf1828`  
		Last Modified: Sat, 21 Jul 2018 09:45:17 GMT  
		Size: 181.2 MB (181174505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bfb8be80f5fc3b8ee2d4f04c666d83d928a369dd8207aedeb61bd5a964cd9d`  
		Last Modified: Sat, 21 Jul 2018 09:43:55 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
