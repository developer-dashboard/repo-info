## `mariadb:latest`

```console
$ docker pull mariadb@sha256:c987e36e50dcc02a17b8ea6319dd0f82d0e3ca13a85a3cc94f1857bf5561fd1c
```

-	Platforms:
	-	linux; amd64

### `mariadb:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134854164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0322bb409611aa9ecec09eb469ce1da062415f653811387b5e9857f7f7f5e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 May 2017 23:28:14 GMT
ADD file:f4e6551ac34ab446a297849489a5693d67a7e76c9cb9ed9346d82392c9d9a5fe in / 
# Mon, 08 May 2017 23:28:15 GMT
CMD ["/bin/bash"]
# Tue, 09 May 2017 17:26:22 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 09 May 2017 17:26:23 GMT
ENV GOSU_VERSION=1.7
# Tue, 09 May 2017 17:26:43 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 09 May 2017 17:26:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 May 2017 17:27:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		apt-transport-https ca-certificates 		pwgen 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 May 2017 17:27:03 GMT
ENV GPG_KEYS=199369E5404BD5FC7D2FE43BCBCB082A1BB943DB 	430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	4D1BB29D63D98E422B2113B19334A25F8507EFA5
# Tue, 09 May 2017 17:27:06 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 09 May 2017 17:27:08 GMT
RUN echo "deb https://repo.percona.com/apt jessie main" > /etc/apt/sources.list.d/percona.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release o=Percona Development Team'; 		echo 'Pin-Priority: 998'; 	} > /etc/apt/preferences.d/percona
# Tue, 09 May 2017 17:27:08 GMT
ENV MARIADB_MAJOR=10.1
# Wed, 31 May 2017 21:29:44 GMT
ENV MARIADB_VERSION=10.1.24+maria-1~jessie
# Wed, 31 May 2017 21:29:45 GMT
RUN echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/debian jessie main" > /etc/apt/sources.list.d/mariadb.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 31 May 2017 21:30:31 GMT
RUN { 		echo mariadb-server-$MARIADB_MAJOR mysql-server/root_password password 'unused'; 		echo mariadb-server-$MARIADB_MAJOR mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mariadb-server=$MARIADB_VERSION 		percona-xtrabackup 		socat 	&& rm -rf /var/lib/apt/lists/* 	&& sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 31 May 2017 21:30:33 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/my.cnf 	&& echo 'skip-host-cache\nskip-name-resolve' | awk '{ print } $1 == "[mysqld]" && c == 0 { c = 1; system("cat") }' /etc/mysql/my.cnf > /tmp/my.cnf 	&& mv /tmp/my.cnf /etc/mysql/my.cnf
# Wed, 31 May 2017 21:30:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 31 May 2017 21:30:35 GMT
COPY file:d559178e6a2929e36791c6a1fa232dc4ac4298ecc446d38972ee1d2a58e30621 in /usr/local/bin/ 
# Wed, 31 May 2017 21:30:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 31 May 2017 21:30:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 May 2017 21:30:38 GMT
EXPOSE 3306/tcp
# Wed, 31 May 2017 21:30:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:10a267c67f423630f3afe5e04bbbc93d578861ddcc54283526222f3ad5e895b9`  
		Last Modified: Mon, 08 May 2017 23:43:59 GMT  
		Size: 52.6 MB (52584016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dcc7bb2a88d3f5f2e2f57c03798de132417029412461fa5c2a3980a432ac00`  
		Last Modified: Sat, 13 May 2017 07:01:23 GMT  
		Size: 2.1 KB (2066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e7a0445698ef7ccb14c188ceef9c98785c4adf909704a86a019721e94a8eff`  
		Last Modified: Sat, 13 May 2017 07:01:23 GMT  
		Size: 1.3 MB (1307767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61839a176f4d61f2b383652722e0dc8f63ffd12828405b1d7d0facc903b4df`  
		Last Modified: Sat, 13 May 2017 07:01:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64675690edb1a9570a687eeb066ea1c9f445ebea6143d0e3315343a8433a6282`  
		Last Modified: Sat, 13 May 2017 07:01:25 GMT  
		Size: 6.7 MB (6674171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de17e25148882a0df702a696d70beba7abcf53fd04fc777e1418dbc6304a1c8`  
		Last Modified: Sat, 13 May 2017 07:01:22 GMT  
		Size: 20.8 KB (20827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f814b22b783e01a2e2dce50c55554ca2777bb4f56098398d96d4532aa7642e1f`  
		Last Modified: Sat, 13 May 2017 07:01:20 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527ba05ab10059761c14b9ae7947c26ca16257de47fd325495a8f8e8b0bb13f8`  
		Last Modified: Wed, 31 May 2017 21:32:40 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb46c338b799cf34cfcc57e561219d15f0b22111533697532db9f2872776aa4e`  
		Last Modified: Wed, 31 May 2017 21:32:52 GMT  
		Size: 74.3 MB (74259271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9db88489b39a0662dc3138dcb689d3504de8b7cc777a47dfae445a3693c6ef`  
		Last Modified: Wed, 31 May 2017 21:32:39 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2c709137569599306d15fa23b15d24cc9c02886f95836e278358b5262597c7`  
		Last Modified: Wed, 31 May 2017 21:32:39 GMT  
		Size: 2.5 KB (2543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46185579593e9be386e3d4dc2fceae22981d16f3ce556148bb8ad9a0863a4969`  
		Last Modified: Wed, 31 May 2017 21:32:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
