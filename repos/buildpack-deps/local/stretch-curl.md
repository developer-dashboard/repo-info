# `buildpack-deps:stretch-curl`

## Docker Metadata

- Image ID: `sha256:444acb4af228415feeed8cc2cbc031a27f0e6f5b96c3238e533a6687fc59a50c`
- Created: `2017-05-09T00:00:54.65451859Z`
- Virtual Size: ~ 163.08 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.2.52-3`

Binary Packages:

- `libacl1:amd64=2.2.52-3+b1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.2.52-3
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.2.52-3.dsc' acl_2.2.52-3.dsc 2025 SHA256:82e344b9ab176559a85630b74ee5a68d678d7f24b6fe8139f2fd9fcf38a48095
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.2.52.orig.tar.bz2' acl_2.2.52.orig.tar.bz2 312128 SHA256:59d05b38af76baf2eddccbf08c7968a17451cc785ffecc657fcb46ce32b2631d
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.2.52-3.debian.tar.xz' acl_2.2.52-3.debian.tar.xz 8740 SHA256:fc3f1178d18288993fc4ce4853b7f9dcdf0bd1fd26e4f69349a4e4e5916d1fa8
```

Likely also available for browsing at:

- https://sources.debian.net/src/acl/2.2.52-3/
- https://sources.debian.net/src/acl/2.2.52-3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `adduser=3.115`

Binary Packages:

- `adduser=3.115`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.115
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.115.dsc' adduser_3.115.dsc 1701 SHA256:754698aa19d7521080ecacc8033baa20cfa4a963021de6061c68ffa6ee15e9a1
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.115.tar.xz' adduser_3.115.tar.xz 213620 SHA256:e7288281d4d1eec2948ba3687452ca33a8224d40c98d321bc3fbaefcf6d4c0db
```

Likely also available for browsing at:

- https://sources.debian.net/src/adduser/3.115/
- https://sources.debian.net/src/adduser/3.115/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `apt=1.4.1`

Binary Packages:

- `apt=1.4.1`
- `libapt-pkg5.0:amd64=1.4.1`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg5.0/copyright`)

- `GPL-2`
- `GPLv2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `attr=1:2.4.47-2`

Binary Packages:

- `libattr1:amd64=1:2.4.47-2+b2`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.4.47-2
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.4.47-2.dsc' attr_2.4.47-2.dsc 2027 SHA256:ee842d6d62d473acf02b494c432cf33128fa46455a09d3172c77c252449fa1a6
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.4.47.orig.tar.bz2' attr_2.4.47.orig.tar.bz2 281877 SHA256:6c1208035757f5ce9b516402dd45b8299a53ae4d69ad2c352116f9cb8d7bc274
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.4.47-2.debian.tar.xz' attr_2.4.47-2.debian.tar.xz 8096 SHA256:f65909562def601b1556393f5656032c058dc574ba622414ad3eb80c7b05a42a
```

Likely also available for browsing at:

- https://sources.debian.net/src/attr/1:2.4.47-2/
- https://sources.debian.net/src/attr/1:2.4.47-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `audit=1:2.6.7-2`

Binary Packages:

- `libaudit-common=1:2.6.7-2`
- `libaudit1:amd64=1:2.6.7-2`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:2.6.7-2
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.6.7-2.dsc' audit_2.6.7-2.dsc 2485 SHA256:3cc48a56a06f29cff62d35267471d1775a5b201cd947385566fc8f8d49bc1280
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.6.7.orig.tar.gz' audit_2.6.7.orig.tar.gz 1080848 SHA256:8923917332daa7833bbc0c1d9eb012167093fbad000da4a9630fb3356aff8cdc
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.6.7-2.debian.tar.xz' audit_2.6.7-2.debian.tar.xz 18820 SHA256:04b40b6ae73625c6a27a9949b28c751a83c97220f59a712b2ea9c03f5cab0fcf
```

Likely also available for browsing at:

- https://sources.debian.net/src/audit/1:2.6.7-2/
- https://sources.debian.net/src/audit/1:2.6.7-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `base-files=9.9`

Binary Packages:

- `base-files=9.9`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=9.9
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_9.9.dsc' base-files_9.9.dsc 1067 SHA256:4ae5728880b81789ae95f0aca8f630d51c4b894e00c4b0e8bfc7c3ebabb595d1
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_9.9.tar.xz' base-files_9.9.tar.xz 62840 SHA256:c941e091eea9d2949b6ed3b8d37ea1d086b50b10d564103d52fafcd129ac1931
```

Likely also available for browsing at:

- https://sources.debian.net/src/base-files/9.9/
- https://sources.debian.net/src/base-files/9.9/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `base-passwd=3.5.43`

Binary Packages:

- `base-passwd=3.5.43`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `PD`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.5.43
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.5.43.dsc' base-passwd_3.5.43.dsc 1749 SHA256:174a03d0df0d0f36cc186592e36472339632de094d60f9fcab370e1101a2430d
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.5.43.tar.xz' base-passwd_3.5.43.tar.xz 52596 SHA256:7768d10e2c08469cc81342e391e059f0426afdb6eb74a3102beef59ac45ab994
```

Likely also available for browsing at:

- https://sources.debian.net/src/base-passwd/3.5.43/
- https://sources.debian.net/src/base-passwd/3.5.43/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `bash=4.4-4`

Binary Packages:

- `bash=4.4-4+b2`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `bzip2=1.0.6-8.1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.6-8.1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.6-8.1
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6-8.1.dsc' bzip2_1.0.6-8.1.dsc 2082 SHA256:d80deed11a1419ad090cb486dd2335850fd8719b809c32002dea04b485f55dbd
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6.orig.tar.bz2' bzip2_1.0.6.orig.tar.bz2 708737 SHA256:d70a9ccd8bdf47e302d96c69fecd54925f45d9c7b966bb4ef5f56b770960afa7
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6-8.1.debian.tar.bz2' bzip2_1.0.6-8.1.debian.tar.bz2 59875 SHA256:bdbe7bf29e014e44d79bb7c733fe63cae990ab50882a4a07867cf69c61ad72b7
```

Likely also available for browsing at:

- https://sources.debian.net/src/bzip2/1.0.6-8.1/
- https://sources.debian.net/src/bzip2/1.0.6-8.1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `ca-certificates=20161130`

Binary Packages:

- `ca-certificates=20161130`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20161130
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20161130.dsc' ca-certificates_20161130.dsc 1506 SHA256:bbba50a4391b33d8f5c8db97e4f077d861ff9f95cc6a3f45ca43fc5be6536617
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20161130.tar.xz' ca-certificates_20161130.tar.xz 298656 SHA256:04bca9e142a90a834aca0311f7ced237368d71fee7bd5c9f68ef7f4611aee471
```

Likely also available for browsing at:

- https://sources.debian.net/src/ca-certificates/20161130/
- https://sources.debian.net/src/ca-certificates/20161130/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `cdebconf=0.227`

Binary Packages:

- `libdebconfclient0:amd64=0.227`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.227
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.227.dsc' cdebconf_0.227.dsc 2662 SHA256:23531e6cbf4acb4edc5a2c3eda7a5095b82c396d801ade72d669b6fcf2c5aaa2
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.227.tar.xz' cdebconf_0.227.tar.xz 272716 SHA256:df2092bb5d4fe76c318adfd1cc756f78b48a668704b6e71e161143e7c782da58
```

Likely also available for browsing at:

- https://sources.debian.net/src/cdebconf/0.227/
- https://sources.debian.net/src/cdebconf/0.227/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `coreutils=8.26-3`

Binary Packages:

- `coreutils=8.26-3`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris coreutils=8.26-3
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_8.26-3.dsc' coreutils_8.26-3.dsc 1955 SHA256:f62ab642e46e02c470cc045316643de530a0be50446151a5e449ca12da6485c4
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_8.26.orig.tar.xz' coreutils_8.26.orig.tar.xz 5810244 SHA256:155e94d748f8e2bc327c66e0cbebdb8d6ab265d2f37c3c928f7bf6c3beba9a8e
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_8.26-3.debian.tar.xz' coreutils_8.26-3.debian.tar.xz 22392 SHA256:cef6a15eb95d9e7bc992bca95010bc5ea9e25e98d8f4f668a698eee534d14b93
```

Likely also available for browsing at:

- https://sources.debian.net/src/coreutils/8.26-3/
- https://sources.debian.net/src/coreutils/8.26-3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `curl=7.52.1-5`

Binary Packages:

- `curl=7.52.1-5`
- `libcurl3:amd64=7.52.1-5`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3/copyright`)

- `BSD-3-Clause`
- `BSD-4-Clause`
- `ISC`
- `curl`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris curl=7.52.1-5
'http://deb.debian.org/debian/pool/main/c/curl/curl_7.52.1-5.dsc' curl_7.52.1-5.dsc 2765 SHA256:40e5e7c680d0246e12bdebf4f84949412c7846d95708c688df9dd7e77119960e
'http://deb.debian.org/debian/pool/main/c/curl/curl_7.52.1.orig.tar.gz' curl_7.52.1.orig.tar.gz 3504621 SHA256:a8984e8b20880b621f61a62d95ff3c0763a3152093a9f9ce4287cfd614add6ae
'http://deb.debian.org/debian/pool/main/c/curl/curl_7.52.1-5.debian.tar.xz' curl_7.52.1-5.debian.tar.xz 33004 SHA256:67e9388c5562edbdd63fa31a892d446bd7dee18207a62ec367bc925f6ce50fcf
```

Likely also available for browsing at:

- https://sources.debian.net/src/curl/7.52.1-5/
- https://sources.debian.net/src/curl/7.52.1-5/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `cyrus-sasl2=2.1.27~101-g0780600+dfsg-3`

Binary Packages:

- `libsasl2-2:amd64=2.1.27~101-g0780600+dfsg-3`
- `libsasl2-modules-db:amd64=2.1.27~101-g0780600+dfsg-3`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.27~101-g0780600+dfsg-3
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.dsc' cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.dsc 3176 SHA256:abc0b2b0e8757195689821a724037c2017f8d06d63d357e1663d679226ef71d4
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg.orig.tar.xz' cyrus-sasl2_2.1.27~101-g0780600+dfsg.orig.tar.xz 1143888 SHA256:69f34971f768e7ee6a6b647ec2d16a5a72a854ecd4602b019d5f79ba61063fdc
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.debian.tar.xz' cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.debian.tar.xz 94664 SHA256:5094c002044588381e417c112f0f85d33242651f2739783b4dbd673321e7a386
```

Likely also available for browsing at:

- https://sources.debian.net/src/cyrus-sasl2/2.1.27~101-g0780600+dfsg-3/
- https://sources.debian.net/src/cyrus-sasl2/2.1.27~101-g0780600+dfsg-3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `dash=0.5.8-2.4`

Binary Packages:

- `dash=0.5.8-2.4`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.8-2.4
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.8-2.4.dsc' dash_0.5.8-2.4.dsc 1461 SHA256:c83f68c3727e9fd3691117d1f67a2bd049ae2411d2137d50ea6d36122cec6482
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.8.orig.tar.gz' dash_0.5.8.orig.tar.gz 223028 SHA256:c6db3a237747b02d20382a761397563d813b306c020ae28ce25a1c3915fac60f
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.8-2.4.diff.gz' dash_0.5.8-2.4.diff.gz 44058 SHA256:230717c04af659a6a09b2c39158d9167fdd3392a6716c0ff36fe40dff1ca8b9d
```

Likely also available for browsing at:

- https://sources.debian.net/src/dash/0.5.8-2.4/
- https://sources.debian.net/src/dash/0.5.8-2.4/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `db5.3=5.3.28-12`

Binary Packages:

- `libdb5.3:amd64=5.3.28-12+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28-12
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28-12.dsc' db5.3_5.3.28-12.dsc 3199 SHA256:1c4d6149f83a798e69f6d8e7444711d963c31d649284357135ea33b319c71bba
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28.orig.tar.xz' db5.3_5.3.28.orig.tar.xz 24154920 SHA256:e1f85c8b6ebd0ed3ca72fa0ae97b65006f6d0bd0cd6f4ac24bed103cb5497bf5
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28-12.debian.tar.xz' db5.3_5.3.28-12.debian.tar.xz 27812 SHA256:7907d8ad4c408857a71782436283a7ab67d7fe0f38ae15782f08077bdfd55c03
```

Likely also available for browsing at:

- https://sources.debian.net/src/db5.3/5.3.28-12/
- https://sources.debian.net/src/db5.3/5.3.28-12/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `debconf=1.5.60`

Binary Packages:

- `debconf=1.5.60`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `debian-archive-keyring=2014.3`

Binary Packages:

- `debian-archive-keyring=2014.3`

Licenses: (parsed from: `/usr/share/doc/debian-archive-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debian-archive-keyring=2014.3
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2014.3.dsc' debian-archive-keyring_2014.3.dsc 1597 SHA256:2a3e604f936b8fbaf1beeea0a7611a1a88cacffd26571df4cc58c16ecefa362a
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2014.3.tar.xz' debian-archive-keyring_2014.3.tar.xz 61380 SHA256:46be978ec2f72b0277d9e71bda30ea1b2b9aa00b1952cb35e8b22a2c016f5e22
```

Likely also available for browsing at:

- https://sources.debian.net/src/debian-archive-keyring/2014.3/
- https://sources.debian.net/src/debian-archive-keyring/2014.3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `debianutils=4.8.1`

Binary Packages:

- `debianutils=4.8.1`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debianutils=4.8.1
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_4.8.1.dsc' debianutils_4.8.1.dsc 1693 SHA256:0f187e087a9c96a70e672f58fa324d4b65f60f1e13ee8219de7e58f061ae7c9e
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_4.8.1.tar.xz' debianutils_4.8.1.tar.xz 156072 SHA256:2c395c0bdcfe89de30828b1d25cc5549ded5225a6d3625fbcb2cc0881ef5f026
```

Likely also available for browsing at:

- https://sources.debian.net/src/debianutils/4.8.1/
- https://sources.debian.net/src/debianutils/4.8.1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `diffutils=1:3.5-3`

Binary Packages:

- `diffutils=1:3.5-3`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.5-3
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.5-3.dsc' diffutils_3.5-3.dsc 1453 SHA256:8b8e4d9d48ab35fd2c5759a3d0854e7d85c33b3fa09a185c20865793090feff9
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.5.orig.tar.xz' diffutils_3.5.orig.tar.xz 1360996 SHA256:dad398ccd5b9faca6b0ab219a036453f62a602a56203ac659b43e889bec35533
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.5-3.debian.tar.xz' diffutils_3.5-3.debian.tar.xz 10796 SHA256:5c8464482951de1dcf3c1c53643cd7d0939cd8f7568a7ef84982d368c5cb6695
```

Likely also available for browsing at:

- https://sources.debian.net/src/diffutils/1:3.5-3/
- https://sources.debian.net/src/diffutils/1:3.5-3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `dpkg=1.18.23`

Binary Packages:

- `dpkg=1.18.23`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain-md5`
- `public-domain-s-s-d`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `e2fsprogs=1.43.4-2`

Binary Packages:

- `e2fslibs:amd64=1.43.4-2`
- `e2fsprogs=1.43.4-2`
- `libcomerr2:amd64=1.43.4-2`
- `libss2:amd64=1.43.4-2`

Licenses: (parsed from: `/usr/share/doc/e2fslibs/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcomerr2/copyright`, `/usr/share/doc/libss2/copyright`)

- `GPL-2`
- `LGPL-2`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.43.4-2
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.4-2.dsc' e2fsprogs_1.43.4-2.dsc 2043 SHA256:e6f6b8dddeb97cc81c3aa7aa826305e1f9c9cd1c3066b2b916e558682fdc7f70
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.4.orig.tar.gz' e2fsprogs_1.43.4.orig.tar.gz 7552218 SHA256:484ab0bc1bc07c64267b18cfe7871b6b975bf0a705c5a4563001f035071cdc7c
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.4-2.debian.tar.xz' e2fsprogs_1.43.4-2.debian.tar.xz 76444 SHA256:e1713f9e686a71a9d6f119cd178c4ebea502a7c2b43901cc41bcdb61b142b1c8
```

Likely also available for browsing at:

- https://sources.debian.net/src/e2fsprogs/1.43.4-2/
- https://sources.debian.net/src/e2fsprogs/1.43.4-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `elfutils=0.168-0.2`

Binary Packages:

- `libelf1:amd64=0.168-0.2`

Licenses: (parsed from: `/usr/share/doc/libelf1/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-`

Source:

```console
$ apt-get source -qq --print-uris elfutils=0.168-0.2
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.168-0.2.dsc' elfutils_0.168-0.2.dsc 2332 SHA256:55e6a746a00cdcef3c389f2caa09e6b6c82b888d3182ee5bfd63df3413431796
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.168.orig.tar.bz2' elfutils_0.168.orig.tar.bz2 6840399 SHA256:b88d07893ba1373c7dd69a7855974706d05377766568a7d9002706d5de72c276
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.168-0.2.debian.tar.xz' elfutils_0.168-0.2.debian.tar.xz 36564 SHA256:8998c51b202ed2efc7b9a3906f0926b8f350b0e0071cf86bb9c06a3aa6d3864e
```

Likely also available for browsing at:

- https://sources.debian.net/src/elfutils/0.168-0.2/
- https://sources.debian.net/src/elfutils/0.168-0.2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `findutils=4.6.0+git+20161106-2`

Binary Packages:

- `findutils=4.6.0+git+20161106-2`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `GFDL-1.3`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris findutils=4.6.0+git+20161106-2
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.6.0+git+20161106-2.dsc' findutils_4.6.0+git+20161106-2.dsc 2220 SHA256:f92d95f03e56357bb72e897f4d8b363995f280cfdf6dedfabdec3164f3a7651a
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.6.0+git+20161106.orig.tar.xz' findutils_4.6.0+git+20161106.orig.tar.xz 1828956 SHA256:96a3aa120d7300863f39fe56ccb6674d8cde4730b485f4f81083c1a6d33097e3
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.6.0+git+20161106-2.debian.tar.xz' findutils_4.6.0+git+20161106-2.debian.tar.xz 26812 SHA256:aca885ac24582f5c393dbbfa362264712ee4922da0ff7aa1fc602e629c89b71b
```

Likely also available for browsing at:

- https://sources.debian.net/src/findutils/4.6.0+git+20161106-2/
- https://sources.debian.net/src/findutils/4.6.0+git+20161106-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `gcc-6=6.3.0-16`

Binary Packages:

- `gcc-6-base:amd64=6.3.0-16`
- `libgcc1:amd64=1:6.3.0-16`
- `libstdc++6:amd64=6.3.0-16`

Licenses: (parsed from: `/usr/share/doc/gcc-6-base/copyright`, `/usr/share/doc/libgcc1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `gdbm=1.8.3-14`

Binary Packages:

- `libgdbm3:amd64=1.8.3-14`

Licenses: (parsed from: `/usr/share/doc/libgdbm3/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.8.3-14
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.8.3-14.dsc' gdbm_1.8.3-14.dsc 1841 SHA256:312d3d28e287d287ee66e8ae3f25769676b1680ec1adc8c0815b5e9808405b13
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.8.3.orig.tar.bz2' gdbm_1.8.3.orig.tar.bz2 172796 SHA256:1d5995b6e9e6be4ff62c8126d019f184a083dd8e6f75f6c74b9fe023b5b9440e
'http://deb.debian.org/debian/pool/main/g/gdbm/gdbm_1.8.3-14.debian.tar.xz' gdbm_1.8.3-14.debian.tar.xz 15308 SHA256:1c0570dd53947ea5980111f51b67356d647c4f21c502443b02397041dde0bf31
```

Likely also available for browsing at:

- https://sources.debian.net/src/gdbm/1.8.3-14/
- https://sources.debian.net/src/gdbm/1.8.3-14/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `glibc=2.24-10`

Binary Packages:

- `libc-bin=2.24-10`
- `libc6:amd64=2.24-10`
- `multiarch-support=2.24-10`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/multiarch-support/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.24-10
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.24-10.dsc' glibc_2.24-10.dsc 8355 SHA256:bc3eecc0bc562837941133cd3a71f3055c13d43cd49fd326bd0575fcf6b09625
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.24.orig.tar.xz' glibc_2.24.orig.tar.xz 13921912 SHA256:ed71e8afd2b270f7947a2cea2457a31e1ca4fac08e2731d80edd7ec1730ec84f
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.24-10.debian.tar.xz' glibc_2.24-10.debian.tar.xz 987372 SHA256:4b3789ce164d3b7fb7d01cdfb967a84bcbf4369c4570e201dff37432c8e2dd67
```

Likely also available for browsing at:

- https://sources.debian.net/src/glibc/2.24-10/
- https://sources.debian.net/src/glibc/2.24-10/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `gmp=2:6.1.2+dfsg-1`

Binary Packages:

- `libgmp10:amd64=2:6.1.2+dfsg-1`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris gmp=2:6.1.2+dfsg-1
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.1.2+dfsg-1.dsc' gmp_6.1.2+dfsg-1.dsc 2183 SHA256:3a53f6c74c9b2465c1c61446aa9bdc6182fdec8b04075849d4cbf224a73b6fbe
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.1.2+dfsg.orig.tar.xz' gmp_6.1.2+dfsg.orig.tar.xz 1804424 SHA256:18016f718f621e7641ddd4e57f8e140391c5183252e5998263ffff59198a65b7
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.1.2+dfsg-1.debian.tar.xz' gmp_6.1.2+dfsg-1.debian.tar.xz 20652 SHA256:79e73f74197e7628b2f0c02edf01b6eea3716c13152044ed8e0e0ee4178394df
```

Likely also available for browsing at:

- https://sources.debian.net/src/gmp/2:6.1.2+dfsg-1/
- https://sources.debian.net/src/gmp/2:6.1.2+dfsg-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `gnupg2=2.1.18-6`

Binary Packages:

- `gpgv=2.1.18-6`

Licenses: (parsed from: `/usr/share/doc/gpgv/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `RFC-Reference`
- `TinySCHEME`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris gnupg2=2.1.18-6
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.1.18-6.dsc' gnupg2_2.1.18-6.dsc 3148 SHA256:a7b69e22c8de6637ce4e267907ac13bd5144c1abf010ad33d8f48b9c9839bbe8
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.1.18.orig.tar.bz2' gnupg2_2.1.18.orig.tar.bz2 6308666 SHA256:d04c6fab7e5562ce4b915b22020e34d4c1a256847690cf149842264fc7cef994
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.1.18-6.debian.tar.bz2' gnupg2_2.1.18-6.debian.tar.bz2 67292 SHA256:fc8a74741a0383afcc8abef63a9449750c99051eb8b6e841e5aae62a2976969f
```

Likely also available for browsing at:

- https://sources.debian.net/src/gnupg2/2.1.18-6/
- https://sources.debian.net/src/gnupg2/2.1.18-6/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `gnutls28=3.5.8-5`

Binary Packages:

- `libgnutls30:amd64=3.5.8-5`

Licenses: (parsed from: `/usr/share/doc/libgnutls30/copyright`)

- `CC0 license`
- `GFDL-1.3`
- `GPL`
- `GPL-3`
- `LGPL`
- `LGPL-3`
- `LGPL2.1`
- `The MIT License (MIT)`
- `The main library is licensed under GNU Lesser`

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.5.8-5
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.5.8-5.dsc' gnutls28_3.5.8-5.dsc 3258 SHA256:1609d51af0485c909648209e36d7b2d256680f617d1ce122e3687aeaf56e1266
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.5.8.orig.tar.xz' gnutls28_3.5.8.orig.tar.xz 7264448 SHA256:0e97f243ae72b70307d684b84c7fe679385aa7a7a0e37e5be810193dcc17d4ff
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.5.8.orig.tar.xz.asc' gnutls28_3.5.8.orig.tar.xz.asc 287 SHA256:417da9db564a841128edb2dc2c98465a5749541f7d71492cb7c4905a0bfeac82
'http://deb.debian.org/debian/pool/main/g/gnutls28/gnutls28_3.5.8-5.debian.tar.xz' gnutls28_3.5.8-5.debian.tar.xz 104860 SHA256:db08c67dd060c6c921026e0c4446d7168748b7972bafa593109ed6409c754081
```

Likely also available for browsing at:

- https://sources.debian.net/src/gnutls28/3.5.8-5/
- https://sources.debian.net/src/gnutls28/3.5.8-5/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `grep=2.27-2`

Binary Packages:

- `grep=2.27-2`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=2.27-2
'http://deb.debian.org/debian/pool/main/g/grep/grep_2.27-2.dsc' grep_2.27-2.dsc 2053 SHA256:c048a1ad8c39877c2fb0279887c8ea93e59591788fdb08e2f75249ebdcecdea7
'http://deb.debian.org/debian/pool/main/g/grep/grep_2.27.orig.tar.xz' grep_2.27.orig.tar.xz 1360388 SHA256:ad4cc44d23074a1c3a8baae8fbafff2a8c60f38a9a6108f985eef6fbee6dcaeb
'http://deb.debian.org/debian/pool/main/g/grep/grep_2.27-2.debian.tar.bz2' grep_2.27-2.debian.tar.bz2 112728 SHA256:445eaf71811df5ca18242fb5adc417d35e349e49810201977bf7086746b967f4
```

Likely also available for browsing at:

- https://sources.debian.net/src/grep/2.27-2/
- https://sources.debian.net/src/grep/2.27-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `gzip=1.6-5`

Binary Packages:

- `gzip=1.6-5+b1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.6-5
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.6-5.dsc' gzip_1.6-5.dsc 1867 SHA256:922751ee5fc426d623e824c55f7822fa60f26f35b5389b37c8b15feff639608c
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.6.orig.tar.gz' gzip_1.6.orig.tar.gz 1074924 SHA256:97eb83b763d9e5ad35f351fe5517e6b71521d7aac7acf3e3cacdb6b1496d8f7e
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.6-5.debian.tar.xz' gzip_1.6-5.debian.tar.xz 14684 SHA256:ac5282c32083ff58fc01317ee402b687b3806555aa1d4e80a62bb0f2ad93167e
```

Likely also available for browsing at:

- https://sources.debian.net/src/gzip/1.6-5/
- https://sources.debian.net/src/gzip/1.6-5/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `hostname=3.18`

Binary Packages:

- `hostname=3.18+b1`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.18
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.18.dsc' hostname_3.18.dsc 1446 SHA256:4d3d5c8ded08ffc2ebfb39817ba1994b5fc1966652b132ff3e16389b70af28d7
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.18.tar.gz' hostname_3.18.tar.gz 13732 SHA256:5cc3ec120967b8f911e86b9561b53977bcc77191c84fe9c607177ccd09f8d207
```

Likely also available for browsing at:

- https://sources.debian.net/src/hostname/3.18/
- https://sources.debian.net/src/hostname/3.18/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `inetutils=2:1.9.4-2`

Binary Packages:

- `inetutils-ping=2:1.9.4-2+b1`

Licenses: (parsed from: `/usr/share/doc/inetutils-ping/copyright`)

- `BSD-3-clause`
- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL-3`
- `GPL-3+`
- `MIT`
- `Wietse`

Source:

```console
$ apt-get source -qq --print-uris inetutils=2:1.9.4-2
'http://deb.debian.org/debian/pool/main/i/inetutils/inetutils_1.9.4-2.dsc' inetutils_1.9.4-2.dsc 2662 SHA256:bd38f1018bbb697b6e27235a804f742a7bcd5fffb736479e8084f5214ed45669
'http://deb.debian.org/debian/pool/main/i/inetutils/inetutils_1.9.4.orig.tar.xz' inetutils_1.9.4.orig.tar.xz 1364408 SHA256:849d96f136effdef69548a940e3e0ec0624fc0c81265296987986a0dd36ded37
'http://deb.debian.org/debian/pool/main/i/inetutils/inetutils_1.9.4-2.debian.tar.xz' inetutils_1.9.4-2.debian.tar.xz 77188 SHA256:1b67e9197c4205b36e7b05e07eedaf44f9b3971f03ab83b7fed279a692d93a98
```

Likely also available for browsing at:

- https://sources.debian.net/src/inetutils/2:1.9.4-2/
- https://sources.debian.net/src/inetutils/2:1.9.4-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `init-system-helpers=1.48`

Binary Packages:

- `init-system-helpers=1.48`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.48
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.48.dsc' init-system-helpers_1.48.dsc 1916 SHA256:aefcef5270cfae3380f9dfd98336de20580086dbdc65c0dfd7fe1c10f0722bd0
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.48.tar.xz' init-system-helpers_1.48.tar.xz 43384 SHA256:20b4ff9df037cfa64d6c9637e383cb09135cb97114d932032160cdfaf01d08b8
```

Likely also available for browsing at:

- https://sources.debian.net/src/init-system-helpers/1.48/
- https://sources.debian.net/src/init-system-helpers/1.48/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `iproute2=4.9.0-1`

Binary Packages:

- `iproute2=4.9.0-1`

Licenses: (parsed from: `/usr/share/doc/iproute2/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris iproute2=4.9.0-1
'http://deb.debian.org/debian/pool/main/i/iproute2/iproute2_4.9.0-1.dsc' iproute2_4.9.0-1.dsc 2397 SHA256:30ead60a56ff3d3a2ba61079790292952d66b5a74b1685133b7a69ef14a82e2e
'http://deb.debian.org/debian/pool/main/i/iproute2/iproute2_4.9.0.orig.tar.xz' iproute2_4.9.0.orig.tar.xz 613032 SHA256:c0f30f043f7767cc1b2cd2197b08d4e9b2392c95823fabe30bbce308c30116c4
'http://deb.debian.org/debian/pool/main/i/iproute2/iproute2_4.9.0-1.debian.tar.xz' iproute2_4.9.0-1.debian.tar.xz 26752 SHA256:1926348d3c8c9e90f7826f5d409d5dc17a2cbf5d247206f1bc4b9a584c672be2
```

Likely also available for browsing at:

- https://sources.debian.net/src/iproute2/4.9.0-1/
- https://sources.debian.net/src/iproute2/4.9.0-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `keyutils=1.5.9-9`

Binary Packages:

- `libkeyutils1:amd64=1.5.9-9`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.5.9-9
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.5.9-9.dsc' keyutils_1.5.9-9.dsc 2033 SHA256:5fe3b2578a7ec662b7f495b11b7d861c3ee68c9550d4dec20c10ff4f3b3ca3dd
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.5.9.orig.tar.bz2' keyutils_1.5.9.orig.tar.bz2 74683 SHA256:4da2c5552c688b65ab14d4fd40fbdf720c8b396d8ece643e040cf6e707e083ae
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.5.9-9.debian.tar.xz' keyutils_1.5.9-9.debian.tar.xz 17588 SHA256:2e9db3f51d902a4d8fa4bef3b914353f9f83ed53b9003f24b5fc44748f4d6d80
```

Likely also available for browsing at:

- https://sources.debian.net/src/keyutils/1.5.9-9/
- https://sources.debian.net/src/keyutils/1.5.9-9/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `krb5=1.15-1`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.15-1`
- `libk5crypto3:amd64=1.15-1`
- `libkrb5-3:amd64=1.15-1`
- `libkrb5support0:amd64=1.15-1`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.15-1
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.15-1.dsc' krb5_1.15-1.dsc 3282 SHA256:ec2a3211b949480f2419dd4731e8213635d7dfcbe1658d1000cea8fa950599aa
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.15.orig.tar.gz' krb5_1.15.orig.tar.gz 9327157 SHA256:fd34752774c808ab4f6f864f935c49945f5a56b62240b1ad4ab1af7b4ded127c
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.15-1.debian.tar.xz' krb5_1.15-1.debian.tar.xz 141624 SHA256:ddad4ec3d024b1164d1726c767ed8ea4900454793f5a2ce53a5cf7a123c5b4e7
```

Likely also available for browsing at:

- https://sources.debian.net/src/krb5/1.15-1/
- https://sources.debian.net/src/krb5/1.15-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libcap-ng=0.7.7-3`

Binary Packages:

- `libcap-ng0:amd64=0.7.7-3+b1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.7.7-3
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.7.7-3.dsc' libcap-ng_0.7.7-3.dsc 1722 SHA256:6f5262f0ed2792c135e9b6bf7d30461cc3015249832f381505d21b9217a67685
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.7.7.orig.tar.gz' libcap-ng_0.7.7.orig.tar.gz 420178 SHA256:615549ce39b333f6b78baee0c0b4ef18bc726c6bf1cca123dfd89dd963f6d06b
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.7.7-3.debian.tar.xz' libcap-ng_0.7.7-3.debian.tar.xz 5248 SHA256:b7a0846dbd0451903bcbbe3a2696341f4e6000ebd64bed259c7fbf9dfc818363
```

Likely also available for browsing at:

- https://sources.debian.net/src/libcap-ng/0.7.7-3/
- https://sources.debian.net/src/libcap-ng/0.7.7-3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libffi=3.2.1-6`

Binary Packages:

- `libffi6:amd64=3.2.1-6`

Licenses: (parsed from: `/usr/share/doc/libffi6/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libffi=3.2.1-6
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.2.1-6.dsc' libffi_3.2.1-6.dsc 1923 SHA256:f901298b078c7d7f3f75459b5ff74cc804f6f2cfd65ed619d2082d5f77089954
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.2.1.orig.tar.gz' libffi_3.2.1.orig.tar.gz 940837 SHA256:d06ebb8e1d9a22d19e38d63fdb83954253f39bedc5d46232a05645685722ca37
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.2.1-6.debian.tar.xz' libffi_3.2.1-6.debian.tar.xz 11252 SHA256:477709fa90f8c7631fa226a48cdf38737c9f195f3686f62aa76714bcffaee512
```

Likely also available for browsing at:

- https://sources.debian.net/src/libffi/3.2.1-6/
- https://sources.debian.net/src/libffi/3.2.1-6/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libgcrypt20=1.7.6-1`

Binary Packages:

- `libgcrypt20:amd64=1.7.6-1`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.7.6-1
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.6-1.dsc' libgcrypt20_1.7.6-1.dsc 2914 SHA256:ce72ec0f5d8dc26d30433e8e7f85f241b81edf652af6a282a4616fca201288de
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.6.orig.tar.bz2' libgcrypt20_1.7.6.orig.tar.bz2 2897695 SHA256:626aafee84af9d2ce253d2c143dc1c0902dda045780cc241f39970fc60be05bc
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.6.orig.tar.bz2.asc' libgcrypt20_1.7.6.orig.tar.bz2.asc 310 SHA256:91ad5a0efafb0edc63c083f733ce476b2a0da663aea5118126aa63825d314e00
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.6-1.debian.tar.xz' libgcrypt20_1.7.6-1.debian.tar.xz 30444 SHA256:03d93d653e1708063320d11735f1dafa45431f16b07f76f6ed059bbef524ea54
```

Likely also available for browsing at:

- https://sources.debian.net/src/libgcrypt20/1.7.6-1/
- https://sources.debian.net/src/libgcrypt20/1.7.6-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libgpg-error=1.26-2`

Binary Packages:

- `libgpg-error0:amd64=1.26-2`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `GPL-2.1+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.26-2
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.26-2.dsc' libgpg-error_1.26-2.dsc 2454 SHA256:ea53df72d922f224cf0bb69df5a20100a2a5826e890741277425269d70eade20
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.26.orig.tar.bz2' libgpg-error_1.26.orig.tar.bz2 798096 SHA256:4c4bcbc90116932e3acd37b37812d8653b1b189c1904985898e860af818aee69
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.26-2.debian.tar.xz' libgpg-error_1.26-2.debian.tar.xz 12740 SHA256:20a73d5bcc4f523ae16b9279698c01b37dd5cffd2b7dc317c65923aa115ca46c
```

Likely also available for browsing at:

- https://sources.debian.net/src/libgpg-error/1.26-2/
- https://sources.debian.net/src/libgpg-error/1.26-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libidn2-0=0.16-1`

Binary Packages:

- `libidn2-0:amd64=0.16-1`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2-0=0.16-1
'http://deb.debian.org/debian/pool/main/libi/libidn2-0/libidn2-0_0.16-1.dsc' libidn2-0_0.16-1.dsc 1786 SHA256:d806657d36a5836ab08ccc5488372d7b95c03e10964b1c692b0948e6805bc84e
'http://deb.debian.org/debian/pool/main/libi/libidn2-0/libidn2-0_0.16.orig.tar.gz' libidn2-0_0.16.orig.tar.gz 1494295 SHA256:2fad9efff4082ae2143f69df76339ca99379e0e0f4231455f5d3d9d2089c688f
'http://deb.debian.org/debian/pool/main/libi/libidn2-0/libidn2-0_0.16-1.debian.tar.xz' libidn2-0_0.16-1.debian.tar.xz 57392 SHA256:9b643e5a5bd9f3eff52cd5508b1f15f44fe32bca4c1a6c3aa04ebad59d16272d
```

Likely also available for browsing at:

- https://sources.debian.net/src/libidn2-0/0.16-1/
- https://sources.debian.net/src/libidn2-0/0.16-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libidn=1.33-1`

Binary Packages:

- `libidn11:amd64=1.33-1`

Licenses: (parsed from: `/usr/share/doc/libidn11/copyright`)

- `GAP`
- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libidn=1.33-1
'http://deb.debian.org/debian/pool/main/libi/libidn/libidn_1.33-1.dsc' libidn_1.33-1.dsc 1848 SHA256:f076f7dddc45717542a48123d7dddb638beebe8521f5fba29f2d148fdcf12bf0
'http://deb.debian.org/debian/pool/main/libi/libidn/libidn_1.33.orig.tar.gz' libidn_1.33.orig.tar.gz 3501056 SHA256:44a7aab635bb721ceef6beecc4d49dfd19478325e1b47f3196f7d2acc4930e19
'http://deb.debian.org/debian/pool/main/libi/libidn/libidn_1.33-1.debian.tar.xz' libidn_1.33-1.debian.tar.xz 60264 SHA256:a50ee1e2598670ca1166d218e546c4cc031c658188b1193b73d98175d4405ef0
```

Likely also available for browsing at:

- https://sources.debian.net/src/libidn/1.33-1/
- https://sources.debian.net/src/libidn/1.33-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libmnl=1.0.4-2`

Binary Packages:

- `libmnl0:amd64=1.0.4-2`

Licenses: (parsed from: `/usr/share/doc/libmnl0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libmnl=1.0.4-2
'http://deb.debian.org/debian/pool/main/libm/libmnl/libmnl_1.0.4-2.dsc' libmnl_1.0.4-2.dsc 1994 SHA256:131106bb7eb4a94fa8e8c135f92c38068d0b42681f166eb159137f171c568630
'http://deb.debian.org/debian/pool/main/libm/libmnl/libmnl_1.0.4.orig.tar.bz2' libmnl_1.0.4.orig.tar.bz2 301270 SHA256:171f89699f286a5854b72b91d06e8f8e3683064c5901fb09d954a9ab6f551f81
'http://deb.debian.org/debian/pool/main/libm/libmnl/libmnl_1.0.4-2.debian.tar.xz' libmnl_1.0.4-2.debian.tar.xz 7512 SHA256:208d62777081ffe6d7dffde0d7370cefb03fe0a6a0486a1b50f6b7b8e9a5b068
```

Likely also available for browsing at:

- https://sources.debian.net/src/libmnl/1.0.4-2/
- https://sources.debian.net/src/libmnl/1.0.4-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libpsl=0.17.0-3`

Binary Packages:

- `libpsl5:amd64=0.17.0-3`

Licenses: (parsed from: `/usr/share/doc/libpsl5/copyright`)

- `Chromium`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.17.0-3
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.17.0-3.dsc' libpsl_0.17.0-3.dsc 2224 SHA256:20a4c84ba8348ed3839dd79fdafc230f7a0463a68f5af6a2b81b81ba33f77501
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.17.0.orig.tar.gz' libpsl_0.17.0.orig.tar.gz 49087 SHA256:7731e28393e1b4ca363eaffecd6c7570023a7c18c017b45d683ac7d2ba1f0bd1
'http://deb.debian.org/debian/pool/main/libp/libpsl/libpsl_0.17.0-3.debian.tar.xz' libpsl_0.17.0-3.debian.tar.xz 8516 SHA256:d0bd2abdaccadf2603f566e119b949a02523177199455e01c13a9c9deac1e6c3
```

Likely also available for browsing at:

- https://sources.debian.net/src/libpsl/0.17.0-3/
- https://sources.debian.net/src/libpsl/0.17.0-3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libselinux=2.6-3`

Binary Packages:

- `libselinux1:amd64=2.6-3+b1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libselinux=2.6-3
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_2.6-3.dsc' libselinux_2.6-3.dsc 2217 SHA256:91bb53feba8031bfc7b0110fc4e0e1dae4a8e2906f4a524f83252a95ae0e639c
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_2.6.orig.tar.gz' libselinux_2.6.orig.tar.gz 203119 SHA256:4ea2dde50665c202253ba5caac7738370ea0337c47b251ba981c60d24e1a118a
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_2.6-3.debian.tar.xz' libselinux_2.6-3.debian.tar.xz 24396 SHA256:5a06841565e7907bc0dae9f8ed5940d040316192bd9662df59c79af7c212a171
```

Likely also available for browsing at:

- https://sources.debian.net/src/libselinux/2.6-3/
- https://sources.debian.net/src/libselinux/2.6-3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libsemanage=2.6-2`

Binary Packages:

- `libsemanage-common=2.6-2`
- `libsemanage1:amd64=2.6-2`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage1/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=2.6-2
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_2.6-2.dsc' libsemanage_2.6-2.dsc 2338 SHA256:2806bf3591dc7eb4c80d647a9e65df13d03657cfa6e049de1035165e0d8484d0
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_2.6.orig.tar.gz' libsemanage_2.6.orig.tar.gz 155897 SHA256:4f81541047290b751f2ffb926fcd381c186f22db18d9fe671b0b4a6a54e8cfce
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_2.6-2.debian.tar.xz' libsemanage_2.6-2.debian.tar.xz 17088 SHA256:3d1c4c5ea5d4f27a521b64ba3fc499c8b662257ffec773706501f466032db8cf
```

Likely also available for browsing at:

- https://sources.debian.net/src/libsemanage/2.6-2/
- https://sources.debian.net/src/libsemanage/2.6-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libsepol=2.6-2`

Binary Packages:

- `libsepol1:amd64=2.6-2`

Licenses: (parsed from: `/usr/share/doc/libsepol1/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libsepol=2.6-2
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_2.6-2.dsc' libsepol_2.6-2.dsc 1814 SHA256:197ddaf44a5139d7ca6c12ce6b29fca0589f72c59ac588a7fa39d11b2e65778a
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_2.6.orig.tar.gz' libsepol_2.6.orig.tar.gz 442549 SHA256:d856d6506054f52abeaa3543ea2f2344595a3dc05d0d873ed7f724f7a16b1874
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_2.6-2.debian.tar.xz' libsepol_2.6-2.debian.tar.xz 14320 SHA256:d7a1022d03eb53a8d30262e06f14f691e553b3db684ca0f3549cd17b93fb7465
```

Likely also available for browsing at:

- https://sources.debian.net/src/libsepol/2.6-2/
- https://sources.debian.net/src/libsepol/2.6-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libssh2=1.7.0-1`

Binary Packages:

- `libssh2-1:amd64=1.7.0-1`

Licenses: (parsed from: `/usr/share/doc/libssh2-1/copyright`)

- `BSD3`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.7.0-1
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.7.0-1.dsc' libssh2_1.7.0-1.dsc 1828 SHA256:4f2880ce02d40c4904f750687424e9f2c1aa68a4632da9866e08c809a69f7425
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.7.0.orig.tar.gz' libssh2_1.7.0.orig.tar.gz 811714 SHA256:e4561fd43a50539a8c2ceb37841691baf03ecb7daf043766da1b112e4280d584
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.7.0-1.debian.tar.xz' libssh2_1.7.0-1.debian.tar.xz 6396 SHA256:2f4fb78f0d6d33492ef63e04a0d007f03e56466542c0b8271bbcdcb530f31f8e
```

Likely also available for browsing at:

- https://sources.debian.net/src/libssh2/1.7.0-1/
- https://sources.debian.net/src/libssh2/1.7.0-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libtasn1-6=4.10-1`

Binary Packages:

- `libtasn1-6:amd64=4.10-1`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `libunistring=0.9.6+really0.9.3-0.1`

Binary Packages:

- `libunistring0:amd64=0.9.6+really0.9.3-0.1`

Licenses: (parsed from: `/usr/share/doc/libunistring0/copyright`)

- `GFDL-1.2`
- `GFDL-1.2+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libunistring=0.9.6+really0.9.3-0.1
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_0.9.6+really0.9.3-0.1.dsc' libunistring_0.9.6+really0.9.3-0.1.dsc 2109 SHA256:bf73a89a416333268ac9b457a06d1d92e5402c4f392187ad30e6146ffd3600ae
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_0.9.6+really0.9.3.orig.tar.gz' libunistring_0.9.6+really0.9.3.orig.tar.gz 2555215 SHA256:610d3ec724fbdaa654afe3cff20b9f4d504be3fd296fded2e0f7f764041006a3
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_0.9.6+really0.9.3-0.1.debian.tar.xz' libunistring_0.9.6+really0.9.3-0.1.debian.tar.xz 35372 SHA256:2d7636b16a56f1ad09748121a2181db4c2687fa83324c2f17bf451ee01b9de93
```

Likely also available for browsing at:

- https://sources.debian.net/src/libunistring/0.9.6+really0.9.3-0.1/
- https://sources.debian.net/src/libunistring/0.9.6+really0.9.3-0.1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `lsb=9.20161125`

Binary Packages:

- `lsb-base=9.20161125`

Licenses: (parsed from: `/usr/share/doc/lsb-base/copyright`)

- `BSD-3-clause`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris lsb=9.20161125
'http://deb.debian.org/debian/pool/main/l/lsb/lsb_9.20161125.dsc' lsb_9.20161125.dsc 1697 SHA256:f2dd58084b1beabe966136cfd2e1b355002c1fb1635a6db5ef159b09ed94864f
'http://deb.debian.org/debian/pool/main/l/lsb/lsb_9.20161125.tar.xz' lsb_9.20161125.tar.xz 43096 SHA256:0f9889ff1922da54d1f1538c11a57aa21dc5adf621e6201b18026f6633088bbd
```

Likely also available for browsing at:

- https://sources.debian.net/src/lsb/9.20161125/
- https://sources.debian.net/src/lsb/9.20161125/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `lz4=0.0~r131-2`

Binary Packages:

- `liblz4-1:amd64=0.0~r131-2+b1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=0.0~r131-2
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_0.0~r131-2.dsc' lz4_0.0~r131-2.dsc 1973 SHA256:304cf9dddee387377929adf3f2cef0ae19fb2e56b6cc9eab05798845b58bd9b6
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_0.0~r131.orig.tar.gz' lz4_0.0~r131.orig.tar.gz 133784 SHA256:9d4d00614d6b9dec3114b33d1224b6262b99ace24434c53487a0c8fd0b18cfed
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_0.0~r131-2.debian.tar.xz' lz4_0.0~r131-2.debian.tar.xz 4936 SHA256:966df055dd8fa7f292c283452b43a5d2d2047d542fe49e97025006e69525e224
```

Likely also available for browsing at:

- https://sources.debian.net/src/lz4/0.0~r131-2/
- https://sources.debian.net/src/lz4/0.0~r131-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `mawk=1.3.3-17`

Binary Packages:

- `mawk=1.3.3-17+b3`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.3-17
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.3-17.dsc' mawk_1.3.3-17.dsc 1801 SHA256:f98ce6e153e8ac1faf8165bbf77447a4279313f1c18f6bfeec0c5ce35e4b9c03
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.3.orig.tar.gz' mawk_1.3.3.orig.tar.gz 209942 SHA256:32649c46063d4ef0777a12ae6e9a26bcc920833d54e1abca7edb8d37481e7485
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.3-17.diff.gz' mawk_1.3.3-17.diff.gz 63506 SHA256:13cb66b6eb5ee654d5626621d5ef476ede6b0bebac18ce765516de810e58490c
```

Likely also available for browsing at:

- https://sources.debian.net/src/mawk/1.3.3-17/
- https://sources.debian.net/src/mawk/1.3.3-17/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `ncurses=6.0+20161126-1`

Binary Packages:

- `libncursesw5:amd64=6.0+20161126-1`
- `libtinfo5:amd64=6.0+20161126-1`
- `ncurses-base=6.0+20161126-1`
- `ncurses-bin=6.0+20161126-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris ncurses=6.0+20161126-1
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.0+20161126-1.dsc' ncurses_6.0+20161126-1.dsc 3781 SHA256:362e1e63f99b83d3ef10946bc3caf5618066dc361a79861ee37b2ac12ac77201
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.0+20161126.orig.tar.gz' ncurses_6.0+20161126.orig.tar.gz 3192242 SHA256:e4b9cf1cfcf5a2db7df1d36402967783ba759246c8ff5a17a85ffd7e79296ec0
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.0+20161126-1.debian.tar.xz' ncurses_6.0+20161126-1.debian.tar.xz 52608 SHA256:262970bf8159e962f204fa12ce18d59ea631b3d33c43335912f4f2fe85d73003
```

Likely also available for browsing at:

- https://sources.debian.net/src/ncurses/6.0+20161126-1/
- https://sources.debian.net/src/ncurses/6.0+20161126-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `netbase=5.4`

Binary Packages:

- `netbase=5.4`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=5.4
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_5.4.dsc' netbase_5.4.dsc 1326 SHA256:ebe29d45e65b661d64636cbce3840997d8079cf338efbfa347b4c73ed2831b7b
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_5.4.tar.xz' netbase_5.4.tar.xz 31524 SHA256:66ff73d2d162e2d49db43988d8b8cd328cf7fffca042db73397f14c71825e80d
```

Likely also available for browsing at:

- https://sources.debian.net/src/netbase/5.4/
- https://sources.debian.net/src/netbase/5.4/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `nettle=3.3-1`

Binary Packages:

- `libhogweed4:amd64=3.3-1+b1`
- `libnettle6:amd64=3.3-1+b1`

Licenses: (parsed from: `/usr/share/doc/libhogweed4/copyright`, `/usr/share/doc/libnettle6/copyright`)

- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1+`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris nettle=3.3-1
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.3-1.dsc' nettle_3.3-1.dsc 2043 SHA256:3336bc6e8e5b1acad66afa97a05f934e4d758c614fd468d5650b5a38049f1161
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.3.orig.tar.gz' nettle_3.3.orig.tar.gz 1887927 SHA256:46942627d5d0ca11720fec18d81fc38f7ef837ea4197c1f630e71ce0d470b11e
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.3-1.debian.tar.xz' nettle_3.3-1.debian.tar.xz 19428 SHA256:42fef549318af6cfdf76336eb348501d09454a1d873a84f66440b9a791a0ff1b
```

Likely also available for browsing at:

- https://sources.debian.net/src/nettle/3.3-1/
- https://sources.debian.net/src/nettle/3.3-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `nghttp2=1.18.1-1`

Binary Packages:

- `libnghttp2-14:amd64=1.18.1-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `SIL-OFL-1.1`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.18.1-1
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.18.1-1.dsc' nghttp2_1.18.1-1.dsc 2283 SHA256:a473983d2630c5f9df6b1ef439e4eee9fbb4fbe9b61bc1b80289b1ba0a84336d
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.18.1.orig.tar.bz2' nghttp2_1.18.1.orig.tar.bz2 1780766 SHA256:5d8bb930eb90c552ec836c7b1862406b69cafcda5520bf266c8f5d914d9b447c
'http://deb.debian.org/debian/pool/main/n/nghttp2/nghttp2_1.18.1-1.debian.tar.xz' nghttp2_1.18.1-1.debian.tar.xz 11716 SHA256:ffcd8e21b6824b6907466f4d3c481f4a68601f8b0b09545e19c033d14a0d16d5
```

Likely also available for browsing at:

- https://sources.debian.net/src/nghttp2/1.18.1-1/
- https://sources.debian.net/src/nghttp2/1.18.1-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `openldap=2.4.44+dfsg-4`

Binary Packages:

- `libldap-2.4-2:amd64=2.4.44+dfsg-4+b1`
- `libldap-common=2.4.44+dfsg-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openldap=2.4.44+dfsg-4
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.4.44+dfsg-4.dsc' openldap_2.4.44+dfsg-4.dsc 2946 SHA256:884e1b0923ebf4360e1be2c16ef456fa6b8706dd4f5199521c97fd966a025081
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.4.44+dfsg.orig.tar.gz' openldap_2.4.44+dfsg.orig.tar.gz 4826590 SHA256:d5187c229bec163c5d97845846e1b87917755f85b04f444c08836384f4bd7ffe
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.4.44+dfsg-4.debian.tar.xz' openldap_2.4.44+dfsg-4.debian.tar.xz 162840 SHA256:d4ffd3036dbbbc340034974d6585f2129c786ee04506efced37f8a1d132644cf
```

Likely also available for browsing at:

- https://sources.debian.net/src/openldap/2.4.44+dfsg-4/
- https://sources.debian.net/src/openldap/2.4.44+dfsg-4/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `openssl1.0=1.0.2k-1`

Binary Packages:

- `libssl1.0.2:amd64=1.0.2k-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openssl1.0=1.0.2k-1
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2k-1.dsc' openssl1.0_1.0.2k-1.dsc 2529 SHA256:d814c48e2fb24841dcba89a8107e62c42d9ecbf50f35dbf6456dc4dcf1628f9a
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2k.orig.tar.gz' openssl1.0_1.0.2k.orig.tar.gz 5309236 SHA256:6b3977c61f2aedf0f96367dcfb5c6e578cf37e7b8d913b4ecb6643c3cb88d8c0
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2k.orig.tar.gz.asc' openssl1.0_1.0.2k.orig.tar.gz.asc 455 SHA256:88ea1b7a34f5b7516d3b6d0d8ae55961979f7832c12ab42d033af0867033bc05
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2k-1.debian.tar.xz' openssl1.0_1.0.2k-1.debian.tar.xz 75800 SHA256:667f5a187a0877131efbd98f2b693f93db6f4cba0658ed9d7f7f720b5724c424
```

Likely also available for browsing at:

- https://sources.debian.net/src/openssl1.0/1.0.2k-1/
- https://sources.debian.net/src/openssl1.0/1.0.2k-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `openssl=1.1.0e-1`

Binary Packages:

- `libssl1.1:amd64=1.1.0e-1`
- `openssl=1.1.0e-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `p11-kit=0.23.3-2`

Binary Packages:

- `libp11-kit0:amd64=0.23.3-2`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`)

- `BSD-3-Clause`
- `ISC`
- `ISC+IBM`
- `permissive-like-automake-output`
- `same-as-rest-of-p11kit`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.23.3-2
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.3-2.dsc' p11-kit_0.23.3-2.dsc 2452 SHA256:fc8e87147d30de8d33e78adb805530d582655999762129b75097a9824679b0cc
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.3.orig.tar.gz' p11-kit_0.23.3.orig.tar.gz 1047441 SHA256:d487f04dba3f9e8256f53034c59c944ca45fd7b8434c095da6a74079644dcd82
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.3.orig.tar.gz.asc' p11-kit_0.23.3.orig.tar.gz.asc 543 SHA256:a9268313ad8e6c3dae5f4cf9006d8a773861e567c98786482304b3cc91883647
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.3-2.debian.tar.xz' p11-kit_0.23.3-2.debian.tar.xz 19784 SHA256:952f55f8c5e2cdc03c8388b59b0bd77bb53eb8f2c2ca2a686cfc91b52100e257
```

Likely also available for browsing at:

- https://sources.debian.net/src/p11-kit/0.23.3-2/
- https://sources.debian.net/src/p11-kit/0.23.3-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `pam=1.1.8-3.5`

Binary Packages:

- `libpam-modules:amd64=1.1.8-3.5`
- `libpam-modules-bin=1.1.8-3.5`
- `libpam-runtime=1.1.8-3.5`
- `libpam0g:amd64=1.1.8-3.5`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `pcre3=2:8.39-3`

Binary Packages:

- `libpcre3:amd64=2:8.39-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre3=2:8.39-3
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39-3.dsc' pcre3_8.39-3.dsc 2133 SHA256:3180a023c33b5eb7f0a853bec887be867d00a68da8d119d989909e40c6168fd7
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39.orig.tar.bz2' pcre3_8.39.orig.tar.bz2 1560758 SHA256:b858099f82483031ee02092711689e7245586ada49e534a06e678b8ea9549e8b
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39-3.debian.tar.gz' pcre3_8.39-3.debian.tar.gz 25025 SHA256:a9f0e1a96b6a017965fe69233e267682c289f2cfeb33b46fb78aedcb8cf2c16a
```

Likely also available for browsing at:

- https://sources.debian.net/src/pcre3/2:8.39-3/
- https://sources.debian.net/src/pcre3/2:8.39-3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `perl=5.24.1-2`

Binary Packages:

- `libperl5.24:amd64=5.24.1-2`
- `perl=5.24.1-2`
- `perl-base=5.24.1-2`
- `perl-modules-5.24=5.24.1-2`

Licenses: (parsed from: `/usr/share/doc/libperl5.24/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.24/copyright`)

- `Artistic`
- `Artistic,`
- `Artistic-2`
- `BSD-3-clause`
- `BSD-3-clause-GENERIC`
- `BSD-3-clause-with-weird-numbering`
- `BSD-4-clause-POWERDOG`
- `BZIP`
- `CC0-1.0`
- `DONT-CHANGE-THE-GPL`
- `Expat`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3+-WITH-BISON-EXCEPTION`
- `HSIEH-BSD`
- `HSIEH-DERIVATIVE`
- `LGPL-2.1`
- `REGCOMP`
- `REGCOMP,`
- `RRA-KEEP-THIS-NOTICE`
- `S2P`
- `SDBM-PUBLIC-DOMAIN`
- `TEXT-TABS`
- `Unicode`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris perl=5.24.1-2
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.24.1-2.dsc' perl_5.24.1-2.dsc 2316 SHA256:4938b6b81912d4fea8626b84f14292d49c25d500a223644b2f67db8f1d01e150
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.24.1.orig.tar.xz' perl_5.24.1.orig.tar.xz 11569284 SHA256:03a77bac4505c270f1890ece75afc7d4b555090b41aa41ea478747e23b2afb3f
'http://deb.debian.org/debian/pool/main/p/perl/perl_5.24.1-2.debian.tar.xz' perl_5.24.1-2.debian.tar.xz 165680 SHA256:e398649c63c1f50adace04531856b03a73892f6f210b2d18b16fb8978c5d28b8
```

Likely also available for browsing at:

- https://sources.debian.net/src/perl/5.24.1-2/
- https://sources.debian.net/src/perl/5.24.1-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-1`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-1+b1`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-1
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1-1.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-1.dsc 2315 SHA256:e56822b88625bf6a51f06652fc36fa2a1348b4325ac76541800cd078192aa3d2
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA256:5c032f5c8cc2937eb55a81a94effdfed3b0a0304b6376147b86f951e225e3ab5
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1-1.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-1.debian.tar.xz 8044 SHA256:675847f5cddb860256cbf2e7d5b85918aa53b59b0fd97a466b39a5c77a399537
```

Likely also available for browsing at:

- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-1/
- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `sed=4.4-1`

Binary Packages:

- `sed=4.4-1`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris sed=4.4-1
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.4-1.dsc' sed_4.4-1.dsc 2048 SHA256:bb2a11d04f3aeba73cc994e097219fde8c5e0fd1bcf42e0ecc8a4f2282c00fc9
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.4.orig.tar.xz' sed_4.4.orig.tar.xz 1181664 SHA256:cbd6ebc5aaf080ed60d0162d7f6aeae58211a1ee9ba9bb25623daa6cd942683b
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.4-1.debian.tar.xz' sed_4.4-1.debian.tar.xz 59552 SHA256:56dd1f91c5e33b419f38cde93afc90d6fad9064ef4594a877424a0ab2ac9a4bf
```

Likely also available for browsing at:

- https://sources.debian.net/src/sed/4.4-1/
- https://sources.debian.net/src/sed/4.4-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `sensible-utils=0.0.9`

Binary Packages:

- `sensible-utils=0.0.9`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.9
'http://deb.debian.org/debian/pool/main/s/sensible-utils/sensible-utils_0.0.9.dsc' sensible-utils_0.0.9.dsc 1405 SHA256:390c29b31a09ab7f31f8b5fc0fd82e47c25f15b22b17c614fb87f12d3b091070
'http://deb.debian.org/debian/pool/main/s/sensible-utils/sensible-utils_0.0.9.tar.gz' sensible-utils_0.0.9.tar.gz 74331 SHA256:6fcb5cc0f7f1cf80421840cfa17b1b3fa5afaf3fe852dc984a789023af2f70c6
```

Likely also available for browsing at:

- https://sources.debian.net/src/sensible-utils/0.0.9/
- https://sources.debian.net/src/sensible-utils/0.0.9/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `shadow=1:4.4-4`

Binary Packages:

- `login=1:4.4-4`
- `passwd=1:4.4-4`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `systemd=232-22`

Binary Packages:

- `libsystemd0:amd64=232-22`
- `libudev1:amd64=232-22`

Licenses: (parsed from: `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`)

- `CC0`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `sysvinit=2.88dsf-59.9`

Binary Packages:

- `sysvinit-utils=2.88dsf-59.9`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris sysvinit=2.88dsf-59.9
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_2.88dsf-59.9.dsc' sysvinit_2.88dsf-59.9.dsc 2123 SHA256:a943edeac16668d3e55583daa4033ad46469e84ffad014e0e2007d9c3167e63d
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_2.88dsf.orig.tar.gz' sysvinit_2.88dsf.orig.tar.gz 125330 SHA256:b016f937958d2809a020d407e1287bdc09abf1d44efaa96530e2ea57f544f4e8
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_2.88dsf-59.9.debian.tar.xz' sysvinit_2.88dsf-59.9.debian.tar.xz 132584 SHA256:fbd5c085680d896ec6ee1c5a55ae2d8a5a6b9fd5a7ec1e13010dace24fdbcd5c
```

Likely also available for browsing at:

- https://sources.debian.net/src/sysvinit/2.88dsf-59.9/
- https://sources.debian.net/src/sysvinit/2.88dsf-59.9/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `tar=1.29b-1.1`

Binary Packages:

- `tar=1.29b-1.1`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris tar=1.29b-1.1
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.29b-1.1.dsc' tar_1.29b-1.1.dsc 2057 SHA256:9474ed422017e23e8208785c071b9f7765d73d704b9bb19da22699c6581d73ef
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.29b.orig.tar.xz' tar_1.29b.orig.tar.xz 1822008 SHA256:6a59706ebee384a6cd2fb3ee1dbfbfc20c5c66c7efd7cedb28edc054fca8ba00
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.29b-1.1.debian.tar.xz' tar_1.29b-1.1.debian.tar.xz 28484 SHA256:380f80af0e87446796f05ba384c5d130ea2ad5978b8cfdcf315503966333ebb9
```

Likely also available for browsing at:

- https://sources.debian.net/src/tar/1.29b-1.1/
- https://sources.debian.net/src/tar/1.29b-1.1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `tzdata=2017b-1`

Binary Packages:

- `tzdata=2017b-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tzdata=2017b-1
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2017b-1.dsc' tzdata_2017b-1.dsc 2005 SHA256:ab26ea2d019b6db54abd8ee17c90aeb717641dc8900ab19dca8d5faa4b66d852
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2017b.orig.tar.gz' tzdata_2017b.orig.tar.gz 324317 SHA256:f8242a522ea3496b0ce4ff4f2e75a049178da21001a08b8e666d8cbe07d18086
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2017b-1.debian.tar.xz' tzdata_2017b-1.debian.tar.xz 101168 SHA256:b7ed1f68343a5463aa2efbc527a05b89461e93b5626337d8d581c78e8fdf180c
```

Likely also available for browsing at:

- https://sources.debian.net/src/tzdata/2017b-1/
- https://sources.debian.net/src/tzdata/2017b-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `ustr=1.0.4-6`

Binary Packages:

- `libustr-1.0-1:amd64=1.0.4-6`

Licenses: (parsed from: `/usr/share/doc/libustr-1.0-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris ustr=1.0.4-6
'http://deb.debian.org/debian/pool/main/u/ustr/ustr_1.0.4-6.dsc' ustr_1.0.4-6.dsc 2029 SHA256:87a854fc03dc059d5d4f135dfd36353c8c09f88a6eb216c6dcea8adadbe6ba59
'http://deb.debian.org/debian/pool/main/u/ustr/ustr_1.0.4.orig.tar.gz' ustr_1.0.4.orig.tar.gz 301345 SHA256:4d293b6b9d9fe51d58441f4b09b1f0005fcad8256ae8048587789bf5dbefb62e
'http://deb.debian.org/debian/pool/main/u/ustr/ustr_1.0.4-6.debian.tar.xz' ustr_1.0.4-6.debian.tar.xz 25608 SHA256:75aa6be2c70eba632ac63078e55ecb4b5a45e6624501a8ed6d81b9a2014d149e
```

Likely also available for browsing at:

- https://sources.debian.net/src/ustr/1.0.4-6/
- https://sources.debian.net/src/ustr/1.0.4-6/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `util-linux=2.29.2-1`

Binary Packages:

- `bsdutils=1:2.29.2-1`
- `libblkid1:amd64=2.29.2-1`
- `libfdisk1:amd64=2.29.2-1`
- `libmount1:amd64=2.29.2-1`
- `libsmartcols1:amd64=2.29.2-1`
- `libuuid1:amd64=2.29.2-1`
- `mount=2.29.2-1`
- `util-linux=2.29.2-1`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libfdisk1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.29.2-1
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.29.2-1.dsc' util-linux_2.29.2-1.dsc 3918 SHA256:a1b5983b4ae58c6478d05f34b120b6a9d51b18dc2287ee9e52de8bf6e43e2bb0
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.29.2.orig.tar.xz' util-linux_2.29.2.orig.tar.xz 4277668 SHA256:accea4d678209f97f634f40a93b7e9fcad5915d1f4749f6c47bee6bf110fe8e3
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.29.2-1.debian.tar.xz' util-linux_2.29.2-1.debian.tar.xz 73664 SHA256:820511a8c7c03c7b62218c03f57e4a33e5e928a2cb7d9cda58b9c07aade7744b
```

Likely also available for browsing at:

- https://sources.debian.net/src/util-linux/2.29.2-1/
- https://sources.debian.net/src/util-linux/2.29.2-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `wget=1.18-5`

Binary Packages:

- `wget=1.18-5`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.18-5
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.18-5.dsc' wget_1.18-5.dsc 1902 SHA256:3aabc0aeb73b151e9e6433db98270cb88629197dec6cfd7b811f237402b27fdb
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.18.orig.tar.gz' wget_1.18.orig.tar.gz 3865525 SHA256:a00a65fab84cc46e24c53ce88c45604668a7a479276e037dc2f558e34717fb2d
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.18-5.debian.tar.xz' wget_1.18-5.debian.tar.xz 21940 SHA256:398296b9ac72a8471ad3478370d4ed674be478572ccb70f6b61950d9b1d8044f
```

Likely also available for browsing at:

- https://sources.debian.net/src/wget/1.18-5/
- https://sources.debian.net/src/wget/1.18-5/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `xz-utils=5.2.2-1.2`

Binary Packages:

- `liblzma5:amd64=5.2.2-1.2+b1`

Licenses: (parsed from: `/usr/share/doc/liblzma5/copyright`)

- `Autoconf`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PD`
- `PD-debian`
- `config-h`
- `noderivs`
- `none`
- `permissive-fsf`
- `permissive-nowarranty`
- `probably-PD`

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.2.2-1.2
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2-1.2.dsc' xz-utils_5.2.2-1.2.dsc 2550 SHA256:13c8d8d0c243af78dc89b6e2cd670c8d8a2522379e1fcd196957c95d988d5961
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2.orig.tar.xz' xz-utils_5.2.2.orig.tar.xz 1016404 SHA256:f341b1906ebcdde291dd619399ae944600edc9193619dd0c0110a5f05bfcc89e
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2.orig.tar.xz.asc' xz-utils_5.2.2.orig.tar.xz.asc 543 SHA256:2cc0575556e1331b3f468e6e7dca5969ce86efcc315d62672279b4e68b2e449f
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2-1.2.debian.tar.xz' xz-utils_5.2.2-1.2.debian.tar.xz 108632 SHA256:231c08d5c2c4e5c8ef5d6d58cac91aaeb2e4fcddc35e1ed3c69d730a2375c948
```

Likely also available for browsing at:

- https://sources.debian.net/src/xz-utils/5.2.2-1.2/
- https://sources.debian.net/src/xz-utils/5.2.2-1.2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `zlib=1:1.2.8.dfsg-5`

Binary Packages:

- `zlib1g:amd64=1:1.2.8.dfsg-5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.2.8.dfsg-5
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg-5.dsc' zlib_1.2.8.dfsg-5.dsc 2259 SHA256:35ebfdbb74b3563d344b2bb946909f5d3221cdf971876549ea7ccec01fabcbec
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg.orig.tar.gz' zlib_1.2.8.dfsg.orig.tar.gz 361943 SHA256:2caecc2c3f1ef8b87b8f72b128a03e61c307e8c14f5ec9b422ef7914ba75cf9f
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg-5.debian.tar.xz' zlib_1.2.8.dfsg-5.debian.tar.xz 18500 SHA256:7b88f58d1bfe8e873b8362ede3d0bc569793decc60094189fad1a110599cdd95
```

Likely also available for browsing at:

- https://sources.debian.net/src/zlib/1:1.2.8.dfsg-5/
- https://sources.debian.net/src/zlib/1:1.2.8.dfsg-5/debian/copyright (for direct copyright/license information)
