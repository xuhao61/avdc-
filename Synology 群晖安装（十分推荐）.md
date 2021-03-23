## 安装Docker

确保群晖安装了Docker，不回的话可以参考这篇[知乎教程](https://zhuanlan.zhihu.com/p/146175822)

## 下载文件

下载[avdc.db](https://github.com/xjasonlyu/avdc-api/raw/main/avdc.db)并上传至群晖，目录任意

## 添加镜像

映像 -> 新增 -> 从URL添加 -> 输入 `xjasonlyu/avdc-api`

[[/images/add.png]]

## 启动镜像

选择刚刚下载完成的镜像，点击启动，进入下图

[[/images/start.png]]

接着 高级设置 -> 端口设置，输入合适的端口号，例如`6666`

[[/images/6666.png]]

进入 卷 设置，添加文件，将之前下载的avdc.db载入

[[/images/db.png]]

【可选】环境设置

- `HTTP_PROXY`和`HTTPS_PROXY`，填入代理地址（如http://192.168.1.1:8080， 不需要的空着即可）
- `AVDC_TOKEN`，填入需要的token（不需要的空着即可）

[[/images/env.png]]

一路应用确定下一步，最后应用创建容器

[[/images/done.png]]

------

打开浏览器，输入`http://<你的IP>:6666`，看到JSON显示即为安装成功

[[/images/ok.png]]
