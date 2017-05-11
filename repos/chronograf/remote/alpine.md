## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:9e4d53599e9d6baeb8dc8d2786482a67b38d7152713ee95e9b12862a1feefda1
```

-	Platforms:
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7835263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aa34d65cb74e319bd41db68fa9ae12313c5afd930442bcc878d90f4d10ee9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Wed, 12 Apr 2017 18:58:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 12 Apr 2017 19:05:20 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 10 May 2017 02:50:40 GMT
ENV CHRONOGRAF_VERSION=1.3.0
# Wed, 10 May 2017 02:50:49 GMT
RUN apk add --no-cache --virtual .build-deps wget gnupg tar &&     gpg --keyserver hkp://ha.pool.sks-keyservers.net         --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     wget -q https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 10 May 2017 02:50:50 GMT
COPY file:bb4b392707bfb4ca737581b240f672796f5744c7220fea711a5d1f669992b912 in /usr/share/chronograf/LICENSE 
# Wed, 10 May 2017 02:50:51 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 May 2017 02:50:51 GMT
EXPOSE 8888/tcp
# Wed, 10 May 2017 02:50:52 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 May 2017 02:50:53 GMT
COPY file:e80544d3968a14563170636bcb18d09f20de2940dee8d16c52668d53d6d6b8ec in /entrypoint.sh 
# Wed, 10 May 2017 02:50:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2017 02:50:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827570184fa82dc6defc05bcf5838dba590096d8add32bb847191bd7232cfcba`  
		Last Modified: Wed, 12 Apr 2017 19:02:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a07567aee09be1af1aec1476fe3261b0b717c05954d31456c578c63429e532`  
		Last Modified: Wed, 12 Apr 2017 19:06:54 GMT  
		Size: 352.8 KB (352777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01262e45b9a9de688912cc2be9fbb756a10a7d7a71bb195b800f6b99ecaf3e48`  
		Last Modified: Wed, 10 May 2017 02:52:25 GMT  
		Size: 5.6 MB (5552748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7092b32f267176966a17c5e5a43bbeafc3c22fab11f6d0227e3126725f9666c`  
		Last Modified: Wed, 10 May 2017 02:52:24 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e06c37bf927d446f42c8b1d234d1515d3f5d94d1f0dd7ba5326487a40c5a65c`  
		Last Modified: Wed, 10 May 2017 02:52:24 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ee68e6b5e6f4d1a373a82aa7476460bd3bbcbe4e6e58b7ceecde3ba569404b`  
		Last Modified: Wed, 10 May 2017 02:52:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip