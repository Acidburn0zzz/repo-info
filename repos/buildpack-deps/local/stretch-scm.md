# `buildpack-deps:stretch-scm`

## Docker Metadata

- Image ID: `sha256:c0c216b9f113588fc9081fa6f5bec2386721286cc8740fa0f75182c630219219`
- Created: `2017-01-17T00:02:18.604803706Z`
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.2.52-3`

Binary Packages:

- `libacl1:amd64=2.2.52-3`

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

### `dpkg` source package: `apr-util=1.5.4-3`

Binary Packages:

- `libaprutil1:amd64=1.5.4-3`

Licenses: (parsed from: `/usr/share/doc/libaprutil1/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.5.4-3
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.5.4-3.dsc' apr-util_1.5.4-3.dsc 2646 SHA256:352bbbdf8d4e18014614d5a92da11b599cd04bb30ee03d9f04f26a75626371c7
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.5.4.orig.tar.bz2' apr-util_1.5.4.orig.tar.bz2 694427 SHA256:a6cf327189ca0df2fb9d5633d7326c460fe2b61684745fd7963e79a6dd0dc82e
'http://deb.debian.org/debian/pool/main/a/apr-util/apr-util_1.5.4-3.debian.tar.xz' apr-util_1.5.4-3.debian.tar.xz 212220 SHA256:c5e7bfcdafb16104e324ddb6825b94577a57a5b77b809dc0330e38ecab030efa
```

Likely also available for browsing at:

- https://sources.debian.net/src/apr-util/1.5.4-3/
- https://sources.debian.net/src/apr-util/1.5.4-3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `apr=1.5.2-5`

Binary Packages:

- `libapr1:amd64=1.5.2-5`

Licenses: (parsed from: `/usr/share/doc/libapr1/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.5.2-5
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.5.2-5.dsc' apr_1.5.2-5.dsc 2115 SHA256:b58bb3209c8a28bff47666de6a9bf32292303fdc2433c9fafb15f2a9e6c16ca6
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.5.2.orig.tar.bz2' apr_1.5.2.orig.tar.bz2 826885 SHA256:7d03ed29c22a7152be45b8e50431063736df9e1daa1ddf93f6a547ba7a28f67a
'http://deb.debian.org/debian/pool/main/a/apr/apr_1.5.2-5.debian.tar.xz' apr_1.5.2-5.debian.tar.xz 212856 SHA256:5b253cd3acc284241c3cb4a84d9d16f9c5c7775c8f7a26b3a0068ff174bacf76
```

Likely also available for browsing at:

- https://sources.debian.net/src/apr/1.5.2-5/
- https://sources.debian.net/src/apr/1.5.2-5/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `apt=1.4~beta3`

Binary Packages:

- `apt=1.4~beta3`
- `libapt-pkg5.0:amd64=1.4~beta3`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg5.0/copyright`)

- `GPL-2`
- `GPLv2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `attr=1:2.4.47-2`

Binary Packages:

- `libattr1:amd64=1:2.4.47-2`

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

### `dpkg` source package: `audit=1:2.6.7-1`

Binary Packages:

- `libaudit-common=1:2.6.7-1`
- `libaudit1:amd64=1:2.6.7-1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:2.6.7-1
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.6.7-1.dsc' audit_2.6.7-1.dsc 2296 SHA256:1a7aa3f84928888f90132250e729c49079a0218870fadfb4c8227db81074ee5f
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.6.7.orig.tar.gz' audit_2.6.7.orig.tar.gz 1080848 SHA256:8923917332daa7833bbc0c1d9eb012167093fbad000da4a9630fb3356aff8cdc
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.6.7-1.debian.tar.xz' audit_2.6.7-1.debian.tar.xz 18208 SHA256:1a10461619f8c94113618e2f0a9287688f1d6ee46c847be89f572bc2d047982f
```

Likely also available for browsing at:

- https://sources.debian.net/src/audit/1:2.6.7-1/
- https://sources.debian.net/src/audit/1:2.6.7-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `base-files=9.7`

Binary Packages:

- `base-files=9.7`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `base-passwd=3.5.42`

Binary Packages:

- `base-passwd=3.5.42`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `PD`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `bash=4.4-2`

Binary Packages:

- `bash=4.4-2`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `bzip2=1.0.6-8`

Binary Packages:

- `libbz2-1.0:amd64=1.0.6-8`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.6-8
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6-8.1.dsc' bzip2_1.0.6-8.1.dsc 2082 SHA256:d80deed11a1419ad090cb486dd2335850fd8719b809c32002dea04b485f55dbd
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6.orig.tar.bz2' bzip2_1.0.6.orig.tar.bz2 708737 SHA256:d70a9ccd8bdf47e302d96c69fecd54925f45d9c7b966bb4ef5f56b770960afa7
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6-8.1.debian.tar.bz2' bzip2_1.0.6-8.1.debian.tar.bz2 59875 SHA256:bdbe7bf29e014e44d79bb7c733fe63cae990ab50882a4a07867cf69c61ad72b7
```

Likely also available for browsing at:

- https://sources.debian.net/src/bzip2/1.0.6-8/
- https://sources.debian.net/src/bzip2/1.0.6-8/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `bzr=2.7.0+bzr6619-4`

Binary Packages:

- `bzr=2.7.0+bzr6619-4`
- `python-bzrlib=2.7.0+bzr6619-4`

Licenses: (parsed from: `/usr/share/doc/bzr/copyright`, `/usr/share/doc/python-bzrlib/copyright`)

- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


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

### `dpkg` source package: `cdebconf=0.219`

Binary Packages:

- `libdebconfclient0:amd64=0.219`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.219
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.219.dsc' cdebconf_0.219.dsc 2662 SHA256:2b10fbd993eab15fb9b775ac1033876e0db7ae31dc1b5040b9b39f61306d1f37
'http://deb.debian.org/debian/pool/main/c/cdebconf/cdebconf_0.219.tar.xz' cdebconf_0.219.tar.xz 271988 SHA256:e1cc4d092f07fe4437d12e42ac956ac3b3b039d1b25d971ed79d931b1d1ba0b4
```

Likely also available for browsing at:

- https://sources.debian.net/src/cdebconf/0.219/
- https://sources.debian.net/src/cdebconf/0.219/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `configobj=5.0.6-2`

Binary Packages:

- `python-configobj=5.0.6-2`

Licenses: (parsed from: `/usr/share/doc/python-configobj/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris configobj=5.0.6-2
'http://deb.debian.org/debian/pool/main/c/configobj/configobj_5.0.6-2.dsc' configobj_5.0.6-2.dsc 2381 SHA256:9bb8577128460ff33326d3d90b8454376c83f4d41b1da61aeabdbfcbfb5e0087
'http://deb.debian.org/debian/pool/main/c/configobj/configobj_5.0.6.orig.tar.gz' configobj_5.0.6.orig.tar.gz 143664 SHA256:2e140354efcca6f558ff9ee941b435ae09a617bc071797bef62c8d6ed2033d5e
'http://deb.debian.org/debian/pool/main/c/configobj/configobj_5.0.6-2.debian.tar.xz' configobj_5.0.6-2.debian.tar.xz 7436 SHA256:dc677cd329b4a3aacebe10c5a169d9d092cc27888c3f3f9203930cacd6a0eab8
```

Likely also available for browsing at:

- https://sources.debian.net/src/configobj/5.0.6-2/
- https://sources.debian.net/src/configobj/5.0.6-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `coreutils=8.26-1`

Binary Packages:

- `coreutils=8.26-1`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `curl=7.51.0-1`

Binary Packages:

- `curl=7.51.0-1`
- `libcurl3-gnutls:amd64=7.51.0-1`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3-gnutls/copyright`)

- `BSD-3-Clause`
- `BSD-4-Clause`
- `ISC`
- `curl`
- `other`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `cyrus-sasl2=2.1.27~101-g0780600+dfsg-2`

Binary Packages:

- `libsasl2-2:amd64=2.1.27~101-g0780600+dfsg-2`
- `libsasl2-modules-db:amd64=2.1.27~101-g0780600+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.27~101-g0780600+dfsg-2
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg-2.dsc' cyrus-sasl2_2.1.27~101-g0780600+dfsg-2.dsc 3314 SHA256:8ad6f65f2969f6af8dadf0ba75a9bf3fd685e509d28ecc840382df567b350b00
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg.orig.tar.xz' cyrus-sasl2_2.1.27~101-g0780600+dfsg.orig.tar.xz 1143888 SHA256:69f34971f768e7ee6a6b647ec2d16a5a72a854ecd4602b019d5f79ba61063fdc
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg-2.debian.tar.xz' cyrus-sasl2_2.1.27~101-g0780600+dfsg-2.debian.tar.xz 94416 SHA256:14001f7a60ce08898e6f87ea973d1f8e42aedb752ffb06020cd9ba693a5ca005
```

Likely also available for browsing at:

- https://sources.debian.net/src/cyrus-sasl2/2.1.27~101-g0780600+dfsg-2/
- https://sources.debian.net/src/cyrus-sasl2/2.1.27~101-g0780600+dfsg-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `dash=0.5.8-2.3`

Binary Packages:

- `dash=0.5.8-2.3`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `db5.3=5.3.28-12`

Binary Packages:

- `libdb5.3:amd64=5.3.28-12`

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

### `dpkg` source package: `debconf=1.5.59`

Binary Packages:

- `debconf=1.5.59`

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

### `dpkg` source package: `diffutils=1:3.5-1`

Binary Packages:

- `diffutils=1:3.5-1`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `GFDL`
- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `dpkg=1.18.18`

Binary Packages:

- `dpkg=1.18.18`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain-md5`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.18.18
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.18.18.dsc' dpkg_1.18.18.dsc 2032 SHA256:9c1d708ce829901d5eb012e976aace86554d01bb0643edd1b7a05c261e42d60c
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.18.18.tar.xz' dpkg_1.18.18.tar.xz 4501988 SHA256:c88b61e3d4660500753142689e8ddbeff1c731f29549f3338e6975f655936ff5
```

Likely also available for browsing at:

- https://sources.debian.net/src/dpkg/1.18.18/
- https://sources.debian.net/src/dpkg/1.18.18/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `e2fsprogs=1.43.3-1`

Binary Packages:

- `e2fslibs:amd64=1.43.3-1`
- `e2fsprogs=1.43.3-1`
- `libcomerr2:amd64=1.43.3-1`
- `libss2:amd64=1.43.3-1`

Licenses: (parsed from: `/usr/share/doc/e2fslibs/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcomerr2/copyright`, `/usr/share/doc/libss2/copyright`)

- `GPL-2`
- `LGPL-2`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.43.3-1
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.3-1.dsc' e2fsprogs_1.43.3-1.dsc 2028 SHA256:d15bc76f9790bad181770238e71242c1987e779941acccedf4beaefa22adb84b
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.3.orig.tar.gz' e2fsprogs_1.43.3.orig.tar.gz 7405892 SHA256:ce8ef1bbb0d4730f170167284fda156ac9d6bf18db2750eb94af619a81b19927
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.3-1.debian.tar.xz' e2fsprogs_1.43.3-1.debian.tar.xz 75724 SHA256:4b8d31ae65c7fa29d9b9a2cec022d272cec1d00e3c789849094467b6c408dbb5
```

Likely also available for browsing at:

- https://sources.debian.net/src/e2fsprogs/1.43.3-1/
- https://sources.debian.net/src/e2fsprogs/1.43.3-1/debian/copyright (for direct copyright/license information)

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

### `dpkg` source package: `expat=2.2.0-2`

Binary Packages:

- `libexpat1:amd64=2.2.0-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris expat=2.2.0-2
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.2.0-2.dsc' expat_2.2.0-2.dsc 2267 SHA256:16163e949855ce70b7fc5092e8c75ffc405d8f02162badc3ba5fe6ea669b1959
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.2.0.orig.tar.bz2' expat_2.2.0.orig.tar.bz2 414352 SHA256:d9e50ff2d19b3538bd2127902a89987474e1a4db8e43a66a4d1a712ab9a504ff
'http://deb.debian.org/debian/pool/main/e/expat/expat_2.2.0-2.debian.tar.xz' expat_2.2.0-2.debian.tar.xz 10676 SHA256:3e99516590c6719bcba54281b16900be19651b7d3b29ba8e4e9632306235f29b
```

Likely also available for browsing at:

- https://sources.debian.net/src/expat/2.2.0-2/
- https://sources.debian.net/src/expat/2.2.0-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `explorercanvas=0.r3-4`

Binary Packages:

- `libjs-excanvas=0.r3-4`

Licenses: (parsed from: `/usr/share/doc/libjs-excanvas/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris explorercanvas=0.r3-4
'http://deb.debian.org/debian/pool/main/e/explorercanvas/explorercanvas_0.r3-4.dsc' explorercanvas_0.r3-4.dsc 2000 SHA256:d168011ed1f110f82b5039a6b070167f1f262d2a35d7fa25a6b5462f73761637
'http://deb.debian.org/debian/pool/main/e/explorercanvas/explorercanvas_0.r3.orig.tar.gz' explorercanvas_0.r3.orig.tar.gz 50748 SHA256:687af8084781b8eb3451fc55c88f6dfddc2b84428d197daf2c4c33fd5c55fed8
'http://deb.debian.org/debian/pool/main/e/explorercanvas/explorercanvas_0.r3-4.debian.tar.xz' explorercanvas_0.r3-4.debian.tar.xz 2040 SHA256:afcaa3e229d9b423988fc30439aeee1599c9dac8ad94430309404f9cf9f0c11f
```

Likely also available for browsing at:

- https://sources.debian.net/src/explorercanvas/0.r3-4/
- https://sources.debian.net/src/explorercanvas/0.r3-4/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `findutils=4.6.0+git+20161106-1`

Binary Packages:

- `findutils=4.6.0+git+20161106-1`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `GFDL-1.3`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `gcc-5=5.4.1-4`

Binary Packages:

- `gcc-5-base:amd64=5.4.1-4`

Licenses: (parsed from: `/usr/share/doc/gcc-5-base/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `gcc-6=6.2.1-5`

Binary Packages:

- `gcc-6-base:amd64=6.2.1-5`
- `libgcc1:amd64=1:6.2.1-5`
- `libstdc++6:amd64=6.2.1-5`

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

### `dpkg` source package: `git=1:2.11.0-2`

Binary Packages:

- `git=1:2.11.0-2`
- `git-man=1:2.11.0-2`

Licenses: (parsed from: `/usr/share/doc/git/copyright`, `/usr/share/doc/git-man/copyright`)

- `Apache-2.0`
- `Artistic`
- `Artistic-1`
- `BSD-2-clause`
- `Boost`
- `EDL-1.0`
- `Expat`
- `GPL`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `dlmalloc`
- `mingw-runtime`

Source:

```console
$ apt-get source -qq --print-uris git=1:2.11.0-2
'http://deb.debian.org/debian/pool/main/g/git/git_2.11.0-2.dsc' git_2.11.0-2.dsc 2871 SHA256:98551f60e49b1447ea2a937cd29c359cfc3de963150dde9343e45c6414b31ddd
'http://deb.debian.org/debian/pool/main/g/git/git_2.11.0.orig.tar.xz' git_2.11.0.orig.tar.xz 4197984 SHA256:7e7e8d69d494892373b87007674be5820a4bc1ef596a0117d03ea3169119fd0b
'http://deb.debian.org/debian/pool/main/g/git/git_2.11.0-2.debian.tar.xz' git_2.11.0-2.debian.tar.xz 519184 SHA256:2787c4f6a8ceeb0dc78edaffbc7320947bc9674a784c69c45736a05f95aae346
```

Likely also available for browsing at:

- https://sources.debian.net/src/git/1:2.11.0-2/
- https://sources.debian.net/src/git/1:2.11.0-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `glibc=2.24-8`

Binary Packages:

- `libc-bin=2.24-8`
- `libc6:amd64=2.24-8`
- `multiarch-support=2.24-8`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/multiarch-support/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.24-8
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.24-8.dsc' glibc_2.24-8.dsc 8329 SHA256:c96e0bc7ef320e79819f7e94bcece804bae729c1ee36950d19b6927fdbe4cd1d
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.24.orig.tar.xz' glibc_2.24.orig.tar.xz 13921912 SHA256:ed71e8afd2b270f7947a2cea2457a31e1ca4fac08e2731d80edd7ec1730ec84f
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.24-8.debian.tar.xz' glibc_2.24-8.debian.tar.xz 965768 SHA256:2f3c1cfe0b4284400f4c91cd7ee82d6c1c7e5e6f627337e453b34b3bdf18e88e
```

Likely also available for browsing at:

- https://sources.debian.net/src/glibc/2.24-8/
- https://sources.debian.net/src/glibc/2.24-8/debian/copyright (for direct copyright/license information)

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

### `dpkg` source package: `gnupg2=2.1.17-2`

Binary Packages:

- `gpgv=2.1.17-2`

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
$ apt-get source -qq --print-uris gnupg2=2.1.17-2
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.1.17-2.dsc' gnupg2_2.1.17-2.dsc 3145 SHA256:466620fa204d41b8b45ba2711ed701dcac50459dbaee9081fa7920ca0546de98
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.1.17.orig.tar.bz2' gnupg2_2.1.17.orig.tar.bz2 5970042 SHA256:c5dc54db432209fa8f9bdb071c8fb60a765ff28e363150e30bdd4543160243cb
'http://deb.debian.org/debian/pool/main/g/gnupg2/gnupg2_2.1.17-2.debian.tar.bz2' gnupg2_2.1.17-2.debian.tar.bz2 50710 SHA256:0b9f1a605b870e356cc7bc6ceb0fc5edd195ca78fd8dee5df73958bad9f19b01
```

Likely also available for browsing at:

- https://sources.debian.net/src/gnupg2/2.1.17-2/
- https://sources.debian.net/src/gnupg2/2.1.17-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `gnutls28=3.5.7-3`

Binary Packages:

- `libgnutls30:amd64=3.5.7-3`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `grep=2.27-1`

Binary Packages:

- `grep=2.27-1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `gzip=1.6-5`

Binary Packages:

- `gzip=1.6-5`

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

- `hostname=3.18`

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

### `dpkg` source package: `icu=57.1-5`

Binary Packages:

- `libicu57:amd64=57.1-5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris icu=57.1-5
'http://deb.debian.org/debian/pool/main/i/icu/icu_57.1-5.dsc' icu_57.1-5.dsc 2105 SHA256:46210c5e254e13e38948bad23ce19ad773e54872af1489eb6752e44ea74d16ef
'http://deb.debian.org/debian/pool/main/i/icu/icu_57.1.orig.tar.gz' icu_57.1.orig.tar.gz 22360664 SHA256:ff8c67cb65949b1e7808f2359f2b80f722697048e90e7cfc382ec1fe229e9581
'http://deb.debian.org/debian/pool/main/i/icu/icu_57.1-5.debian.tar.xz' icu_57.1-5.debian.tar.xz 30696 SHA256:bb40a948b1ad71a4a597231fbf4c94ebc1ed9a17c5b4ff897fdf1b066c0b387b
```

Likely also available for browsing at:

- https://sources.debian.net/src/icu/57.1-5/
- https://sources.debian.net/src/icu/57.1-5/debian/copyright (for direct copyright/license information)

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

### `dpkg` source package: `init-system-helpers=1.46`

Binary Packages:

- `init-system-helpers=1.46`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


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

### `dpkg` source package: `libbsd=0.8.3-1`

Binary Packages:

- `libbsd0:amd64=0.8.3-1`

Licenses: (parsed from: `/usr/share/doc/libbsd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-2-clause-author`
- `BSD-2-clause-verbatim`
- `BSD-3-clause`
- `BSD-3-clause-Peter-Wemm`
- `BSD-3-clause-Regents`
- `BSD-4-clause-Christopher-G-Demetriou`
- `BSD-4-clause-Niels-Provos`
- `BSD-5-clause-Peter-Wemm`
- `Beerware`
- `Expat`
- `ISC`
- `ISC-Original`
- `public-domain`
- `public-domain-Colin-Plumb`

Source:

```console
$ apt-get source -qq --print-uris libbsd=0.8.3-1
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.8.3-1.dsc' libbsd_0.8.3-1.dsc 2212 SHA256:8b53b3731a95f00a0f47195e6afdf8dc4bcb3ed3b9b0d3e7046d8c9c98e5c8f2
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.8.3.orig.tar.xz' libbsd_0.8.3.orig.tar.xz 356772 SHA256:934b634f4dfd865b6482650b8f522c70ae65c463529de8be907b53c89c3a34a8
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.8.3.orig.tar.xz.asc' libbsd_0.8.3.orig.tar.xz.asc 819 SHA256:c0e26a577d19404d05515e0559b9224106a59ecd30910d6896694c4a5a4b021d
'http://deb.debian.org/debian/pool/main/libb/libbsd/libbsd_0.8.3-1.debian.tar.xz' libbsd_0.8.3-1.debian.tar.xz 14924 SHA256:c2beb8b2c4678c9f700b09834d1083fb6b1f883b112e493bd1ed1177355114fc
```

Likely also available for browsing at:

- https://sources.debian.net/src/libbsd/0.8.3-1/
- https://sources.debian.net/src/libbsd/0.8.3-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libcap-ng=0.7.7-3`

Binary Packages:

- `libcap-ng0:amd64=0.7.7-3`

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

### `dpkg` source package: `libedit=3.1-20160903-2`

Binary Packages:

- `libedit2:amd64=3.1-20160903-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `liberror-perl=0.17024-1`

Binary Packages:

- `liberror-perl=0.17024-1`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

Source:

```console
$ apt-get source -qq --print-uris liberror-perl=0.17024-1
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17024-1.dsc' liberror-perl_0.17024-1.dsc 2193 SHA256:3d269abc34facfde4e4caf5d2eac38dbce07739d3fe2167ff982140af513d17e
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17024.orig.tar.gz' liberror-perl_0.17024.orig.tar.gz 31269 SHA256:074db7c783a67b0667eca64a4f6a0c3de94998afc92c01d6453163eb04b9150d
'http://deb.debian.org/debian/pool/main/libe/liberror-perl/liberror-perl_0.17024-1.debian.tar.xz' liberror-perl_0.17024-1.debian.tar.xz 4028 SHA256:7b490f3655df007a1153883608161822036837eaf49f7d6014d3a096be4a65cb
```

Likely also available for browsing at:

- https://sources.debian.net/src/liberror-perl/0.17024-1/
- https://sources.debian.net/src/liberror-perl/0.17024-1/debian/copyright (for direct copyright/license information)

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

### `dpkg` source package: `libgcrypt20=1.7.5-2`

Binary Packages:

- `libgcrypt20:amd64=1.7.5-2`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.7.5-2
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.5-2.dsc' libgcrypt20_1.7.5-2.dsc 2914 SHA256:6946764a678f67c38505ffdd1e2fec1023222094a370a3b9310f7e6133acfe62
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.5.orig.tar.bz2' libgcrypt20_1.7.5.orig.tar.bz2 2883968 SHA256:d1fea4128beef2bb30a470af6bafabccc503ced350534fb9dd8f5a53ffbae800
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.5.orig.tar.bz2.asc' libgcrypt20_1.7.5.orig.tar.bz2.asc 620 SHA256:8f320166f6e04a2a0c4252ab85e17d860dc309c827f8dfa54d3a29a14511b929
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.7.5-2.debian.tar.xz' libgcrypt20_1.7.5-2.debian.tar.xz 30352 SHA256:e769625bdd2c9257fa26159eea905d23a39b8bbce3796872df09ed09d682dc5d
```

Likely also available for browsing at:

- https://sources.debian.net/src/libgcrypt20/1.7.5-2/
- https://sources.debian.net/src/libgcrypt20/1.7.5-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `libgpg-error=1.26-1`

Binary Packages:

- `libgpg-error0:amd64=1.26-1`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `GPL-2.1+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.26-1
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.26-1.dsc' libgpg-error_1.26-1.dsc 2454 SHA256:76661ccfdd36ac41cf889d8ad4b2a31c39f2e78115e27ae0eda4e31df896f6c3
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.26.orig.tar.bz2' libgpg-error_1.26.orig.tar.bz2 798096 SHA256:4c4bcbc90116932e3acd37b37812d8653b1b189c1904985898e860af818aee69
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.26-1.debian.tar.xz' libgpg-error_1.26-1.debian.tar.xz 12732 SHA256:7c974a57441cb9c1f47f61e91023b582089747062f642424e244dc73e160b917
```

Likely also available for browsing at:

- https://sources.debian.net/src/libgpg-error/1.26-1/
- https://sources.debian.net/src/libgpg-error/1.26-1/debian/copyright (for direct copyright/license information)

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

### `dpkg` source package: `libpsl=0.16.1-1`

Binary Packages:

- `libpsl5:amd64=0.16.1-1`

Licenses: (parsed from: `/usr/share/doc/libpsl5/copyright`)

- `Chromium`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `libselinux=2.6-3`

Binary Packages:

- `libselinux1:amd64=2.6-3`

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

### `dpkg` source package: `libtasn1-6=4.9-4`

Binary Packages:

- `libtasn1-6:amd64=4.9-4`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


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

- `liblz4-1:amd64=0.0~r131-2`

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

- `mawk=1.3.3-17`

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

### `dpkg` source package: `mercurial=4.0-1`

Binary Packages:

- `mercurial=4.0-1`
- `mercurial-common=4.0-1`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=4.0-1
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_4.0-1.dsc' mercurial_4.0-1.dsc 2364 SHA256:ff0e5c095bc7968180186caae755a7db258d474fc3cec759c2043ca53770db0f
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_4.0.orig.tar.gz' mercurial_4.0.orig.tar.gz 4850316 SHA256:24be080745230840f214d93e9f9fb4e25510f9abbbec2e56fab18543fedc43a7
'http://deb.debian.org/debian/pool/main/m/mercurial/mercurial_4.0-1.debian.tar.xz' mercurial_4.0-1.debian.tar.xz 95148 SHA256:2ebf7404aec85e37a751950678b12df1a6fd7c3b7fa405e87673cb4eaabdf2b8
```

Likely also available for browsing at:

- https://sources.debian.net/src/mercurial/4.0-1/
- https://sources.debian.net/src/mercurial/4.0-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `mime-support=3.60`

Binary Packages:

- `mime-support=3.60`

Licenses: (parsed from: `/usr/share/doc/mime-support/copyright`)

- `Bellcore`
- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris mime-support=3.60
'http://deb.debian.org/debian/pool/main/m/mime-support/mime-support_3.60.dsc' mime-support_3.60.dsc 1605 SHA256:1c3c61f6943b130ee6518facac394b733661975955b84af640b78fa354d7595d
'http://deb.debian.org/debian/pool/main/m/mime-support/mime-support_3.60.tar.gz' mime-support_3.60.tar.gz 36840 SHA256:f31d81f68dc007f56567cc14fb3b2effbd42d1dd087e414508e14e33d1a6a3a4
```

Likely also available for browsing at:

- https://sources.debian.net/src/mime-support/3.60/
- https://sources.debian.net/src/mime-support/3.60/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `ncurses=6.0+20161126-1`

Binary Packages:

- `libncurses5:amd64=6.0+20161126-1`
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

- `libhogweed4:amd64=3.3-1`
- `libnettle6:amd64=3.3-1`

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

### `dpkg` source package: `nghttp2=1.17.0-1`

Binary Packages:

- `libnghttp2-14:amd64=1.17.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `SIL-OFL-1.1`
- `all-permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `openldap=2.4.44+dfsg-2`

Binary Packages:

- `libldap-2.4-2:amd64=2.4.44+dfsg-2`
- `libldap-common=2.4.44+dfsg-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `openssh=1:7.4p1-5`

Binary Packages:

- `openssh-client=1:7.4p1-5`

Licenses: (parsed from: `/usr/share/doc/openssh-client/copyright`)

- `BSD-3-clause`
- `Beer-ware`
- `CORE-SDI-BSD-style`
- `Expat-with-advertising-restriction`
- `GPL-2 with OpenSSH-linking exception`
- `Mazieres-BSD-style`
- `OpenSSH`
- `Powell-BSD-style`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openssh=1:7.4p1-5
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_7.4p1-5.dsc' openssh_7.4p1-5.dsc 2956 SHA256:4db3672c393dc69944a68e82773519d37c31d67c5f003fb03516e038347a7427
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_7.4p1.orig.tar.gz' openssh_7.4p1.orig.tar.gz 1511780 SHA256:1b1fc4a14e2024293181924ed24872e6f2e06293f3e8926a376b8aec481f19d1
'http://deb.debian.org/debian/pool/main/o/openssh/openssh_7.4p1-5.debian.tar.xz' openssh_7.4p1-5.debian.tar.xz 157404 SHA256:7cd48ba265be55eac54956ee2cb94c265f1885c74af328e2eadd73ce44357955
```

Likely also available for browsing at:

- https://sources.debian.net/src/openssh/1:7.4p1-5/
- https://sources.debian.net/src/openssh/1:7.4p1-5/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `openssl1.0=1.0.2j-4`

Binary Packages:

- `libssl1.0.2:amd64=1.0.2j-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openssl1.0=1.0.2j-4
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2j-4.dsc' openssl1.0_1.0.2j-4.dsc 2468 SHA256:19d9da65e37d460b94cbfb7f7fd306ede46e2d57ea8c5d0fc040ace56ff98cf5
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2j.orig.tar.gz' openssl1.0_1.0.2j.orig.tar.gz 5307912 SHA256:e7aff292be21c259c6af26469c7a9b3ba26e9abaaffd325e3dccc9785256c431
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2j.orig.tar.gz.asc' openssl1.0_1.0.2j.orig.tar.gz.asc 473 SHA256:b3551e17fef7df2eb901aa9c1cbc41e5cf7c9d5d10e546936145f24d1e52efdc
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2j-4.debian.tar.xz' openssl1.0_1.0.2j-4.debian.tar.xz 74788 SHA256:591263249b907f9b39964bfa3fda94735f5f315b1bb47bf80d5f6e458a5262ef
```

Likely also available for browsing at:

- https://sources.debian.net/src/openssl1.0/1.0.2j-4/
- https://sources.debian.net/src/openssl1.0/1.0.2j-4/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `openssl=1.1.0c-2`

Binary Packages:

- `libssl1.1:amd64=1.1.0c-2`
- `openssl=1.1.0c-2`

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

Source:

```console
$ apt-get source -qq --print-uris pam=1.1.8-3.5
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.1.8-3.5.dsc' pam_1.1.8-3.5.dsc 2572 SHA256:9f7dff8ae2e0a20e4d7ad267d2843aefed721b06c56276e9308a276e1a04c6d0
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.1.8.orig.tar.gz' pam_1.1.8.orig.tar.gz 1892765 SHA256:4183409a450708a976eca5af561dbf4f0490141a08e86e4a1e649c7c1b094876
'http://deb.debian.org/debian/pool/main/p/pam/pam_1.1.8-3.5.diff.gz' pam_1.1.8-3.5.diff.gz 139150 SHA256:6991af2b57eeffbe35a176c48e6c926631886eba4b8e33ae2eaffda44d7eb98e
```

Likely also available for browsing at:

- https://sources.debian.net/src/pam/1.1.8-3.5/
- https://sources.debian.net/src/pam/1.1.8-3.5/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `pcre3=2:8.39-2`

Binary Packages:

- `libpcre3:amd64=2:8.39-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre3=2:8.39-2
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39-2.dsc' pcre3_8.39-2.dsc 2133 SHA256:8c5ba4886410322adb13986748280e95fb9334bb5b86aeee6b4ba9295144eb12
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39.orig.tar.bz2' pcre3_8.39.orig.tar.bz2 1560758 SHA256:b858099f82483031ee02092711689e7245586ada49e534a06e678b8ea9549e8b
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39-2.debian.tar.gz' pcre3_8.39-2.debian.tar.gz 23765 SHA256:375c8c6c746553dd3c7364d53c4e85f68694c58763e4bc541821060cbb52eef6
```

Likely also available for browsing at:

- https://sources.debian.net/src/pcre3/2:8.39-2/
- https://sources.debian.net/src/pcre3/2:8.39-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `perl=5.24.1~rc4-1`

Binary Packages:

- `libperl5.24:amd64=5.24.1~rc4-1`
- `perl=5.24.1~rc4-1`
- `perl-base=5.24.1~rc4-1`
- `perl-modules-5.24=5.24.1~rc4-1`

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `procps=2:3.3.12-3`

Binary Packages:

- `libprocps6:amd64=2:3.3.12-3`
- `procps=2:3.3.12-3`

Licenses: (parsed from: `/usr/share/doc/libprocps6/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:3.3.12-3
'http://deb.debian.org/debian/pool/main/p/procps/procps_3.3.12-3.dsc' procps_3.3.12-3.dsc 2118 SHA256:5bff9bf045fb88118e5fe69df1ed1d092c49b258ebae5368222a16900288f12e
'http://deb.debian.org/debian/pool/main/p/procps/procps_3.3.12.orig.tar.xz' procps_3.3.12.orig.tar.xz 840540 SHA256:042fcc93e1850aee4c193c51c03f369293fb64fe47e37b38852be6693d12a3af
'http://deb.debian.org/debian/pool/main/p/procps/procps_3.3.12-3.debian.tar.xz' procps_3.3.12-3.debian.tar.xz 27260 SHA256:5907253fba4f11755b60d7d47ffd8212564d7e2c692dcfffc951e4026c465f9e
```

Likely also available for browsing at:

- https://sources.debian.net/src/procps/2:3.3.12-3/
- https://sources.debian.net/src/procps/2:3.3.12-3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `python-defaults=2.7.13-1`

Binary Packages:

- `libpython-stdlib:amd64=2.7.13-1`
- `python=2.7.13-1`
- `python-minimal=2.7.13-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `python2.7=2.7.13-1`

Binary Packages:

- `libpython2.7-minimal:amd64=2.7.13-1`
- `libpython2.7-stdlib:amd64=2.7.13-1`
- `python2.7=2.7.13-1`
- `python2.7-minimal=2.7.13-1`

Licenses: (parsed from: `/usr/share/doc/libpython2.7-minimal/copyright`, `/usr/share/doc/libpython2.7-stdlib/copyright`, `/usr/share/doc/python2.7/copyright`, `/usr/share/doc/python2.7-minimal/copyright`)

- `# Licensed to PSF under a Contributor Agreement`
- `* Permission to use this software in any way is granted without`
- `Apache`
- `Apache-2`
- `Apache-2.0`
- `Expat`
- `GPL-2`
- `ISC`
- `LGPL-2.1+`
- `PSF-2`
- `Permission is hereby granted, free of charge, to any person obtaining`
- `Python`
- `This software is provided 'as-is', without any express`
- `This software is provided as-is, without express`
- `implied`
- `see above, some license as Python`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `readline=7.0-1`

Binary Packages:

- `libreadline7:amd64=7.0-1`
- `readline-common=7.0-1`

Licenses: (parsed from: `/usr/share/doc/libreadline7/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-1`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-1`

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

### `dpkg` source package: `sed=4.2.2-8`

Binary Packages:

- `sed=4.2.2-8`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


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

### `dpkg` source package: `serf=1.3.9-1`

Binary Packages:

- `libserf-1-1:amd64=1.3.9-1`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `shadow=1:4.2-3.3`

Binary Packages:

- `login=1:4.2-3.3`
- `passwd=1:4.2-3.3`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `six=1.10.0-3`

Binary Packages:

- `python-six=1.10.0-3`

Licenses: (parsed from: `/usr/share/doc/python-six/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris six=1.10.0-3
'http://deb.debian.org/debian/pool/main/s/six/six_1.10.0-3.dsc' six_1.10.0-3.dsc 2158 SHA256:71f2d5ff8b999c471cc2e92712befe482351a5ae226321e0e795bc683c8729cb
'http://deb.debian.org/debian/pool/main/s/six/six_1.10.0.orig.tar.gz' six_1.10.0.orig.tar.gz 29630 SHA256:105f8d68616f8248e24bf0e9372ef04d3cc10104f1980f54d57b2ce73a5ad56a
'http://deb.debian.org/debian/pool/main/s/six/six_1.10.0-3.debian.tar.xz' six_1.10.0-3.debian.tar.xz 3668 SHA256:860cc57244ea4e69eb4ee3ad1b823472c20d868c1cc25745b236ba6c9e1f3563
```

Likely also available for browsing at:

- https://sources.debian.net/src/six/1.10.0-3/
- https://sources.debian.net/src/six/1.10.0-3/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `sqlite3=3.15.2-2`

Binary Packages:

- `libsqlite3-0:amd64=3.15.2-2`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


### `dpkg` source package: `subversion=1.9.5-1`

Binary Packages:

- `libsvn1:amd64=1.9.5-1`
- `subversion=1.9.5-1`

Licenses: (parsed from: `/usr/share/doc/libsvn1/copyright`, `/usr/share/doc/subversion/copyright`)

- `Apache-2.0`
- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris subversion=1.9.5-1
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.9.5-1.dsc' subversion_1.9.5-1.dsc 3049 SHA256:27f998d99a5dc7311fa53085c580a1db81ed82ea4d4ffcaa3eddd9b3c937ed43
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.9.5.orig.tar.gz' subversion_1.9.5.orig.tar.gz 10615674 SHA256:280ba586c5d51d7b976b65d22d5e8e42f3908ed1c968d71120dcf534ce857a83
'http://deb.debian.org/debian/pool/main/s/subversion/subversion_1.9.5-1.diff.gz' subversion_1.9.5-1.diff.gz 2534370 SHA256:1d876bf34c60fdd836dbc6c7b86a0c96fd6458393074c73137266f2d64865350
```

Likely also available for browsing at:

- https://sources.debian.net/src/subversion/1.9.5-1/
- https://sources.debian.net/src/subversion/1.9.5-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `systemd=232-8`

Binary Packages:

- `libsystemd0:amd64=232-8`
- `libudev1:amd64=232-8`

Licenses: (parsed from: `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`)

- `CC0`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris systemd=232-8
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_232-8.dsc' systemd_232-8.dsc 4653 SHA256:3ca60d621830e7df68aff42fcd7e09ad3eeca54ce15cade2f5190ad5d9208581
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_232.orig.tar.gz' systemd_232.orig.tar.gz 4529048 SHA256:1172c7c7d5d72fbded53186e7599d5272231f04cc8b72f9a0fb2c5c20dfc4880
'http://deb.debian.org/debian/pool/main/s/systemd/systemd_232-8.debian.tar.xz' systemd_232-8.debian.tar.xz 131676 SHA256:5dcb0e19e7a33e15ad5cea4b9806c4705b78ebe87a0478fbdf7d85c20fc29bab
```

Likely also available for browsing at:

- https://sources.debian.net/src/systemd/232-8/
- https://sources.debian.net/src/systemd/232-8/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `sysvinit=2.88dsf-59.8`

Binary Packages:

- `sysvinit-utils=2.88dsf-59.8`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!


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

### `dpkg` source package: `tzdata=2016j-2`

Binary Packages:

- `tzdata=2016j-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tzdata=2016j-2
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2016j-2.dsc' tzdata_2016j-2.dsc 2005 SHA256:f3d5625674688b1bde68ba3e258102d69979a00a65ad3d0a78007668f19327a3
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2016j.orig.tar.gz' tzdata_2016j.orig.tar.gz 321185 SHA256:f5ee4e0f115f6c2faee1c4b16193a97338cbd1b503f2cea6c5a768c82ff39dc8
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2016j-2.debian.tar.xz' tzdata_2016j-2.debian.tar.xz 100588 SHA256:04b8920c2b2116806bc5b86c161299827e303f4018aac233c01d2503a94e4a53
```

Likely also available for browsing at:

- https://sources.debian.net/src/tzdata/2016j-2/
- https://sources.debian.net/src/tzdata/2016j-2/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `ucf=3.0036`

Binary Packages:

- `ucf=3.0036`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0036
'http://deb.debian.org/debian/pool/main/u/ucf/ucf_3.0036.dsc' ucf_3.0036.dsc 1343 SHA256:e67a8a3012ac357c7759dabd93d258422b1003bad8c3f17f25fc2a289eeda3bb
'http://deb.debian.org/debian/pool/main/u/ucf/ucf_3.0036.tar.xz' ucf_3.0036.tar.xz 65020 SHA256:34aa44416106f1205376918386b2896edf21dd42b633133b5f8fedecae17fca8
```

Likely also available for browsing at:

- https://sources.debian.net/src/ucf/3.0036/
- https://sources.debian.net/src/ucf/3.0036/debian/copyright (for direct copyright/license information)

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

### `dpkg` source package: `util-linux=2.29-1`

Binary Packages:

- `bsdutils=1:2.29-1`
- `libblkid1:amd64=2.29-1`
- `libfdisk1:amd64=2.29-1`
- `libmount1:amd64=2.29-1`
- `libsmartcols1:amd64=2.29-1`
- `libuuid1:amd64=2.29-1`
- `mount=2.29-1`
- `util-linux=2.29-1`

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
$ apt-get source -qq --print-uris util-linux=2.29-1
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.29-1.dsc' util-linux_2.29-1.dsc 3872 SHA256:83355cf6d188db9feac1842a82afef5c96935950f961b97838ecd2a7134d603e
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.29.orig.tar.xz' util-linux_2.29.orig.tar.xz 4249020 SHA256:2c59ea67cc7b564104f60532f6e0a95fe17a91acb870ba8fd7e986f273abf9e7
'http://deb.debian.org/debian/pool/main/u/util-linux/util-linux_2.29-1.debian.tar.xz' util-linux_2.29-1.debian.tar.xz 73256 SHA256:8eba5cdc8836b0c67a39ca9cffe735d2462e1a31dd577bc97cef787502812f38
```

Likely also available for browsing at:

- https://sources.debian.net/src/util-linux/2.29-1/
- https://sources.debian.net/src/util-linux/2.29-1/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `wget=1.18-4`

Binary Packages:

- `wget=1.18-4`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.18-4
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.18-4.dsc' wget_1.18-4.dsc 1870 SHA256:0c40295fd54d845b9c81c06b985f334771bd6e6d3d19007b251852aeff03b2a2
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.18.orig.tar.gz' wget_1.18.orig.tar.gz 3865525 SHA256:a00a65fab84cc46e24c53ce88c45604668a7a479276e037dc2f558e34717fb2d
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.18-4.debian.tar.xz' wget_1.18-4.debian.tar.xz 21408 SHA256:30f87c9465311bd1ab935dce7b1b6d9e1be3c9ff5c40a43f052f145a823debd9
```

Likely also available for browsing at:

- https://sources.debian.net/src/wget/1.18-4/
- https://sources.debian.net/src/wget/1.18-4/debian/copyright (for direct copyright/license information)

### `dpkg` source package: `xz-utils=5.2.2-1.2`

Binary Packages:

- `liblzma5:amd64=5.2.2-1.2`

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

### `dpkg` source package: `zlib=1:1.2.8.dfsg-4`

Binary Packages:

- `zlib1g:amd64=1:1.2.8.dfsg-4`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)
  If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.2.8.dfsg-4
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg-4.dsc' zlib_1.2.8.dfsg-4.dsc 2153 SHA256:1fe1021b16ef7dd17b5d593d1686335c706d15a6b19379e57831f1fec4d4cef4
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg.orig.tar.gz' zlib_1.2.8.dfsg.orig.tar.gz 361943 SHA256:2caecc2c3f1ef8b87b8f72b128a03e61c307e8c14f5ec9b422ef7914ba75cf9f
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg-4.debian.tar.xz' zlib_1.2.8.dfsg-4.debian.tar.xz 18108 SHA256:791f25b1cc3f731b5c26462f42f0937c94d74be56de96bcf1f01befdc6115ce7
```

Likely also available for browsing at:

- https://sources.debian.net/src/zlib/1:1.2.8.dfsg-4/
- https://sources.debian.net/src/zlib/1:1.2.8.dfsg-4/debian/copyright (for direct copyright/license information)
