## `docker:rc-dind`

```console
$ docker pull docker@sha256:9e82bbf4053ebd0e4157d7ef41cd03f22d77d0febc5c99164c30420438e8ca61
```

-	Platforms:
	-	linux; amd64

### `docker:rc-dind` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34705736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3db18d7e67232db374c859c3357f4ef8c6c97721661fc221fb4d8e2389893cb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

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
# Wed, 31 May 2017 20:09:39 GMT
RUN apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		xfsprogs 		xz
# Wed, 31 May 2017 20:09:41 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 31 May 2017 20:10:01 GMT
ENV DIND_COMMIT=3b5fac462d21ca164b3778647420016315289034
# Wed, 31 May 2017 20:10:06 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps libressl; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind; 	apk del .fetch-deps
# Wed, 31 May 2017 20:10:07 GMT
COPY file:7070e4b35c137a8ec5904300d19b8f7ee74aa76659517767c617249cece98a4a in /usr/local/bin/ 
# Wed, 31 May 2017 20:10:08 GMT
VOLUME [/var/lib/docker]
# Wed, 31 May 2017 20:10:10 GMT
EXPOSE 2375/tcp
# Wed, 31 May 2017 20:10:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 31 May 2017 20:10:11 GMT
CMD []
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
	-	`sha256:4b034f56bd89a27392b5616c4486c4b2f6c4fe0f47885b95b29a16c75441ac8f`  
		Last Modified: Wed, 31 May 2017 20:23:59 GMT  
		Size: 2.2 MB (2209037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c766dfb0ad5ea046adc00e1ce269c82c0874cd813b1446ef566257fc01b16124`  
		Last Modified: Wed, 31 May 2017 20:23:58 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb7fea7d770e4118bf71cd42cabc5d3a046c85c9dd2703b2f16a684e3e0054d`  
		Last Modified: Wed, 31 May 2017 20:23:58 GMT  
		Size: 176.1 KB (176123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98089e303f413d6fa88edd3f2e48b256260e1cbd2a4aafa5a3d0d37e37b870e3`  
		Last Modified: Wed, 31 May 2017 20:23:59 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
