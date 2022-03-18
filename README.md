# docker-openresty
基于 alpine 的 openresty docker镜像， build完成仅101M

# 进入容器
docker exec -it 76f3bfab1e86 /bin/sh
后面的路径不是/bin/bash

# 打包
docker build -t openresty:v1 .

# 运行
docker run -p 8081:80 -d openresty:v1

# 测试
curl http://127.0.0.1:8081/test/lua-block
