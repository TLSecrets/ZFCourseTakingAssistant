# ZFCourseTakingAssistant (TLSecrets 修改版)

本项目基于 [Void-JackLee/ZFCourseTakingAssistant](https://github.com/Void-JackLee/ZFCourseTakingAssistant) 复刻并修改，遵循 GNU General Public License v2.0 开源。

**原始项目作者**：VoidJackLee  
**修改者**：TLSecrets  
**修改日期**：2026-07-03  

---

## 🔧 本修改版的主要变更

基于原版 v1.1.4，本修改版进行了以下调整：

### ✅ 保留的核心功能
- 课程加载与解析
- 教学班浏览与队列管理（左侧课程列表 → 中间详情 → 右侧待抢队列）
- 一键抢课（手动触发）
- 捡漏（定时轮询）
- 从队列删除课程
- 安全补丁（HTML转义、`.append` 劫持）

### ✨ 新增与修复
- **队列点击同步**：点击右侧待抢队列中的教学班，详情面板正确显示课程信息。
- **本地持久化存储**：待抢队列保存在 `localStorage` 中，刷新页面自动恢复。
- **全局自动确认**：选课时的“确认提示”弹窗自动点击，无需手动干预。

---

## 📌 原始项目介绍（以下内容源自原项目）

# ZFCourseTakingAssistant
A script for Chinese University Student grabbing courses with Zheng Fang Educational administration system.

一款面向正方教学一体化教育服务系统（浙江中医药大学）的抢课脚本。

# Features

* 支持一键抢课（提前进入网站，预先选好要的课程，到了抢课的时间一键抢课）
* 支持捡漏（可以自动反复抢列表里的课）

> **程序仅供交流学习，请勿用作非法用途，一经发现将追究法律责任**

# Applicable

本脚本适用于**新版正方教学一体化教育服务系统**。

![主界面](pic/main.png)

目前仅测试过**浙江中医药大学**和**杭州电子科技大学**(此处感谢[@weixiabing](https://github.com/weixiabing ))的教务系统，欢迎其他学校的同学测试后提交issue。

## Environment

* Google Chrome
* Tampermonkey

建议使用安装了Tampermonkey(油猴脚本插件)的谷歌浏览器，其他浏览器没有测试过不敢保证稳定性。

**经测试，火狐浏览器也有不错的效果，安装Tampermonkey插件不需要翻墙，适合安利给妹纸。**

## Usage

1. 安装油猴子，安装本脚本 [https://github.com/TLSecrets/ZFCourseTakingAssistant/raw/main/抢课助手.user.js](https://github.com/TLSecrets/ZFCourseTakingAssistant/raw/main/%E6%8A%A2%E8%AF%BE%E5%8A%A9%E6%89%8B.user.js)

2. 访问你的选课网址，待他加载完毕后如图所示。（可以按F12打开控制台查看详情）![食用方法](pic/usage.jpg)

红色代表没有余量，白色代表还可以选。

**已知问题：如果过了好久都没显示，强制刷新（快捷键：control+shift+R/command+shift+R）即可，是缓存问题。**

# Development

## Environment

* Unix Base System(Linux/Unix/macOS)
* WebStorm
* node.js
* webpack
* css-loader
* style-loader

## Build

Run `build.py` script in project folder to build.

---

## 📄 许可证

本项目是 [Void-JackLee/ZFCourseTakingAssistant](https://github.com/Void-JackLee/ZFCourseTakingAssistant) 的修改版本，遵循 **GNU General Public License v2.0**。

- 您必须保留原始版权声明。
- 您必须标明修改内容。
- 修改后的代码必须以相同许可证（GPL v2）发布。
- 提供完整的源代码（本仓库已包含）。

完整的许可证文本请参见 [LICENSE](LICENSE) 文件。

**原始版权声明**：  
Copyright © VoidJackLee. All rights reserved.  
**修改部分版权**：© 2026 TLSecrets, under GPL v2.