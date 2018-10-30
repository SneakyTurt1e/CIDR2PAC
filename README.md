# CIDR2PAC

A es6 script for covering CIDRs list to PAC proxy script.

一个用于将 CIDR 列表文件转换为 PAC 自动代理文件的脚本。

## 使用姿势
* 本地部署

```sh
# 安装 node 6+ 与 npm
# 根据需求修改 index.js 文件中的 CIDR_PATH / DIST_PAC_PATH / PROXY 三个常量

git clone https://github.com/SneakyTurt1e/CIDR2PAC.git
cd ./CIDR2PAC
npm install
node ./

# 然后就可以在 DIST_PAC_PATH 找到你的 PAC 文件。
```

* 编译运行镜像
```sh
# 安装 docker.io 容器引擎
# 根据需求修改 index.js 文件中的 CIDR_PATH / DIST_PAC_PATH / PROXY 三个常量

git clone https://github.com/SneakyTurt1e/CIDR2PAC.git
cd ./CIDR2PAC
docker build -t tools/cidr2pac .
docker run -d -p 8123:8080 tools/cidr2pac
curl -o my.pac http://127.0.0.1:8123
# 目录下的 my.pac 就是你的 PAC 文件
```
