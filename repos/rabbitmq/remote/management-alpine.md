## `rabbitmq:management-alpine`

```console
$ docker pull rabbitmq@sha256:8b832341851dfdba77e01d451915dd7d2d57108564168da790a3820048fb0015
```

-	Platforms:
	-	linux; amd64

### `rabbitmq:management-alpine` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23034639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1172aa351a53ad2cc9dc014cec164bf570a359eee1c46bf0fdf8e4e7d7a43b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 25 May 2017 23:32:38 GMT
ADD file:df15515197b183747a0b7ccefd75973edc87fc7a5bce30fa10ae94e75928d25c in / 
# Thu, 25 May 2017 23:32:38 GMT
CMD ["/bin/sh"]
# Tue, 30 May 2017 17:42:37 GMT
RUN addgroup -S rabbitmq && adduser -S -h /var/lib/rabbitmq -G rabbitmq rabbitmq
# Tue, 30 May 2017 17:43:21 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 30 May 2017 17:44:08 GMT
RUN apk add --no-cache 		bash 		erlang-asn1 		erlang-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang 		erlang-os-mon 		erlang-public-key 		erlang-sasl 		erlang-ssl 		erlang-syntax-tools 		erlang-xmerl
# Tue, 30 May 2017 17:45:04 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Tue, 30 May 2017 17:45:46 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 30 May 2017 17:49:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 May 2017 17:49:43 GMT
ENV GPG_KEY=0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 30 May 2017 17:50:25 GMT
ENV RABBITMQ_VERSION=3.6.10
# Tue, 30 May 2017 17:51:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gnupg 		libressl 		tar 		xz 	; 		wget -O rabbitmq-server.tar.xz "https://www.rabbitmq.com/releases/rabbitmq-server/v${RABBITMQ_VERSION}/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz"; 	wget -O rabbitmq-server.tar.xz.asc "https://www.rabbitmq.com/releases/rabbitmq-server/v${RABBITMQ_VERSION}/rabbitmq-server-generic-unix-${RABBITMQ_VERSION}.tar.xz.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY"; 	gpg --batch --verify rabbitmq-server.tar.xz.asc rabbitmq-server.tar.xz; 	rm -r "$GNUPGHOME" rabbitmq-server.tar.xz.asc; 		mkdir -p "$RABBITMQ_HOME"; 	tar 		--extract 		--verbose 		--file rabbitmq-server.tar.xz 		--directory "$RABBITMQ_HOME" 		--strip-components 1 	; 	rm rabbitmq-server.tar.xz; 		grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -ri 's!^(SYS_PREFIX=).*$!\1!g' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 		apk del .build-deps
# Tue, 30 May 2017 17:51:29 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 30 May 2017 17:52:12 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq
# Tue, 30 May 2017 17:52:53 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 30 May 2017 17:53:14 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Tue, 30 May 2017 17:53:56 GMT
RUN ln -sf "$RABBITMQ_HOME/plugins" /plugins
# Tue, 30 May 2017 17:54:38 GMT
COPY file:6d5b5641b4ddd6db44e4e5e11ec5ab0346df16687772c50006caf5a342ff05ff in /usr/local/bin/ 
# Tue, 30 May 2017 17:54:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 May 2017 17:55:20 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Tue, 30 May 2017 17:56:03 GMT
CMD ["rabbitmq-server"]
# Tue, 30 May 2017 17:58:25 GMT
RUN rabbitmq-plugins enable --offline rabbitmq_management
# Tue, 30 May 2017 17:58:45 GMT
EXPOSE 15671/tcp 15672/tcp
```

-	Layers:
	-	`sha256:6f821164d5b7ec94868795c1fb8dc6fd7d1fe51e04f97a6cf3a487868f2f5d68`  
		Last Modified: Thu, 25 May 2017 23:36:24 GMT  
		Size: 2.0 MB (1967927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4d31626b4cc745fecb44d4f4d9a435c813c2c849dbcc9a49b2d73e9c23390d`  
		Last Modified: Tue, 30 May 2017 18:05:31 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0a1c444efd570c63e3c0c5b587c3b3dfbca3b87e8ac33431710097d1d953bb`  
		Last Modified: Tue, 30 May 2017 18:05:31 GMT  
		Size: 7.8 KB (7765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7f26d2e4ea099641ab2db1f9cfd0351bf750c1d79a1e861cf1d194f2ec36ed`  
		Last Modified: Tue, 30 May 2017 18:05:33 GMT  
		Size: 16.1 MB (16079815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0afcdcde06c8cd2c5a071e6a2e7bf0e992c0d811562dbd4e82bfa7d20dcab3c`  
		Last Modified: Tue, 30 May 2017 18:05:29 GMT  
		Size: 5.0 MB (4973215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eded4c951133b1f8158c790221e9fb1490ac62f68951956c55f773718d6193a`  
		Last Modified: Tue, 30 May 2017 18:05:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a28c54e2118bd2a706249cf67ef231a617e2b950fc03c0756ea98f00879faa6`  
		Last Modified: Tue, 30 May 2017 18:05:29 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c33ede5ed226518f7d19e45e5520b867820f2daf7a70a373d4f9813d0d33bb`  
		Last Modified: Tue, 30 May 2017 18:05:29 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d0cb4841f683a9174586d6f946beff1a0a26a381f6e7f9f07203659a85fbe`  
		Last Modified: Tue, 30 May 2017 18:05:29 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ed5de78229c61e24e0404fa2793686b94f105bb657242fb225919ee379f3d9`  
		Last Modified: Tue, 30 May 2017 18:08:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
