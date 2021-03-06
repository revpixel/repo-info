## `couchdb:1-couchperuser`

```console
$ docker pull couchdb@sha256:bf6e38728225d1301f96025463a790b42e3da83318b3c71354ee02fd779f5557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchdb:1-couchperuser` - linux; amd64

```console
$ docker pull couchdb@sha256:390fd97472cad3916a047c05f666707998635593d0939ccd6baef17fb34bb42a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115722291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0eb1230276979dc20c90a1f62deb7f9c9b6c2e2eff3d553ec25601a77103836`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["couchdb"]`

```dockerfile
# Tue, 17 Jul 2018 00:20:47 GMT
ADD file:b90e572f7462a23e2e4eda57269941ee7d8f078ca8ab1eefca86927713e13365 in / 
# Tue, 17 Jul 2018 00:20:48 GMT
CMD ["bash"]
# Tue, 17 Jul 2018 01:27:14 GMT
MAINTAINER CouchDB Developers dev@couchdb.apache.org
# Tue, 17 Jul 2018 01:27:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 17 Jul 2018 01:33:26 GMT
RUN apt-get update -y && apt-get install -y --no-install-recommends     ca-certificates     curl     erlang-nox     libicu52     libmozjs185-1.0     libnspr4     libnspr4-0d   && rm -rf /var/lib/apt/lists/*
# Tue, 17 Jul 2018 01:33:38 GMT
ENV GOSU_VERSION=1.10
# Tue, 17 Jul 2018 01:33:38 GMT
ENV TINI_VERSION=0.16.1
# Tue, 17 Jul 2018 01:34:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -r "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     tini --version;         apt-get purge -y --auto-remove wget
# Tue, 17 Jul 2018 01:34:24 GMT
ENV GPG_KEYS=15DD4F3B8AACA54740EB78C7B7B7C53943ECCEE1   1CFBFA43C19B6DF4A0CA3934669C02FFDF3CEBA3   25BBBAC113C1BFD5AA594A4C9F96B92930380381   4BFCA2B99BADC6F9F105BEC9C5E32E2D6B065BFB   5D680346FAA3E51B29DBCB681015F68F9DA248BC   7BCCEB868313DDA925DF1805ECA5BCB7BB9656B0   C3F4DFAEAD621E1C94523AEEC376457E61D50B88   D2B17F9DA23C0A10991AF2E3D9EE01E47852AEE4   E0AF0A194D55C84E4A19A801CDB0C0F904F4EE9B
# Tue, 17 Jul 2018 01:34:26 GMT
RUN set -xe   && for key in $GPG_KEYS; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done
# Tue, 17 Jul 2018 01:34:26 GMT
ENV COUCHDB_VERSION=1.7.2
# Tue, 17 Jul 2018 01:36:59 GMT
RUN buildDeps='     gcc     g++     erlang-dev     libcurl4-openssl-dev     libicu-dev     libmozjs185-dev     libnspr4-dev     make   '   && apt-get update && apt-get install -y --no-install-recommends $buildDeps   && curl -fSL https://apache.osuosl.org/couchdb/source/$COUCHDB_VERSION/apache-couchdb-$COUCHDB_VERSION.tar.gz -o couchdb.tar.gz   && curl -fSL https://www.apache.org/dist/couchdb/source/$COUCHDB_VERSION/apache-couchdb-$COUCHDB_VERSION.tar.gz.asc -o couchdb.tar.gz.asc   && gpg --batch --verify couchdb.tar.gz.asc couchdb.tar.gz   && mkdir -p /usr/src/couchdb   && tar -xzf couchdb.tar.gz -C /usr/src/couchdb --strip-components=1   && cd /usr/src/couchdb   && ./configure --with-js-lib=/usr/lib --with-js-include=/usr/include/mozjs   && make && make install   && apt-get purge -y --auto-remove $buildDeps   && rm -rf /var/lib/apt/lists/* /usr/src/couchdb /couchdb.tar.gz*   && chown -R couchdb:couchdb     /usr/local/lib/couchdb /usr/local/etc/couchdb     /usr/local/var/lib/couchdb /usr/local/var/log/couchdb /usr/local/var/run/couchdb   && chmod -R g+rw     /usr/local/lib/couchdb /usr/local/etc/couchdb     /usr/local/var/lib/couchdb /usr/local/var/log/couchdb /usr/local/var/run/couchdb   && mkdir -p /var/lib/couchdb   && sed -e 's/^bind_address = .*$/bind_address = 0.0.0.0/' -i /usr/local/etc/couchdb/default.ini   && sed -e 's!/usr/local/var/log/couchdb/couch.log$!/dev/null!' -i /usr/local/etc/couchdb/default.ini
# Tue, 17 Jul 2018 01:37:00 GMT
COPY file:f606d0607ab768e5075c660a93ea1c8c4d1306c1d2dff718d4d314268f35517b in / 
# Tue, 17 Jul 2018 01:37:00 GMT
VOLUME [/usr/local/var/lib/couchdb]
# Tue, 17 Jul 2018 01:37:00 GMT
EXPOSE 5984/tcp
# Tue, 17 Jul 2018 01:37:00 GMT
WORKDIR /var/lib/couchdb
# Tue, 17 Jul 2018 01:37:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 17 Jul 2018 01:37:01 GMT
CMD ["couchdb"]
# Tue, 17 Jul 2018 01:37:38 GMT
MAINTAINER CouchDB Developers dev@couchdb.apache.org
# Tue, 17 Jul 2018 01:37:38 GMT
ENV COUCHPERUSER_SHA=5d28db3272eea9619d4391b33aae6030f0319ecc54aa2a2f2b6c6a8d448f03f2
# Tue, 17 Jul 2018 01:38:55 GMT
RUN apt-get update && apt-get install -y rebar make  && mkdir -p /usr/local/lib/couchdb/plugins/couchperuser  && cd /usr/local/lib/couchdb/plugins  && curl -L -o couchperuser.tar.gz https://github.com/etrepum/couchperuser/archive/1.1.0.tar.gz  && echo "$COUCHPERUSER_SHA *couchperuser.tar.gz" | sha256sum -c -  && tar -xzf couchperuser.tar.gz -C couchperuser --strip-components=1  && rm couchperuser.tar.gz  && cd couchperuser  && make  && apt-get purge -y --auto-remove rebar make
```

-	Layers:
	-	`sha256:d660b1f15b9bfb8142f50b518156f2d364d9642fe05854538b060498e2f7928d`  
		Last Modified: Tue, 17 Jul 2018 00:34:02 GMT  
		Size: 54.3 MB (54252125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7aab2be0234a656782e87c9767c5a20906fa27b7d4935e372c24680ae67f16`  
		Last Modified: Tue, 17 Jul 2018 01:39:38 GMT  
		Size: 3.7 KB (3696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9221abe9076804250c5dd53558920302d43468b1dd6ab67c7656e4e93dab1233`  
		Last Modified: Tue, 17 Jul 2018 01:42:48 GMT  
		Size: 42.1 MB (42065927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f172ac18ec412b1aa70cce2c3d8e3a1829dee0c95c3eb8284be53404ef67a4`  
		Last Modified: Tue, 17 Jul 2018 01:42:38 GMT  
		Size: 826.3 KB (826334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd126ba0e97cc478a42ba4ca8197d2d7da918049a3c310d8d4d4aa7814e550c`  
		Last Modified: Tue, 17 Jul 2018 01:42:38 GMT  
		Size: 516.1 KB (516126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85f8bcd0c64afb527c01546be30c0a52cc04780b9c635822baeeb6bd5d253f`  
		Last Modified: Tue, 17 Jul 2018 01:42:39 GMT  
		Size: 7.7 MB (7661298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d086ba53de539ae2175d983887a245c0a721592c9cd0f786cfac86f689455d`  
		Last Modified: Tue, 17 Jul 2018 01:42:37 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a76c161a218b473b74b642459bf08c775bf82c947cf0932c2b10140f1e92510`  
		Last Modified: Tue, 17 Jul 2018 01:44:00 GMT  
		Size: 10.4 MB (10395511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
