# Scrapling Agent Skill（第三方）

> 本目录收录第三方项目官方提供的 Agent Skill 文件，**非本仓库原创**，文件原文未改动。

- 原作者：Karim Shoair（[D4Vinci](https://github.com/D4Vinci)）
- 来源：https://github.com/D4Vinci/Scrapling （Skill 原文件位于 [agent-skill/Scrapling-Skill/](https://github.com/D4Vinci/Scrapling/tree/main/agent-skill/Scrapling-Skill)）
- 许可证：BSD-3-Clause（原文见本目录 [LICENSE.txt](LICENSE.txt)，版权归原作者所有）
- 参考版本：commit `26dc85a`（2026-11-01）

## 简介
Scrapling 是一个 Python 网页抓取库，把 HTTP 请求、隐身/无头浏览器、并发爬虫和自适应解析放进同一套接口，并自带 MCP 服务器可接入 AI Agent。这个官方 Skill（`scrapling-official`）给 Agent 提供最新 API 指南和示例，让它直接写出可用的抓取代码，而不是凭过时的训练数据猜。

包含：`SKILL.md`、`references/`（抓取、解析、爬虫、MCP 服务器等参考文档）、`examples/`（示例脚本）。未复制原仓库中的 zip 包和库源码。

## 安装方法
1. 先安装 Scrapling 库本身（见 [官方文档](https://scrapling.readthedocs.io/)）：`pip install scrapling`（浏览器相关功能需按文档额外安装依赖）。
2. 安装 Skill，任选其一：
```bash
# 从本仓库复制
cp -r skills/scrapling ~/.claude/skills/
# 或官方方式（skills.sh）
npx skills add D4Vinci/Scrapling --skill scrapling-official
# 或 OpenClaw 的 Clawhub
clawhub install scrapling-official
```
请遵守目标网站的服务条款与 robots 规则。
