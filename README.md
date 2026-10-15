# Project Genie 国内使用教程：谷歌 AI 游戏创作平台从 0 到上手

> 谷歌 DeepMind 的世界模型 Project Genie（Genie 3）：输入一句话或一张图，就能生成一个**可交互、可游玩**的虚拟世界——自己当主角在里面跑图。本教程讲清楚国内用户从「听说过」到「玩上」的完整路径：账号、订阅、网络环境，一步到位。

🤖 **想让你的 AI 帮你一步步操作？** 把本仓库链接（或 [README 原文](https://raw.githubusercontent.com/wuwenxux/project-genie-guide/main/README.md)）直接发给你的 AI 即可——仓库含 `llms.txt` 与 `AGENTS.md`，ChatGPT / Claude / Kimi 等都能直接读懂并照做。

## Project Genie 是什么

- 2026 年 1 月底谷歌 DeepMind 发布的实验性产品，底层是 Genie 3 通用世界模型，配合 Nano Banana Pro（图像）与 Gemini（语言理解）
- 用文本提示词或上传图片生成虚拟世界，可定义角色、第一/第三人称视角，在世界里边探索边实时生成
- 支持「世界重混」：在已有世界基础上改美术风格、改角色设定
- 2026 年 5 月 I/O 大会后新增 Street View 玩法：把真实街道变成奇幻世界（街景地点目前限美国）
- 定位是研究原型：单段世界时长有限，别拿它当 Unity 替代品——但它代表的方向已经足够震撼

## 上手三道门槛

| 门槛 | 说明 | 难度 |
|---|---|---|
| ① 网络环境 | 国内访问 Google 系服务需要稳定的科学上网，注册和支付环节对出口 IP 干净度敏感 | 本教程重点 |
| ② Google 账号 | 建议用干净的常用号，新注册号 + 异常 IP 容易触发风控 | 低 |
| ③ Google AI Ultra 订阅 | Project Genie 目前对 AI Ultra 订阅用户开放（美区定价 $249.99/月量级，以 Google 官网为准） | 主要是贵 |

### 第 1 步：搞定网络环境

这是国内用户唯一有技术含量的环节。三个要点：

1. **协议要新**：选 VLESS + Reality / WS + TLS 的服务，老协议（SS/SSR）在访问 Google 这类高风控站点时存活率低。
2. **客户端要新内核**：Windows / macOS 用 [Clash Verge Rev](https://github.com/clash-verge-rev/clash-verge-rev)，Android 用 Clash Meta for Android 或 sing-box，iOS 用 sing-box（免费）/ Stash / Shadowrocket。
3. **IP 要干净**：Google 对机房滥用的 IP 风控很严。免费节点、超低价万人骑机场，注册阶段就会被人机验证循环劝退。

**导入订阅（以 Clash Verge Rev 为例）**：

1. 复制订阅链接（一长串 URL）
2. Clash Verge Rev →「订阅 / Profiles」→ 粘贴导入
3. 选一个**美国节点**（AI Ultra 订阅和街景玩法都偏美区），开启系统代理
4. 浏览器开无痕窗口访问 google.com，能正常打开即环境就绪

> 我自己用的是 token 制的 [FrogLeap](https://fastergamer.click)：免注册，下单拿 token 导入客户端即用，每条订阅链接绑定一台设备，有美国节点且支持 Reality 直连。首页可以免注册领 7 天 8GB 的免费试用，建议先领试用把 Google 账号和 AI Ultra 订阅流程走通，觉得稳再付费。

### 第 2 步：订阅 Google AI Ultra

1. 挂好美国节点，全程保持同一节点（中途换 IP 容易触发支付风控）
2. 访问 Gemini 官网或 Google One 页面，登录 Google 账号
3. 选择 AI Ultra 方案订阅，按页面提示完成支付（需要可国际支付的卡）
4. 订阅生效后，从 Google Labs / Gemini 入口找到 Project Genie

### 第 3 步：开始生成你的世界

1. 输入提示词描述想要的世界（英文提示词效果通常更好），或上传一张参考图
2. 设定角色形象、移动方式、第一/第三人称
3. 生成后即可用键盘在世界中探索，世界会随着你的移动实时生成延展
4. 玩完的片段可以下载保存；想换风格就用「重混」在原世界基础上改

**提示词小技巧**：场景 + 美术风格 + 光照氛围三件套（如 "a misty cyberpunk alley at night, neon signs, rainy reflections, cinematic lighting"），比单写场景名效果好一档。

## 常见问题

**Q：不订阅 AI Ultra 能玩吗？**
A：目前不能，Project Genie 仅对 AI Ultra 订阅用户开放。可以先用本教程第 1 步把网络环境备好，等 Google 扩量或降价再上车。

**Q：为什么打开 Gemini / Google Labs 一直转圈或报地区不可用？**
A：九成是出口 IP 问题：节点不是美区、IP 被 Google 风控标记、或浏览器缓存了旧的地区信息。换美国干净 IP + 无痕窗口重试。

**Q：生成效果一般是怎么回事？**
A：正常现象。它是研究原型不是成品游戏引擎：单段时长有限、偶尔出现场景「幻觉」（比如路中间突然长出草地）。降低预期，把它当作「能走进去玩的 AI 图片」体验会好得多。

**Q：手机能玩吗？**
A：可以，移动端 Gemini App / 浏览器都能入口，但键鼠探索体验更好，建议 PC。

## 相关链接

- [Project Genie 官方介绍（Google 官方博客）](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/project-genie/)
- [Clash Verge Rev](https://github.com/clash-verge-rev/clash-verge-rev) / [sing-box](https://github.com/SagerNet/sing-box)
- [FrogLeap](https://fastergamer.click)：本教程作者自用的网络服务，免注册、有免费试用

---

*本教程为个人经验整理，与 Google 无关；Project Genie 的准入政策随时在变，以 Google 官方页面为准。觉得有用欢迎 Star，也欢迎 Issue 补充最新情况。*
