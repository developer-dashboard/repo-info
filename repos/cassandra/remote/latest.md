## `cassandra:latest`

```console
$ docker pull cassandra@sha256:c8be75ac955e717c2e52034fece8cdd155e83a4fb627c810a2bae1082ce489c7
```

-	Platforms:
	-	linux; amd64

### `cassandra:latest` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164921768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154b919bf8ce6c0d5af25a9ea1d9c763efa72dcc4606d901e82f2e9dc1f9460b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Mon, 08 May 2017 23:28:14 GMT
ADD file:f4e6551ac34ab446a297849489a5693d67a7e76c9cb9ed9346d82392c9d9a5fe in / 
# Mon, 08 May 2017 23:28:15 GMT
CMD ["/bin/bash"]
# Mon, 08 May 2017 23:29:37 GMT
RUN awk '$1 ~ "^deb" { $3 = $3 "-backports"; print; exit }' /etc/apt/sources.list > /etc/apt/sources.list.d/backports.list
# Tue, 09 May 2017 15:59:30 GMT
RUN groupadd -r cassandra --gid=999 && useradd -r -g cassandra --uid=999 cassandra
# Tue, 09 May 2017 15:59:31 GMT
ENV GOSU_VERSION=1.7
# Tue, 09 May 2017 15:59:52 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 09 May 2017 16:00:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libjemalloc1 && rm -rf /var/lib/apt/lists/*
# Tue, 09 May 2017 16:00:02 GMT
RUN { 		echo 'Package: openjdk-* ca-certificates-java'; 		echo 'Pin: release n=*-backports'; 		echo 'Pin-Priority: 990'; 	} > /etc/apt/preferences.d/java-backports
# Tue, 09 May 2017 16:00:02 GMT
ENV GPG_KEYS=514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA
# Tue, 09 May 2017 16:12:54 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/cassandra.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 09 May 2017 16:15:33 GMT
RUN echo 'deb http://www.apache.org/dist/cassandra/debian 310x main' >> /etc/apt/sources.list.d/cassandra.list
# Tue, 09 May 2017 16:15:34 GMT
ENV CASSANDRA_VERSION=3.10
# Tue, 09 May 2017 16:16:06 GMT
RUN apt-get update 	&& apt-get install -y 		cassandra="$CASSANDRA_VERSION" 		cassandra-tools="$CASSANDRA_VERSION" 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 May 2017 16:16:08 GMT
RUN sed -ri 's/^(JVM_PATCH_VERSION)=.*/\1=25/' /etc/cassandra/cassandra-env.sh
# Tue, 09 May 2017 16:16:08 GMT
ENV CASSANDRA_CONFIG=/etc/cassandra
# Tue, 09 May 2017 16:16:09 GMT
COPY file:fe6ed91be8debf19da443f09935b578bf6599e644b7a670bf7048d33fb2efa9e in /docker-entrypoint.sh 
# Tue, 09 May 2017 16:16:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 May 2017 16:16:12 GMT
RUN mkdir -p /var/lib/cassandra "$CASSANDRA_CONFIG" 	&& chown -R cassandra:cassandra /var/lib/cassandra "$CASSANDRA_CONFIG" 	&& chmod 777 /var/lib/cassandra "$CASSANDRA_CONFIG"
# Tue, 09 May 2017 16:16:12 GMT
VOLUME [/var/lib/cassandra]
# Tue, 09 May 2017 16:16:13 GMT
EXPOSE 7000/tcp 7001/tcp 7199/tcp 9042/tcp 9160/tcp
# Tue, 09 May 2017 16:16:14 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:10a267c67f423630f3afe5e04bbbc93d578861ddcc54283526222f3ad5e895b9`  
		Last Modified: Mon, 08 May 2017 23:43:59 GMT  
		Size: 52.6 MB (52584016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0782edf7745aa2722586fd3e27620d5831cac3e4a6162d154aeb735618f1c412`  
		Last Modified: Mon, 08 May 2017 23:46:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80fb4268b40efc6bcea08d2ecb3bd700cb0455b98ce3062dee7ba0de855c8dd`  
		Last Modified: Thu, 11 May 2017 14:45:39 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e953a99f21041c9a41843f3fb4b2199e6a53ab01bdffb2009a56d63e86e8089`  
		Last Modified: Thu, 11 May 2017 14:45:39 GMT  
		Size: 1.3 MB (1307766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8619ee991e193db8069078f20ba6774cf3938dae7b11ffb5f824cfbdd9569eb0`  
		Last Modified: Thu, 11 May 2017 14:45:39 GMT  
		Size: 177.1 KB (177080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60bbbf22fd9085690ccf03b2de4edc3126b182d28dbab2d255330089af47d0d`  
		Last Modified: Thu, 11 May 2017 14:45:38 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae31195e0ccba2e1abbb8037750b7d9166e9b0a81f7cecaf09dcc2476eabaef`  
		Last Modified: Thu, 11 May 2017 14:45:36 GMT  
		Size: 18.2 KB (18228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eedc5c82232c4a728f2ee03bf24727223ef5d507399b82184e52ee22caaac3c`  
		Last Modified: Thu, 11 May 2017 14:49:22 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb88cba8451d38761f8ca85db99fad1cbca4fb93c6f8dea5f7de6b287d03685f`  
		Last Modified: Thu, 11 May 2017 14:49:39 GMT  
		Size: 110.8 MB (110798423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8745e26884b1b4edae34b6cf13ad7125a2843309cb5bb44278670ab2e5589acd`  
		Last Modified: Thu, 11 May 2017 14:49:22 GMT  
		Size: 4.4 KB (4396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7fbe5119031b00ab149aedc1231bf6c03b01d9eb74899bc1608ed4dda2ab99`  
		Last Modified: Thu, 11 May 2017 14:49:22 GMT  
		Size: 732.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171da7079ef2aca3a8bb0ca9e003aafec3a69962990787095a37d79114bd0407`  
		Last Modified: Thu, 11 May 2017 14:49:22 GMT  
		Size: 28.4 KB (28381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
