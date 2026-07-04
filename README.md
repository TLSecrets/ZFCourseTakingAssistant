# ⚠️ 合规前置声明
> **阅读、下载、使用本项目即代表完全同意以下全部条款**
1. 本项目仅作为 **Python 网络编程、爬虫技术教学学习素材**，代码内自动化选课提交接口仅作技术原理演示；
2. **严禁**将本项目用于高校教务系统高频刷课、多账号批量代抢课程、有偿倒卖课程名额、囤积稀缺课程资源；
3. 各高校教务平台均有专属用户使用协议，自动化批量请求会扰乱正常教学秩序、冲击服务器稳定，使用者**账号封禁、校内纪律处分、治安乃至刑事追责全部由使用者自行承担**；
4. 项目作者**未诱导、未推广**任何主体将代码应用于真实选课场景，若使用者利用本代码实施各类违规操作，**所有行为与项目开发者无任何法律关联**；
5. 若收到校方、监管部门下架通知，作者将第一时间归档锁定仓库，永久停止更新维护。
---
# ZFCourseTakingAssistant (TLSecrets 修改版)
本项目基于 [Void-JackLee/ZFCourseTakingAssistant](https://github.com/Void-JackLee/ZFCourseTakingAssistant) 复刻并修改，遵循 GNU General Public License v2.0 开源。
**原始项目作者**：VoidJackLee  
**修改者**：TLSecrets  
**修改日期**：2026-07-04  
---
## 🔧 本修改版的主要变更
### ✨ 新增与修复
- **合规限流**：全局请求间隔强制 ≥3 秒，不可关闭修改，降低服务器冲击
- **强制合规弹窗**：脚本启动时弹出风险告知弹窗，用户必须同意方可使用
- **队列点击同步**：点击右侧待抢队列中的教学班，详情面板正确显示课程信息。
- **本地持久化存储**：待抢队列保存在 `localStorage` 中，刷新页面自动恢复。
- **全局自动确认**：选课时的"确认提示"及"警告提示"弹窗自动点击（默认关闭）。
### ✅ 保留的核心功能
- 课程加载与解析
- 教学班浏览与队列管理（左侧课程列表 → 中间详情 → 右侧待抢队列）
- 一键抢课（手动触发）
- 捡漏（定时轮询，限流≥3秒）
- 从队列删除课程
- 安全补丁（HTML转义、`.append` 劫持）
---
## 📌 原始项目介绍
# ZFCourseTakingAssistant
A script for Chinese University Student grabbing courses with Zheng Fang Educational administration system.
一款面向正方教学一体化教育服务系统的抢课脚本。
# Features
* 支持一键抢课（提前进入网站，预先选好要的课程，到了抢课的时间一键抢课）
* 支持捡漏（可以自动反复抢列表里的课，已内置≥3秒限流）
> **程序仅供交流学习，请勿用作非法用途，一经发现将追究法律责任**
# Applicable
本脚本适用于**新版正方教学一体化教育服务系统**。
![主界面](pic/main.png)
## Environment
* Google Chrome
* Tampermonkey
## Usage
1. 安装油猴子，安装本脚本 [https://github.com/TLSecrets/ZFCourseTakingAssistant/raw/main/抢课助手.user.js](https://github.com/TLSecrets/ZFCourseTakingAssistant/raw/main/%E6%8A%A2%E8%AF%BE%E5%8A%A9%E6%89%8B.user.js)
2. 访问你的选课网址。
---
## 📄 许可证
本项目是 [Void-JackLee/ZFCourseTakingAssistant](https://github.com/Void-JackLee/ZFCourseTakingAssistant) 的修改版本，遵循 **GNU General Public License v2.0**。
**原始版权声明**：Copyright © VoidJackLee. All rights reserved.  
**修改部分版权**：© 2026 TLSecrets, under GPL v2.
---
## 📎 相关文件
- [DISCLAIMER.md](DISCLAIMER.md) — 独立免责声明
- [LICENSE](LICENSE) — GPL v2.0 完整协议