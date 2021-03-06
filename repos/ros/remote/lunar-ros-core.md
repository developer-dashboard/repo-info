## `ros:lunar-ros-core`

```console
$ docker pull ros@sha256:fb4629d880fefc6b468a1129be073cfa657c95ff49a32c84015ca15fda39c6ba
```

-	Platforms:
	-	linux; amd64

### `ros:lunar-ros-core` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299441646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270056370cea82c08882691a3b32b41053c050cd6d98ef3301d91a8bd3ca6134`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 15 May 2017 16:43:34 GMT
ADD file:d14b493577228a498919faab376609c73048c0220b06d2989ecaaf1bdc17cf6c in / 
# Mon, 15 May 2017 16:43:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 15 May 2017 16:43:37 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 15 May 2017 16:43:39 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 15 May 2017 16:43:40 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 15 May 2017 16:43:41 GMT
CMD ["/bin/bash"]
# Wed, 24 May 2017 17:39:43 GMT
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 421C365BD9FF1F717815A3895523BAEEB01FA116
# Wed, 24 May 2017 17:40:05 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list
# Wed, 24 May 2017 17:40:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2017 17:40:54 GMT
ENV LANG=C.UTF-8
# Wed, 24 May 2017 17:40:55 GMT
ENV LC_ALL=C.UTF-8
# Wed, 24 May 2017 17:41:08 GMT
RUN rosdep init     && rosdep update
# Wed, 24 May 2017 17:41:20 GMT
ENV ROS_DISTRO=lunar
# Wed, 24 May 2017 17:42:58 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 24 May 2017 17:43:12 GMT
COPY file:824303428ad16ae6296df253434e00a00126dc8404f740a8b885c9f61a2f5fcb in / 
# Wed, 24 May 2017 17:43:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 24 May 2017 17:43:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b6f892c0043b37bd1834a4a1b7d68fe6421c6acbc7e7e63a4527e1d379f92c1b`  
		Last Modified: Fri, 12 May 2017 22:35:01 GMT  
		Size: 46.9 MB (46893344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55010f332b047687e081a9639fac04918552c144bc2da4edb3422ce8efcc1fb1`  
		Last Modified: Mon, 15 May 2017 16:49:04 GMT  
		Size: 816.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2955fb827c947b782af190a759805d229cfebc75978dba2d01b4a59e6a333845`  
		Last Modified: Mon, 15 May 2017 16:49:05 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deef3fcbd3072b45771bd0d192d4e5ff2b7310b99ea92bce062e01097953505`  
		Last Modified: Mon, 15 May 2017 16:49:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9722e506aada1109f5c00a9ba542a81c9e109606c01c81f5991b1f93de7b66`  
		Last Modified: Mon, 15 May 2017 16:49:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a888df954433da8e538333503c3a3142359dd8b812e77cfc8347c1afc41835`  
		Last Modified: Wed, 24 May 2017 18:20:59 GMT  
		Size: 13.1 KB (13079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4421b4fe281c38da3393d8b6e157d13ec628139c0b907733d2971401d6fd3782`  
		Last Modified: Wed, 24 May 2017 18:20:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354e3e5f562a3e058acd5644d0238b40b3c64f2a315f78d65a298688139681c6`  
		Last Modified: Wed, 24 May 2017 18:21:29 GMT  
		Size: 58.8 MB (58779580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecf6e9dacca1f956b752d6811bc007d41a10fd73ca60dd9b56caa9a567389d4`  
		Last Modified: Wed, 24 May 2017 18:20:59 GMT  
		Size: 711.1 KB (711060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744ce0af0642f091d719c949000088cc3fab0ad4baf4c58bdb3c44829ee2e350`  
		Last Modified: Wed, 24 May 2017 18:22:02 GMT  
		Size: 193.0 MB (193041822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36d3cb3ce89a9ae95dc982242dafedc98d15d52df57f81ac787929414ed10ba`  
		Last Modified: Wed, 24 May 2017 18:20:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
