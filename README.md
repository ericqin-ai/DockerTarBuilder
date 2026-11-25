> This repository is a fork of [wukongdaily/DockerTarBuilder](https://github.com/wukongdaily/DockerTarBuilder). Original attribution and upstream links are retained. It is not presented as an original portfolio project.

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


## 本 fork 的操作说明

本项目来自上游 wukongdaily/DockerTarBuilder，保留原作者链接及 GPL-3.0 LICENSE。工作流实际执行指定平台镜像的 pull/save 和压缩，不是从 Dockerfile 构建新镜像。

1. 打开仓库 Actions，选择 amd64、arm32 或 arm64 对应工作流。
2. 选择 Run workflow，在 docker_images 输入镜像名称；多个镜像用英文逗号分隔。
3. 完成后下载运行页面的 docker-images-tar artifact；amd64 工作流设置保留 1 天，及时下载并检查其他架构工作流的保留设置。
4. 解压后使用 `docker load -i <image-file.tar>` 导入镜像，目标机器须匹配架构。

无需本地 Python 依赖；运行依赖 GitHub Actions 的 Ubuntu runner 与 Docker。请仅由可信维护者输入镜像名称：当前工作流将输入直接插入 shell，本次文档调整未修复该行为。上游教程和第三方镜像查询站点保留作为历史参考，实际可用性需另行确认。
