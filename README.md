## Readme
[![Build Aria2 with msys2](https://github.com/ChiaYen-Kan/aria2-msys2-build/actions/workflows/aria2.yml/badge.svg?branch=master)](https://github.com/ChiaYen-Kan/aria2-msys2-build/actions/workflows/aria2.yml)

use github action to build [aria2](https://github.com/aria2/aria2) with current msys2 system

all lib use msys2 pre-build version without custom build

------------
### Versions

current (at 2023-3) build with 3 system lib and 3 tls lib

|  | wintls | openssl 3 | gnutls |
|-|:-:|:-------------:|:------:|
| mingw64 lib | win7/win10 |  win7/win10 | win7/win10 |
| ucrt64 lib | win7/win10 | win7/win10 | win7/win10 |
| clang64 lib | win7/win10 | win7/win10 | win10 |


------------
### About openssl 3
all openssl 3 file is put together, but need some config before run aria2


> **Step1**:
>
>> add a environment variable 'OPENSSL_MODULES' and set to 'ossl-modules' folder
>
> **Step2**:
>
>> run aria2c with '--ca-certificate' option and set to 'ca-bundle.crt' file


***reference:***

https://github.com/php/php-src/issues/9890#issuecomment-1303855417

https://github.com/aria2/aria2/issues/889

------------
### Issue
if have any issue, please report to [aria2](https://github.com/aria2/aria2/issues), this repository just a build script can't fix any issue

