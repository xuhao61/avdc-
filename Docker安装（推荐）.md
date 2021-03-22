## 开始

### 安装Docker

第一步先确保Docker已正确安装，具体参考[官方文档](https://docs.docker.com/get-docker/)

### 拉取镜像

```
docker pull ghcr.io/xjasonlyu/avdc-api:latest
```

### 运行镜像

1. 下载[avdc.db](https://github.com/xjasonlyu/avdc-api/raw/main/avdc.db)到本地
2. 根据本地情况更改，这里假设本地的HTTP代理地址位为`192.168.1.1:8080`，（不需要可以为空）
3. 假设需要设置TOKEN为`password`，（不需要可以为空）

```
docker run -d \
    -p 5000:5000 \
    -v $PWD/avdc.db:/avdc.db \
    -e HTTP_PROXY=http://192.168.1.1:8080 \
    -e HTTPS_PROXY=http://192.168.1.1:8080 \
    -e AVDC_TOKEN=password \
    ghcr.io/xjasonlyu/avdc:latest
```

### Done

打开浏览器，输入`http://<你的IP>:5000`，看到JSON显示即为安装成功
