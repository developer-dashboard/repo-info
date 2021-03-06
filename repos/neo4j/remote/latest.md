## `neo4j:latest`

```console
$ docker pull neo4j@sha256:a924fd66ed70b546676067b3797c07214b97a33db4696ce9b4966047c1e404ff
```

-	Platforms:
	-	linux; amd64

### `neo4j:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135880191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ca73ed691a42e52ba3f302a864205121fc2b4f4565d817a8bed9a16a992528`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 May 2017 23:33:21 GMT
ADD file:ce33aabbc5f370e58ebe911e081ce093e3df18d689c2d5a5d092c77973f62a54 in / 
# Thu, 25 May 2017 23:33:22 GMT
CMD ["/bin/sh"]
# Thu, 01 Jun 2017 16:58:46 GMT
ENV LANG=C.UTF-8
# Thu, 01 Jun 2017 16:58:47 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 01 Jun 2017 17:00:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Thu, 01 Jun 2017 17:00:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 01 Jun 2017 17:00:31 GMT
ENV JAVA_VERSION=8u131
# Thu, 01 Jun 2017 17:00:32 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r1
# Thu, 01 Jun 2017 17:00:39 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 02 Jun 2017 16:19:47 GMT
RUN apk add --no-cache --quiet     bash     curl
# Fri, 02 Jun 2017 16:20:06 GMT
ENV NEO4J_SHA256=24fd6a704e0d80c4b4f9a3d17ce0db23f258a8cdcfa1eb28d7803b7d1811ee96 NEO4J_TARBALL=neo4j-community-3.2.1-unix.tar.gz
# Fri, 02 Jun 2017 16:20:07 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.2.1-unix.tar.gz
# Fri, 02 Jun 2017 16:20:08 GMT
COPY file:2e411d607fa15f91ae6f4b515dde6bf3e158d34c0036556e00553ed1c50cd63d in /tmp/ 
# Fri, 02 Jun 2017 16:20:50 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.2.1-unix.tar.gz
RUN curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -csw -     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* /var/lib/neo4j     && rm ${NEO4J_TARBALL}     && mv /var/lib/neo4j/data /data     && ln -s /data /var/lib/neo4j/data     && apk del curl
# Fri, 02 Jun 2017 16:20:53 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2017 16:20:54 GMT
VOLUME [/data]
# Fri, 02 Jun 2017 16:20:56 GMT
COPY file:4b58674fde5f35ee7b68cae22e9b985fa91c7de85350af95dcdef88ef233c3d6 in /docker-entrypoint.sh 
# Fri, 02 Jun 2017 16:20:57 GMT
EXPOSE 7473/tcp 7474/tcp 7687/tcp
# Fri, 02 Jun 2017 16:20:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2017 16:20:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2aecc7e1714b6fad58d13aedb0639011b37b86f743ba7b6a52d82bd03014b78e`  
		Last Modified: Thu, 25 May 2017 23:36:54 GMT  
		Size: 2.0 MB (1990101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bb7a1c6ee7ae261bc9a503b112a715153b44524eaf20763357e3c4b1b32983`  
		Last Modified: Thu, 01 Jun 2017 17:04:59 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f1d6835b7d56cd0f4ee6793e1018d3138063fe44de5fac8522d9492c77da7c`  
		Last Modified: Thu, 01 Jun 2017 17:15:06 GMT  
		Size: 54.3 MB (54280719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99d7149263d8cb5ecde83ffbe0b45ed1365fd89a010862e77cfb528b4a6f9d8`  
		Last Modified: Fri, 02 Jun 2017 16:41:00 GMT  
		Size: 1.5 MB (1500952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5210e62f0e6c3006fe79bc70723f7bf2940dbfbb98b9cdffef5ad16d595885af`  
		Last Modified: Fri, 02 Jun 2017 16:40:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4601e7113ac07b72ceea8f2c202cffaf1d1802e370b1bf82b34faed609d01fa`  
		Last Modified: Fri, 02 Jun 2017 16:41:05 GMT  
		Size: 78.1 MB (78106328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd987a14ea0b66a1aef5b3ba5c1b3d959e778511dc8538f59553bfa35de95f76`  
		Last Modified: Fri, 02 Jun 2017 16:40:58 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
