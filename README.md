# ai-creator-skills
中文 AI 内容创作者的原创 Agent Skills（适用于 Claude Code / Cursor 等支持 SKILL.md 的工具）。

## 技能列表
| 技能 | 用途 |
|---|---|
| [platform-playbooks](skills/platform-playbooks) | 抖音/公众号/头条/视频号/X 五平台执行清单 |
| [content-scorecard](skills/content-scorecard) | 图文成品打分标准与一票否决项 |
| [moneyprinterturbo](skills/moneyprinterturbo) | 【第三方·官方 Skill】主题一键生成短视频（harry0703，MIT） |
| [scrapling](skills/scrapling) | 【第三方·官方 Skill】网页抓取/爬虫，自带 MCP（D4Vinci，BSD-3-Clause） |

标注【第三方】的目录收录的是原项目官方 Skill 文件，版权归原作者，许可证见各目录。

## 推荐开源项目（未收录文件，请到原仓库安装）
| 项目 | 简介 | 许可证 |
|---|---|---|
| [ZJU-REAL/Easel](https://github.com/ZJU-REAL/Easel) | 开源社媒运营 AI Agent：发现热点、创作内容、一键发布到小红书/抖音/知乎/B站等（完整应用，内置技能依赖其运行环境） | Apache-2.0 |
| [larksuite/cli](https://github.com/larksuite/cli) | 飞书/Lark 官方 CLI，200+ 命令，自带 20+ 个 AI Agent Skills（体积较大，建议按原仓库说明安装） | MIT |
| [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) | Nous Research 开源的个人 AI Agent | MIT |
| [openclawby/openclawby-skills](https://github.com/openclawby/openclawby-skills) | Clawby 官方 Agent Skill：行情、链上、社交数据与交易执行（需 Clawby API Key，涉及真实交易，谨慎使用） | MIT |

## 安装
```bash
git clone https://github.com/junchenxin88/ai-creator-skills.git
cp -r ai-creator-skills/skills/* ~/.claude/skills/   # 全部安装，或只复制需要的文件夹
```

## 关注作者
- X：[@andyzhang123199](https://x.com/andyzhang123199)

## 许可
MIT，见 [LICENSE](LICENSE)。
