## `maven:3-jdk-7-onbuild-alpine`

```console
$ docker pull maven@sha256:a0987ae2f0b36d90af839a2c917cd8f63ce3128d92ee8217a85c5499ffef3fcb
```

-	Platforms:
	-	linux; amd64

### `maven:3-jdk-7-onbuild-alpine` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89080360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cca92217dcefb0f753fad01e835f11fdb2266e9dea64b408eb3a24040a7c76c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 May 2017 16:37:36 GMT
ADD file:9c596c6cb8ba1d7f93d4dc5fc3f42bfcd5edca57d5be5d60ea04ef42f55fb7a8 in / 
# Wed, 10 May 2017 16:37:37 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2017 21:45:43 GMT
ENV LANG=C.UTF-8
# Wed, 10 May 2017 21:45:45 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 10 May 2017 21:45:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.7-openjdk
# Wed, 10 May 2017 21:45:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.7-openjdk/jre/bin:/usr/lib/jvm/java-1.7-openjdk/bin
# Wed, 10 May 2017 21:45:47 GMT
ENV JAVA_VERSION=7u121
# Wed, 10 May 2017 21:45:48 GMT
ENV JAVA_ALPINE_VERSION=7.121.2.6.8-r0
# Wed, 10 May 2017 21:45:55 GMT
RUN set -x 	&& apk add --no-cache 		openjdk7="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 11 May 2017 05:15:56 GMT
RUN apk add --no-cache curl tar bash
# Thu, 11 May 2017 05:15:57 GMT
ARG MAVEN_VERSION=3.5.0
# Thu, 11 May 2017 05:15:58 GMT
ARG USER_HOME_DIR=/root
# Thu, 11 May 2017 05:15:58 GMT
ARG SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034
# Thu, 11 May 2017 05:15:59 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries
# Thu, 11 May 2017 05:16:01 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-$MAVEN_VERSION-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 11 May 2017 05:16:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 11 May 2017 05:16:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 11 May 2017 05:16:04 GMT
COPY file:e3aa30a24fcf60a59710465ac66fc1d53c35590a74fcdd51e12a5cbce393904b in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 11 May 2017 05:16:05 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Thu, 11 May 2017 05:16:06 GMT
VOLUME [/root/.m2]
# Thu, 11 May 2017 05:16:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 11 May 2017 05:16:08 GMT
CMD ["mvn"]
# Thu, 11 May 2017 05:16:53 GMT
RUN mkdir -p /usr/src/app
# Thu, 11 May 2017 05:16:54 GMT
WORKDIR /usr/src/app
# Thu, 11 May 2017 05:16:55 GMT
ONBUILD ADD . /usr/src/app
# Thu, 11 May 2017 05:16:55 GMT
ONBUILD RUN mvn install
```

-	Layers:
	-	`sha256:79650cf9cc01ddb17cb9c4036ba9268528b775fe0322f347d15b5e4176928f34`  
		Last Modified: Wed, 10 May 2017 16:40:36 GMT  
		Size: 2.4 MB (2383037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef60c9fac754d4f3ad417367907ef7e198902936bad7e24749f08d31ad051ea`  
		Last Modified: Fri, 12 May 2017 15:10:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10ab02e0419619a869a1f649d3eb6efbc4fb91b214709cb2e27af96a50f589a`  
		Last Modified: Fri, 12 May 2017 15:10:38 GMT  
		Size: 76.2 MB (76239840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e04f57e31c78208cc5b3e6a88e91628766f2d58a02957ac23aebf9b53df204`  
		Last Modified: Sat, 13 May 2017 17:04:40 GMT  
		Size: 1.8 MB (1783308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937d9327f372a9d4505338eaccc7f3311281273bb09c100a4a80ef309cb2637e`  
		Last Modified: Sat, 13 May 2017 17:04:40 GMT  
		Size: 8.7 MB (8672750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ea97eef127be9cd3cba09523a8015ef643169b84d7f0cc6c5fd27f5caf4cdc`  
		Last Modified: Sat, 13 May 2017 17:04:39 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a5bdbf75a06e9ff0a842cd6bbc5d8662f52721804bf05ef23e18729d12ebc8`  
		Last Modified: Sat, 13 May 2017 17:04:39 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c9db6285a4dd616ec61d348c0787421494c2c2fe1608723b01b4b7f63fb2e9`  
		Last Modified: Sat, 13 May 2017 17:07:01 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
