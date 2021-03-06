## `jetty:jre8-alpine`

```console
$ docker pull jetty@sha256:a79784d19aa55c60c26f136947d7ad95e8f3e04d2e1b3539f841f8690999c698
```

-	Platforms:
	-	linux; amd64

### `jetty:jre8-alpine` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64302064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b260abf55dd8e74face22d97d5689285c117160cf106a89d65ea95ccd344a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 10 May 2017 16:38:16 GMT
ADD file:63f63606d6e289eb607c90e31de81802258906712727e473a2898f0f1ae55bb5 in / 
# Wed, 10 May 2017 16:38:17 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2017 22:39:51 GMT
ENV LANG=C.UTF-8
# Wed, 10 May 2017 22:39:53 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 10 May 2017 22:40:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Wed, 10 May 2017 22:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Wed, 10 May 2017 22:40:22 GMT
ENV JAVA_VERSION=8u121
# Wed, 10 May 2017 22:40:23 GMT
ENV JAVA_ALPINE_VERSION=8.121.13-r0
# Wed, 10 May 2017 22:40:28 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 11 May 2017 04:40:18 GMT
RUN addgroup -S jetty && adduser -D -S -H -G jetty jetty && rm -rf /etc/group- /etc/passwd- /etc/shadow-
# Thu, 11 May 2017 04:40:19 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 May 2017 04:40:19 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 11 May 2017 04:40:21 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 11 May 2017 04:40:22 GMT
WORKDIR /usr/local/jetty
# Thu, 11 May 2017 04:40:23 GMT
ENV JETTY_VERSION=9.4.5.v20170502
# Thu, 11 May 2017 04:40:24 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.5.v20170502/jetty-home-9.4.5.v20170502.tar.gz
# Thu, 11 May 2017 04:40:24 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D
# Thu, 11 May 2017 04:40:33 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps gnupg curl 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -r "$GNUPGHOME" 	&& tar -xvzf jetty.tar.gz 	&& mv jetty-home-$JETTY_VERSION/* ./ 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -fr jetty-home-$JETTY_VERSION/ 	&& apk del .build-deps 	&& rm -fr .build-deps 	&& rm -rf /tmp/hsperfdata_root
# Thu, 11 May 2017 04:40:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 May 2017 04:40:36 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 11 May 2017 04:40:37 GMT
WORKDIR /var/lib/jetty
# Thu, 11 May 2017 04:40:40 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket,setuid" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 11 May 2017 04:40:41 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 May 2017 04:40:43 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 11 May 2017 04:40:44 GMT
COPY file:4f7da2906a90932cfb90db54a45ee08f86b17253747db62085f7512c9efd46ad in / 
# Thu, 11 May 2017 04:40:45 GMT
EXPOSE 8080/tcp
# Thu, 11 May 2017 04:40:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 May 2017 04:40:46 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:cfc728c1c5584d8e0ae69368fc9c34d54d72651355573ba42554c2469a0a6299`  
		Last Modified: Wed, 10 May 2017 16:41:01 GMT  
		Size: 2.0 MB (1967906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b12b87f0a0e1bc0a163558cc56861b86355598153fb9e35273ece1dabe81cae`  
		Last Modified: Fri, 12 May 2017 15:19:23 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2361cda3c2da7cd65965703a6e97c9869536495a962105e26c948dd9a806e80d`  
		Last Modified: Fri, 12 May 2017 15:21:50 GMT  
		Size: 54.2 MB (54241012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c2009c9ce2f90b1fbf1c434ff6d361c05359cb3db42a738b0a8a81d1287405`  
		Last Modified: Sat, 13 May 2017 16:28:55 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4647ab68c9acef882707d003d64cc7b0b3035db1c15eef817114790e1b9285d0`  
		Last Modified: Sat, 13 May 2017 16:28:52 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11daf06cddcd517cf2b1e1826c40f7984f68ddd0561e936cc4b32b16b018fcd4`  
		Last Modified: Sat, 13 May 2017 16:33:29 GMT  
		Size: 8.1 MB (8088599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fd6c0e3bd91a5d3934615de22aab2a5f3fbc358ec34457db34be81fb05776d`  
		Last Modified: Sat, 13 May 2017 16:33:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0849673adab167da00422d5dd3c4f6f7496b6be304d5e7f670358564fc41dd`  
		Last Modified: Sat, 13 May 2017 16:33:28 GMT  
		Size: 2.3 KB (2251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702be4f60e5d79e8aaf3d18f102d8f1ae4edca69f922a36314836a945e4b7d4e`  
		Last Modified: Sat, 13 May 2017 16:33:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c6818db16c87294af96b6d143c85e4488812e6154092c05d7fca6d242d4d52`  
		Last Modified: Sat, 13 May 2017 16:33:28 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
