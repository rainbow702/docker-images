# docker-images
存放各种 docker 基础镜像的 docker 及相关必要文件

## centos & jdk

* DockerFile7.0
* DockerFile7.1
* DockerFile7.6

因为在官方 docker hub 里没有找到官方的 centos&jdk 的结合版本，所以，就自己做了一个。
这三个为 **centos** 与 **jdk8** (jdk-8u172-linux-x64.tar.gz) 的镜像脚本，可通过下面的命令制作镜像
```
docker build --rm -t centos_jdk:7.0.1406_8u172 -f DockerFile7.0 .
```
三个脚本中其实只有 依赖的基础镜像(centos版本)不一样，其他都一样。

如果要使用其他版本的 jdk，只需用其他版本的 jdk包 替换这里的"jdk-8u172-linux-x64.tar.gz"，同时，将脚本里与jdk配置相关的地方进行修改即可。