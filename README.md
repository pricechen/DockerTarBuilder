https://cloud.tencent.com/developer/article/2434428
使用Github Action 构建docker镜像

三、使用Github Action 构建docker镜像
前置条件
1.可以访问Github，国内环境github时而抽风体质，如果没有科学环境也可以使用 https://github.com/521xueweihan/GitHub520 +SwitchHosts 基本还是可以使用的（有的话就当我没说）。 
2.有个github账号
3.免费版Action 每天能使用1小时，每个月33小时（基本上够用）。
参考博主悟空的日常：使用Github Action 构建docker镜像 http://wkdaily.cpolar.cn/archives/gc
1.要有一个github账号
没有账号就需要注册一个。
https://github.com
2.fork项目DockerTarBuilder
fork 叉子叉到自己的仓库中： https://github.com/wukongdaily/DockerTarBuilder

image-20240704165355729
3.点击 Actions
点击Actions选项卡，再点击同意

image-20240704165435226
选择平台，再填入镜像名

image-20240704165730904
4.下载镜像
点击 All workflows

image-20240704165853901

image-20240704165932860
5.解压恢复镜像
将下载好的压缩包上传到docker宿主机上。
代码语言：javascript
复制
解压
# unzip docker-images-tar.zip
Archive:  docker-images-tar.zip
  inflating: x86-64-images.tar.gz    
再解压：
#tar -zxvf x86-64-images.tar.gz
# ls -lh alpine:latest-amd64.tar
-rw------- 1 mysql 127 7.8M 7月   4 16:57 alpine:latest-amd64.tar
​
导入
# docker load < alpine:latest-amd64.tar
​
导入成功。
# docker images
REPOSITORY                                         TAG                 IMAGE ID            CREATED             SIZE
alpine                                             latest              a606584aa9aa        13 days ago         7.8 MB

From <https://cloud.tencent.com/developer/article/2434428> 

=====================================================================

![image](https://github.com/user-attachments/assets/3dc857e9-185b-4810-b37c-299596da8030)




[![GitHub](https://img.shields.io/github/license/wukongdaily/DockerTarBuilder.svg?label=LICENSE&logo=github&logoColor=%20)](https://github.com/wukongdaily/DockerTarBuilder/blob/master/LICENSE)
![GitHub Stars](https://img.shields.io/github/stars/wukongdaily/DockerTarBuilder.svg?style=flat&logo=appveyor&label=Stars&logo=github)
![GitHub Forks](https://img.shields.io/github/forks/wukongdaily/DockerTarBuilder.svg?style=flat&logo=appveyor&label=Forks&logo=github)

## 🤔 这是什么？
它是一个工作流。可快速构建指定架构/平台的docker镜像

## 使用说明
https://wkdaily.cpolar.cn/archives/gc
## 教学视频
https://www.bilibili.com/video/BV1EZ421M7mL
## 解压工具
> Windows 上推荐使用7zip<br>
> macOS 推荐使用MacZip<br>
> Linux上推荐直接用tar 命令

## 相关项目
https://github.com/wukongdaily/OrangePiShell
## 在哪里可以搜索或查询docker镜像的详细信息
### [查询镜像的详细信息 点击这里直达](https://docker.fxxk.dedyn.io/)
