## `docker:rc-git`

```console
$ docker pull docker@sha256:07bc77166c9835b6121f9b1ecd07ebe521d5c5871574d610cae76805fec1edd0
```

-	Platforms:
	-	linux; amd64

### `docker:rc-git` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44051450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a01ed6de4d83f949d4dbb0c8f51023de63fc482bafaf40abc893a975691bd35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 25 May 2017 23:33:21 GMT
ADD file:ce33aabbc5f370e58ebe911e081ce093e3df18d689c2d5a5d092c77973f62a54 in / 
# Thu, 25 May 2017 23:33:22 GMT
CMD ["/bin/sh"]
# Wed, 31 May 2017 20:08:42 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 31 May 2017 20:08:43 GMT
ENV DOCKER_CHANNEL=test
# Wed, 31 May 2017 20:08:44 GMT
ENV DOCKER_VERSION=17.06.0-ce-rc1
# Wed, 31 May 2017 20:08:52 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		curl 		tar 	; 	curl -fL -o docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/x86_64/docker-${DOCKER_VERSION}.tgz"; 	tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 	apk del .fetch-deps; 	dockerd -v; 	docker -v
# Wed, 31 May 2017 20:09:09 GMT
COPY file:a8b1446f032ff01ac092c29a0af328f0b9d47bbee72d1049499f2a9a89ee988a in /usr/local/bin/ 
# Wed, 31 May 2017 20:09:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 May 2017 20:09:11 GMT
CMD ["sh"]
# Wed, 31 May 2017 20:10:40 GMT
RUN apk add --no-cache 		git 		openssh-client
```

-	Layers:
	-	`sha256:2aecc7e1714b6fad58d13aedb0639011b37b86f743ba7b6a52d82bd03014b78e`  
		Last Modified: Thu, 25 May 2017 23:36:54 GMT  
		Size: 2.0 MB (1990101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfd12279b0d11f205f37f642e15d7328cc23431b4c09a2672b941d67e40685f`  
		Last Modified: Wed, 31 May 2017 20:20:51 GMT  
		Size: 351.3 KB (351277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5075090d89604eb77aeb6fd33351df4b61d98974fa04257438a6957c71c33e9`  
		Last Modified: Wed, 31 May 2017 20:21:02 GMT  
		Size: 30.0 MB (29976920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1011761623a9f800af8b5c32029f1bf657de4191dcd1ee581edf4eb52540a570`  
		Last Modified: Wed, 31 May 2017 20:20:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a686fa10eb52a95055783c21e55dbadc89d6528f3622311a2ef9711262f552`  
		Last Modified: Wed, 31 May 2017 20:28:14 GMT  
		Size: 11.7 MB (11732662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
