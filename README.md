# Custom bsp platfrom for building Yocto for Raspberry pi

## Get BSP platform

```
$: mkdir ~/bin
$: curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
$: chmod a+x ~/bin/repo
$: PATH=${PATH}:~/bin
```

## Download BSP source

```
$: mkdir -p <customdir>/yocto-build/meta-rpi-bsp
$: cd <customdir>/yocto-build/meta-rpi-bsp
$: repo init -u git@github.com:yocro-rpi/meta-rpi-bsp.git -b main -m default.xml
$: repo sync -j4
```

## Get Yocto build configuration repository:

```
$: cd <customdir>/yocto-build
$: git clone git@github.com:yocro-rpi/yocto-conf.git
```

## Get Yocto Docker

```
$: cd <customdir>/yocto-build
$: git clone git@github.com:yocro-rpi/yocto-docker.git
```

See [README](https://github.com/yocro-rpi/yocto-docker/blob/main/README.md) how to use the docker to build Yocto
