<div align="center">
<img width="768" src="https://cdn.jsdelivr.net/gh/zhudpos/lede-actions/images/openwrt.png"/>
<h1>OpenWrt — 多设备固件云编译</h1>

<img src="https://img.shields.io/github/downloads/zhudpos/lede-actions/total.svg?style=for-the-badge&color=32C955"/>
<img src="https://img.shields.io/github/stars/zhudpos/lede-actions.svg?style=for-the-badge&color=orange"/>
<img src="https://img.shields.io/github/forks/zhudpos/lede-actions.svg?style=for-the-badge&color=ff69b4"/>
<img src="https://img.shields.io/github/license/zhudpos/lede-actions.svg?style=for-the-badge&color=blueviolet"/>

[![](https://img.shields.io/badge/-目录:-696969.svg)](#readme) [![](https://img.shields.io/badge/-项目说明-FFFFFF.svg)](#项目说明-) [![](https://img.shields.io/badge/-固件特色-FFFFFF.svg)](#固件特色-) [![](https://img.shields.io/badge/-固件下载-FFFFFF.svg)](#固件下载-) [![](https://img.shields.io/badge/-近期更新-FFFFFF.svg)](#近期更新-) [![](https://img.shields.io/badge/-插件预览-FFFFFF.svg)](#插件预览-) [![](https://img.shields.io/badge/-定制固件-FFFFFF.svg)](#定制固件-) [![](https://img.shields.io/badge/-特别提示-FFFFFF.svg)](#特别提示-) [![](https://img.shields.io/badge/-鸣谢-FFFFFF.svg)](#鸣谢-)
</div>


## 项目说明 [![](https://img.shields.io/badge/-项目基本介绍-FFFFFF.svg)](#项目说明-)
- 固件来源：[![Lean](https://img.shields.io/badge/Lede-Lean-ff69b4.svg?style=flat&logo=appveyor)](https://github.com/zhudpos/lede) [![P3TERX](https://img.shields.io/badge/OpenWrt-P3TERX-blueviolet.svg?style=flat&logo=appveyor)](https://github.com/P3TERX/Actions-OpenWrt) [![Flippy](https://img.shields.io/badge/Package-Flippy-orange.svg?style=flat&logo=appveyor)](https://github.com/unifreq/openwrt_packit) [![zhudpos](https://img.shields.io/badge/Build-zhudpos-32C955.svg?style=flat&logo=appveyor)](https://github.com/zhudpos/lede-actions)
- 项目使用 Github Actions 拉取 [Lean](https://github.com/zhudpos/lede) 的 Openwrt 源码仓库进行云编译
- 固件默认管理地址：`10.0.0.1` 默认用户：`root` 默认密码：`password`
- 提供适配于 ARMv8 电视盒子、Rockchip 平台、树莓派以及 X86 平台设备的 OpenWrt 固件
- ARMv8 盒子固件分为 [Mini版](https://github.com/zhudpos/lede-actions/releases/tag/ARMv8_MINI) 和 [Plus版](https://github.com/zhudpos/lede-actions/releases/tag/ARMv8_PLUS)，Mini 精简版以科学上网为主，Plus 多功能版插件多适合折腾
- ARMv8 系列固件包含 [F大](https://github.com/unifreq/openwrt_packit) 发布的所有已适配的盒子固件，并提供 Docker 镜像固件[➦使用方法](https://hub.docker.com/r/zhudpos/openwrt-aarch64)
- 固件集成的所有 ipk 插件全部打包在 Packages 文件中，可以在 [Releases](https://github.com/zhudpos/lede-actions/releases) 内进行下载
- 项目编译的固件插件为最新版本，最新版插件可能有 BUG，如果之前使用稳定则无需追新
- 第一次使用请采用全新安装，避免出现升级失败以及其他一些可能的 BUG


## 固件特色 [![](https://img.shields.io/badge/-本项目固件特色-FFFFFF.svg)](#固件特色-)
1. 固件每天定时自动编译，以确保获得最新体验
2. 集成部分常用有线、无线、3G / 4G 网卡驱动
3. 集成中文版 netdata 实时监控插件，小白也能轻松看懂系统概况
4. 集成 iStore 应用商店，可根据自己需求自由安装所需插件
5. 集成 Docker 服务，可在 OpenWrt 内自由部署 Docker 应用
6. 集成应用过滤插件，支持游戏、视频、聊天、下载等 APP 过滤
7. 集成在线用户插件，可查看所有在线用户 IP 地址与实时速率等
8. ARMv8 系列固件内置晶晨宝盒，支持在线更新固件及内核等


## 固件下载 [![](https://img.shields.io/badge/-编译状态及下载链接-FFFFFF.svg)](#固件下载-)
点击下表中 [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?style=flat&logo=hack-the-box)](https://github.com/zhudpos/lede-actions/releases) 即可跳转到该设备固件下载页面
| 平台+设备名称 | 固件编译状态 | 配置文件 | 固件下载 |
| :-------------: | :-------------: | :-------------: | :-------------: |
| [![](https://img.shields.io/badge/OpenWrt-X86_64位-32C955.svg?logo=openwrt)](https://github.com/zhudpos/lede-actions/blob/main/.github/workflows/X86_64-OpenWrt.yml) | [![](https://github.com/zhudpos/lede-actions/actions/workflows/X86_64-OpenWrt.yml/badge.svg)](https://github.com/zhudpos/lede-actions/actions/workflows/X86_64-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/zhudpos/lede-actions/blob/main/configs/x86_64.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/zhudpos/lede-actions/releases/tag/X86_64) |
| [![](https://img.shields.io/badge/OpenWrt-ARMv8_Mini-32C955.svg?logo=openwrt)](https://github.com/zhudpos/lede-actions/blob/main/.github/workflows/ARMv8-Mini-OpenWrt.yml) | [![](https://github.com/zhudpos/lede-actions/actions/workflows/ARMv8-Mini-OpenWrt.yml/badge.svg)](https://github.com/zhudpos/lede-actions/actions/workflows/ARMv8-Mini-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/zhudpos/lede-actions/blob/main/configs/armv8-mini.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/zhudpos/lede-actions/releases/tag/ARMv8_MINI) |
| [![](https://img.shields.io/badge/OpenWrt-ARMv8_Plus-32C955.svg?logo=openwrt)](https://github.com/zhudpos/lede-actions/blob/main/.github/workflows/ARMv8-Plus-OpenWrt.yml) | [![](https://github.com/zhudpos/lede-actions/actions/workflows/ARMv8-Plus-OpenWrt.yml/badge.svg)](https://github.com/zhudpos/lede-actions/actions/workflows/ARMv8-Plus-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/zhudpos/lede-actions/blob/main/configs/armv8-plus.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/zhudpos/lede-actions/releases/tag/ARMv8_PLUS) |
| [![](https://img.shields.io/badge/OpenWrt-Rockchip_平台-32C955.svg?logo=openwrt)](https://github.com/zhudpos/lede-actions/blob/main/.github/workflows/Rockchip-OpenWrt.yml) | [![](https://github.com/zhudpos/lede-actions/actions/workflows/Rockchip-OpenWrt.yml/badge.svg)](https://github.com/zhudpos/lede-actions/actions/workflows/Rockchip-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/zhudpos/lede-actions/blob/main/configs/rockchip.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/zhudpos/lede-actions/releases/tag/Rockchip) |
| [![](https://img.shields.io/badge/OpenWrt-树莓派_4B-32C955.svg?logo=openwrt)](https://github.com/zhudpos/lede-actions/blob/main/.github/workflows/RaspberryPi4-OpenWrt.yml) | [![](https://github.com/zhudpos/lede-actions/actions/workflows/RaspberryPi4-OpenWrt.yml/badge.svg)](https://github.com/zhudpos/lede-actions/actions/workflows/RaspberryPi4-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/zhudpos/lede-actions/blob/main/configs/rpi4.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/zhudpos/lede-actions/releases/tag/RaspberryPi4) |
| [![](https://img.shields.io/badge/OpenWrt-树莓派_3B/3B+-32C955.svg?logo=openwrt)](https://github.com/zhudpos/lede-actions/blob/main/.github/workflows/RaspberryPi3-OpenWrt.yml) | [![](https://github.com/zhudpos/lede-actions/actions/workflows/RaspberryPi3-OpenWrt.yml/badge.svg)](https://github.com/zhudpos/lede-actions/actions/workflows/RaspberryPi3-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/zhudpos/lede-actions/blob/main/configs/rpi3.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/zhudpos/lede-actions/releases/tag/RaspberryPi3) |


## 鸣谢 [![](https://img.shields.io/badge/-跪谢各大佬-FFFFFF.svg)](#鸣谢-)
| [ImmortalWrt](https://github.com/immortalwrt) | [zhudpos](https://github.com/zhudpos) | [P3TERX](https://github.com/P3TERX) | [Flippy](https://github.com/unifreq) |
| :-------------: | :-------------: | :-------------: | :-------------: |
| <img width="100" src="https://avatars.githubusercontent.com/u/53193414"/> | <img width="100" src="https://avatars.githubusercontent.com/u/31687149"/> | <img width="100" src="https://avatars.githubusercontent.com/u/25927179"/> | <img width="100" src="https://avatars.githubusercontent.com/u/39355261"/> |
| [Ophub](https://github.com/ophub) | [SuLingGG](https://github.com/SuLingGG) | [QiuSimons](https://github.com/QiuSimons) | [IvanSolis1989](https://github.com/IvanSolis1989) |
| <img width="100" src="https://avatars.githubusercontent.com/u/68696949"/> | <img width="100" src="https://avatars.githubusercontent.com/u/22287562"/> | <img width="100" src="https://avatars.githubusercontent.com/u/45143996"/> | <img width="100" src="https://avatars.githubusercontent.com/u/44228691"/> |


<a href="#readme">
<img src="https://img.shields.io/badge/-返回顶部-FFFFFF.svg" title="返回顶部" align="right"/>
</a>
