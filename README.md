# r2-magic-run

This script is used to run radare2 from non-standard installed directory.

**Status**: [![Build Status][build_status]][travis_repo]

[build_status]: https://travis-ci.com/lzutao/r2-magic-run.svg?branch=master
[travis_repo]: https://travis-ci.com/lzutao/r2-magic-run

## Usage

In specific, first extract the radare2 package by:

```sh
wget -O 'radare2.deb' 'http://radare.mikelloc.com/get/2.9.0/radare2_2.9.0_amd64.deb'
dpkg -x 'radare2.deb' "${HOME}/builddir/radare2"
```

In your case, you need to modify the extracted directory and R2_PREFIX
in [r2](r2) file corresponding.

Then modify the PATH environment variable to point to the cloned repo:

```sh
git clone --depth=1 https://github.com/lzutao/r2-magic-run.git
PATH="${PATH}:$(realpath r2-magic-run/bin)"
export PATH
```
