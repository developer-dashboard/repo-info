## `kong:latest`

```console
$ docker pull kong@sha256:ca0269609f6e627e8c58e91350f50bc426a66bcf86307da80358f9553afcddc6
```

-	Platforms:
	-	linux; amd64

### `kong:latest` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123292736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a0f41778308e15204656732312f5185906525c80c367580c49e7b9deda4031`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Thu, 11 May 2017 19:45:46 GMT
ADD file:f3be3f14a2136b0c38b2d80b90cb1f3bbe5b3c78d35a94f3a0f1fe4219e1806f in / 
# Thu, 11 May 2017 19:45:48 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20170510
# Thu, 11 May 2017 19:45:49 GMT
CMD ["/bin/bash"]
# Thu, 11 May 2017 19:58:34 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Tue, 30 May 2017 17:04:52 GMT
ENV KONG_VERSION=0.10.3
# Tue, 30 May 2017 17:05:25 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Tue, 30 May 2017 17:05:28 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Tue, 30 May 2017 17:05:30 GMT
COPY file:e806c057c1c71a8dd5e684244eed51d4ff17ca43efe7233573320a3bf8dda3a4 in /docker-entrypoint.sh 
# Tue, 30 May 2017 17:05:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 30 May 2017 17:05:32 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Tue, 30 May 2017 17:05:33 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:343b0936103607602d236363460c0368a1cad0ef58a534d5a5c2ecd9f8c2f3dd`  
		Last Modified: Thu, 11 May 2017 19:46:47 GMT  
		Size: 70.5 MB (70522725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d6d56bec9478a03e09057df3dbcff619eb23cd9ef9dc803c3a36cb78284936`  
		Last Modified: Tue, 30 May 2017 17:05:53 GMT  
		Size: 52.7 MB (52745144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b2c37449f0ea719e2e852aed312ad256f393ed2e46b6f8e06d7c6ce813015`  
		Last Modified: Tue, 30 May 2017 17:05:41 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb25a03c773d9d71b4977532c14de4b0334d22540820fdc98dcf96058216b5d`  
		Last Modified: Tue, 30 May 2017 17:05:40 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
