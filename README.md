# ssr_dockerfile

基于 [秋水逸冰](https://github.com/teddysun/shadowsocks_install) 发布的 [一键安装脚本](https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh) 写的 `Dockerfile`。

因为平时会在多个 vps 上都部署一套，有时候还经常换 vps，但是又比较懒，不想每次都得重新创建自己的配置文件，所以索性把配置文件直接放在镜像里面。

你要做的，Clone 下来之后在 `Dockerfile` 的同一目录创建你自己的 `shadowsocks.json` 文件，然后构建生成镜像，然后上传到你自己的 [Docker Hub](https://hub.docker.com/)。之后在任何主机上部署，pull 下你自己的镜像，run 即可，省去每次要修改你的配置的步骤。

> 注意：你创建的这个镜像中是包含了自己的配置文件信息的，所以最好是 `private`。

