# ai-creator-skills
中文 AI 内容创作者的原创 Agent Skills（适用于 Claude Code / Cursor 等支持 SKILL.md 的工具）。

## 技能列表
| 技能 | 用途 |
|---|---|
| [platform-playbooks](skills/platform-playbooks) | 抖音/公众号/头条/视频号/X 五平台执行清单 |
| [content-scorecard](skills/content-scorecard) | 图文成品打分标准与一票否决项 |
| [moneyprinterturbo](skills/moneyprinterturbo) | 【第三方·官方 Skill】主题一键生成短视频（harry0703，MIT） |
| [scrapling](skills/scrapling) | 【第三方·官方 Skill】网页抓取/爬虫，自带 MCP（D4Vinci，BSD-3-Clause） |
| [dsh-superagent](skills/dsh-superagent) | 【第三方·官方 Skill】DeepSeek 主动式 Coding Agent 原型的飞书/GitHub 读取 Skill（deepseek-ai，MIT，需配合原 bundle） |

标注【第三方】的目录收录的是原项目官方 Skill 文件，版权归原作者，许可证见各目录。

## 推荐开源项目（未收录文件，请到原仓库安装）
| 项目 | 简介 | 许可证 |
|---|---|---|
| [ZJU-REAL/Easel](https://github.com/ZJU-REAL/Easel) | 开源社媒运营 AI Agent：发现热点、创作内容、一键发布到小红书/抖音/知乎/B站等（完整应用，内置技能依赖其运行环境） | Apache-2.0 |
| [larksuite/cli](https://github.com/larksuite/cli) | 飞书/Lark 官方 CLI，200+ 命令，自带 20+ 个 AI Agent Skills（体积较大，建议按原仓库说明安装） | MIT |
| [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) | Nous Research 开源的个人 AI Agent | MIT |
| [openclawby/openclawby-skills](https://github.com/openclawby/openclawby-skills) | Clawby 官方 Agent Skill：行情、链上、社交数据与交易执行（需 Clawby API Key，涉及真实交易，谨慎使用） | MIT |
| [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) | 用 HTML 写视频并渲染成 MP4，专为 Agent 设计，自带官方 Skill（skills/hyperframes 约 1.1MB，建议按原仓库安装） | Apache-2.0 |
| [browser-use/video-use](https://github.com/browser-use/video-use) | 让 Coding Agent 帮你剪视频：转录、剪辑方案、字幕、FFmpeg 渲染 | MIT |
| [MengTo/Skills](https://github.com/MengTo/Skills) | 面向设计师/开发者的 Agent Skills 合集（含 browser-video-recording 网页操作演示录制） | MIT |
| [wangzan101/Mika](https://github.com/wangzan101/Mika) | 安卓端侧 AI Agent，后台虚拟屏操作 App，支持 MCP（完整 App） | Apache-2.0 |
| [jackwener/DSH-Android](https://github.com/jackwener/DSH-Android) | 免 Root 免 Termux，一个 APK 在安卓上跑 DeepSeek Harness（社区项目，完整 App） | Apache-2.0 |
| [ccch1mneyyy/dsh-Go](https://github.com/ccch1mneyyy/dsh-Go) | DeepSeek Harness 安卓客户端：手机本机运行或遥控电脑（社区项目，完整 App） | AGPL-3.0 |
| [koala73/worldmonitor](https://github.com/koala73/worldmonitor) | 实时全球情报仪表板：AI 新闻聚合、地缘与基础设施监测（完整应用） | AGPL-3.0 |

## 安装
```bash
git clone https://github.com/junchenxin88/ai-creator-skills.git
cp -r ai-creator-skills/skills/* ~/.claude/skills/   # 全部安装，或只复制需要的文件夹
```

## 关注作者
- X：[@andyzhang123199](https://x.com/andyzhang123199)

## 许可
MIT，见 [LICENSE](LICENSE)。
