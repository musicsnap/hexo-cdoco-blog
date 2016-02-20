---
title: 编译php常见问题
date: 2016-02-20 16:37:44
tags:
 - php
category: php
---

### error 1

``` bash
checking for xml2-config path...
configure: error: xml2-config not found. Please check your libxml2 installation.

解决办法
yum install libxml2-devel.x86_64 -y
```
<!-- more -->

### error 2

``` bash
checking for pkg-config... /usr/bin/pkg-config
configure: error: Cannot find OpenSSL's <evp.h>

解决办法
yum install openssl.x86_64 openssl-devel.x86_64 -y
```
### error 3

``` bash
checking for BZip2 in default path... not found
configure: error: Please reinstall the BZip2 distribution

解决办法
yum install bzip2-devel.x86_64 -y
```

### error 4

``` bash
configure: error: Please reinstall the libcurl distribution -
    easy.h should be in <curl-dir>/include/curl/

解决办法
yum install libcurl.x86_64 libcurl-devel.x86_64 -y
```

### error 5

``` bash
checking whether to enable JIS-mapped Japanese font support in GD... no
checking for fabsf... yes
checking for floorf... yes
configure: error: jpeglib.h not found

解决办法
yum install libjpeg.x86_64 libpng.x86_64 freetype.x86_64 libjpeg-devel.x86_64 libpng-devel.x86_64 freetype-devel.x86_64 -y
```

### error 6

``` bash
checking for stdarg.h... (cached) yes
checking for mcrypt support... yes
configure: error: mcrypt.h not found. Please reinstall libmcrypt.

libmcrypt库没有安装 ，要是不能用yun安装的话  就要去下载个gz包 自己编译安装
ps：编译安装  ./configure --piefix=/usr/local/libmcrypt && make && make install
```
