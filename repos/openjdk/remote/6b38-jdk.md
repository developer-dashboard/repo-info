## `openjdk:6b38-jdk`

```console
$ docker pull openjdk@sha256:72ad2c15b573438e29a6bbf0496c3d78ed6aa5138592b590b85a476b77e92467
```

-	Platforms:
	-	linux; amd64

### `openjdk:6b38-jdk` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189548013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1858c256d709559eb883451c03940397090dcb2146bf0d592773f7d1c1857f9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 May 2017 23:41:02 GMT
ADD file:5f4eeb9d08ac23595a4130e8b7689bd25379e92fecf5f62e18ea0f1c95d73c33 in / 
# Mon, 08 May 2017 23:41:17 GMT
CMD ["/bin/bash"]
# Tue, 09 May 2017 00:07:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 May 2017 00:08:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 May 2017 17:19:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 May 2017 17:19:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 May 2017 17:19:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 10 May 2017 13:54:38 GMT
RUN ln -svT "/usr/lib/jvm/java-6-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 10 May 2017 13:54:39 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 10 May 2017 13:54:40 GMT
ENV JAVA_VERSION=6b38
# Wed, 10 May 2017 13:54:41 GMT
ENV JAVA_DEBIAN_VERSION=6b38-1.13.10-1~deb7u1
# Wed, 10 May 2017 13:55:21 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		openjdk-6-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:af65d799fdb4729bcd56cfa8da95fe4f787ead4b4f434e878c60b3dfa0cebba1`  
		Last Modified: Mon, 08 May 2017 23:58:57 GMT  
		Size: 38.1 MB (38116549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcd4fbbe5807e6012f6fb4cf6bdcae934c77e41d49b46d4ecd9964d7f71619d`  
		Last Modified: Tue, 09 May 2017 16:03:50 GMT  
		Size: 7.0 MB (6953572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb94c92135ba3007986f5325b82b345302f445179b62da69cd717e5cc92b34b2`  
		Last Modified: Tue, 09 May 2017 16:04:25 GMT  
		Size: 37.9 MB (37942414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770582d3b9f383069446919a82c7a0f7646782eefe5b31222b82a80ae3844d46`  
		Last Modified: Sat, 13 May 2017 09:06:39 GMT  
		Size: 419.1 KB (419081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a61c8eb012e52f95ac41be157212e3da1718d9787cca145f995e49abc4a089`  
		Last Modified: Sat, 13 May 2017 09:06:39 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6003cdddf648d272350ae4732d29db1eb7b70c05e56d87b15a9f50124e68ba5`  
		Last Modified: Sat, 13 May 2017 09:06:39 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4400c05c75d71aa500e4bdc2c072c41df8a58e28a62ef6dff584770f1949192f`  
		Last Modified: Sat, 13 May 2017 09:06:56 GMT  
		Size: 106.1 MB (106116026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
