## `maven:3-jdk-9`

```console
$ docker pull maven@sha256:e49f9cc8838422811a1b1798fa6732b5754fb6fd34df8042999886789f670e49
```

-	Platforms:
	-	linux; amd64

### `maven:3-jdk-9` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272067471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8fbdeecc59d50b82e1d371b82f9d845dde91f20328af0c5e186451cc16c594`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 May 2017 23:32:23 GMT
ADD file:485c5e010aec72afb62c7fe5bc651d739dad42e9baf81e811e6b3f369c72a917 in / 
# Mon, 08 May 2017 23:32:23 GMT
CMD ["/bin/bash"]
# Mon, 08 May 2017 23:57:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 08 May 2017 23:58:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2017 14:01:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 May 2017 14:01:36 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Wed, 10 May 2017 14:01:37 GMT
ENV LANG=C.UTF-8
# Wed, 10 May 2017 14:01:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 10 May 2017 14:01:40 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 10 May 2017 14:01:41 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 19 May 2017 23:14:32 GMT
ENV JAVA_VERSION=9~b170
# Fri, 19 May 2017 23:14:32 GMT
ENV JAVA_DEBIAN_VERSION=9~b170-2
# Fri, 19 May 2017 23:15:03 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Mon, 22 May 2017 18:10:19 GMT
ARG MAVEN_VERSION=3.5.0
# Mon, 22 May 2017 18:10:20 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 May 2017 18:10:21 GMT
ARG SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034
# Mon, 22 May 2017 18:10:21 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries
# Mon, 22 May 2017 18:10:24 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-$MAVEN_VERSION-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 22 May 2017 18:10:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 May 2017 18:10:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 May 2017 18:10:27 GMT
COPY file:0ef06202c434fd6422eaf47010435819a589a77ab2d8d5d3b9e497de2fd57b3f in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 22 May 2017 18:10:28 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Mon, 22 May 2017 18:10:29 GMT
VOLUME [/root/.m2]
# Mon, 22 May 2017 18:10:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 May 2017 18:10:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:705d0395ca7a3af6e4662abc693a18e13ffd882aaf93db55fc1a1b313b69cad8`  
		Last Modified: Mon, 08 May 2017 23:48:38 GMT  
		Size: 45.3 MB (45254594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95bfff6e637f7f460b136c6303bc8a9e3341d1821affa81f98ce0d8e2895d0a`  
		Last Modified: Tue, 09 May 2017 15:58:23 GMT  
		Size: 11.3 MB (11265380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403c3d1db0ff620b98f8da5320fbc4e7557b3539d0c89fe984f5f234de90fd16`  
		Last Modified: Tue, 09 May 2017 15:59:04 GMT  
		Size: 50.9 MB (50947148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576e6eaba21c7578ad992b4ff9f6eff4fd1ca8329b9a6c1e9720e2a524b248a0`  
		Last Modified: Fri, 12 May 2017 15:25:09 GMT  
		Size: 659.6 KB (659573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246f443a7ab8ddd8d3567f262c1c4803c4cf5ff9783b17741610868c8d8a0074`  
		Last Modified: Fri, 12 May 2017 15:25:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2c23f42b858c7463b45cdfa706ba72abae930789ebbe7a1b922a1a4edd6b4b`  
		Last Modified: Fri, 12 May 2017 15:25:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2182f7c7320ae2a988e779fffa1264e78dcf1449007063abdd14f92a64aecc`  
		Last Modified: Fri, 12 May 2017 15:25:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8554bacf4b3fcb249c768144ab246015f037740227d4221c8e1dc73fef9393af`  
		Last Modified: Fri, 19 May 2017 23:31:57 GMT  
		Size: 155.3 MB (155266329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6facd240422f4a31eb3f98588de4341607424422ffb9ac091aa2d049f20066c`  
		Last Modified: Mon, 22 May 2017 18:26:49 GMT  
		Size: 8.7 MB (8672794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1081dd424e7d27eb5e967e171871eb01709e9fca8f9a1a22294153551ec48a90`  
		Last Modified: Mon, 22 May 2017 18:26:48 GMT  
		Size: 721.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044f573947d65e47b75b4ea0f21bc2e58e45673894bd71467e9524c9bf315917`  
		Last Modified: Mon, 22 May 2017 18:26:48 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
