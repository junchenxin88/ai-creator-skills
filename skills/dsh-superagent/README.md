# dsh-superagent Skills（第三方）

> 本目录收录第三方项目自带的 Agent Skill 文件，**非本仓库原创**，文件原文未改动。

- 作者：DeepSeek Harness Team（[deepseek-ai](https://github.com/deepseek-ai)）
- 来源：https://github.com/deepseek-ai/dsh-superagent-prototype （原文件位于 [skills/](https://github.com/deepseek-ai/dsh-superagent-prototype/tree/main/skills)）
- 许可证：MIT（原文见本目录 [LICENSE](LICENSE)，版权归原作者所有）
- 参考版本：commit `6337fc8`（2026-11-01）

## 简介
dsh-superagent 是 DeepSeek 发布的研究原型：面向单个 GitHub 仓库的主动式 Coding Agent，打包成 [DeepSeek Harness](https://www.deepseek.com/en/harness/) 的 bundle。它监听 GitHub（可选飞书），有人派活时开工作项、在独立会话里干活，并在原对话里回复（例如提 PR），另有网页面板显示需要人处理的事项。

| Skill | 作用 |
|---|---|
| [dsh-superagent-feishu](dsh-superagent-feishu/SKILL.md) | 以机器人身份读取飞书消息、话题、合并转发、附件和文档 |
| [dsh-superagent-github](dsh-superagent-github/SKILL.md) | 用 gh 读取 GitHub issue、PR、review 和 CI |

⚠️ 这两个 Skill 依赖 dsh-superagent 运行时提供的 `orchestrator_read` 等工具，**脱离该 bundle 单独安装基本无法使用**，这里主要供学习其 Skill 写法参考。

## 安装方法
按原仓库 README / [SETUP.md](https://github.com/deepseek-ai/dsh-superagent-prototype/blob/main/SETUP.md) 部署完整 bundle（需 DeepSeek Harness）：
```bash
git clone https://github.com/deepseek-ai/dsh-superagent-prototype.git
```
