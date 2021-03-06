## `golang:alpine3.6`

```console
$ docker pull golang@sha256:7d00bea3270139a93b42cce94c656062e2597ad098bf97a6b7a105651c31a7d4
```

-	Platforms:
	-	linux; amd64

### `golang:alpine3.6` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78381407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba50c1102404d4ce7719831ce64a0b81a65cd865961477a8cdc019fbe56dfabc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 25 May 2017 23:33:21 GMT
ADD file:ce33aabbc5f370e58ebe911e081ce093e3df18d689c2d5a5d092c77973f62a54 in / 
# Thu, 25 May 2017 23:33:22 GMT
CMD ["/bin/sh"]
# Wed, 31 May 2017 21:01:30 GMT
RUN apk add --no-cache ca-certificates
# Wed, 31 May 2017 21:04:06 GMT
ENV GOLANG_VERSION=1.8.3
# Wed, 31 May 2017 21:04:08 GMT
COPY file:8bfad5c310fe0639fcf658b30e2f65d04df13ad329573b58a3e782441bb7839c in /go-alpine-patches/ 
# Wed, 31 May 2017 21:05:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GO386="$(go env GO386)" 		GOARM="$(go env GOARM)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '5f5dea2447e7dcfdc50fa6b94c512e58bfba5673c039259fd843f68829d99fa6 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	for p in /go-alpine-patches/*.patch; do 		[ -f "$p" ] || continue; 		patch -p2 -i "$p"; 	done; 	./make.bash; 		rm -rf /go-alpine-patches; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 31 May 2017 21:05:04 GMT
ENV GOPATH=/go
# Wed, 31 May 2017 21:05:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 May 2017 21:05:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 31 May 2017 21:05:07 GMT
WORKDIR /go
# Wed, 31 May 2017 21:05:08 GMT
COPY file:f6191f2c86edc9343569339f101facba47e886e33e29d70da6916ca6b1101a53 in /usr/local/bin/ 
```

-	Layers:
	-	`sha256:2aecc7e1714b6fad58d13aedb0639011b37b86f743ba7b6a52d82bd03014b78e`  
		Last Modified: Thu, 25 May 2017 23:36:54 GMT  
		Size: 2.0 MB (1990101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfa590347bf73375736c6a0b21d00bac38f53bd06fd943c63aca693f3179271`  
		Last Modified: Wed, 31 May 2017 21:09:11 GMT  
		Size: 351.3 KB (351290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b807572434883152f5659e65c3bff1cc5512a79cfb9c1690f05760e3856c13`  
		Last Modified: Wed, 31 May 2017 21:26:45 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe451ec3cdc41acefc5baa02de429251d83045b3700814c67f897036799d9285`  
		Last Modified: Wed, 31 May 2017 21:27:09 GMT  
		Size: 76.0 MB (76038057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d473638cce76e7035abef83d37ff1ba55ae6f76377086f4ff48a4452339cdb9`  
		Last Modified: Wed, 31 May 2017 21:26:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b637a38ceb735ad0252a27881a8e591e7976be91e07992fa302a3647e247e06`  
		Last Modified: Wed, 31 May 2017 21:26:45 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
