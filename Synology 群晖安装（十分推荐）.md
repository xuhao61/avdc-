## 安装Docker

确保群晖安装了Docker，不回的话可以参考这篇[知乎教程](https://zhuanlan.zhihu.com/p/146175822)

## 添加镜像

映像 -> 新增 -> 从URL添加 -> 输入 `xjasonlyu/avdc-api`

[[/images/add.png]]

## 启动镜像

选择刚刚下载完成的镜像，点击启动，进入下图

[[/images/start.png]]

接着 高级设置 -> 端口设置，输入合适的端口号，例如`6666`

[[/images/6666.png]]

【可选】然后去环境设置，找到`AVDC_TOKEN`，填入需要的token（不需要的空着即可）

[[/images/token.png]]

一路应用确定下一步，最后应用创建容器

[[/images/done.png]]

------

打开浏览器，输入`http://<你的IP>:6666`，看到JSON显示即为安装成功

[[/images/ok.png]]
