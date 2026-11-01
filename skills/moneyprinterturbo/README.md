# MoneyPrinterTurbo（第三方）

> 本目录收录第三方项目官方提供的 Agent Skill 文件，**非本仓库原创**。

- 原作者：[harry0703](https://github.com/harry0703)
- 来源：https://github.com/harry0703/MoneyPrinterTurbo （Skill 原文件位于 [docs/skill/](https://github.com/harry0703/MoneyPrinterTurbo/tree/main/docs/skill)）
- 许可证：MIT（原文见本目录 [LICENSE](LICENSE)，版权归原作者所有）
- 参考版本：commit `4318f3a`（2026-11-01）

## 本目录文件
| 文件 | 说明 |
|---|---|
| [SKILL.md](SKILL.md) | 官方 Agent Skill：让 AI Agent 根据主题/脚本自动安装、配置并生成成片 MP4（原文未改动） |
| [mpt_agent.py](mpt_agent.py) | Skill 配套的官方辅助脚本（原文未改动） |
| [LICENSE](LICENSE) | 原项目 MIT 许可证 |

未复制完整源码及 `resource/` 下的字体、音乐素材。

## 简介
输入一个主题或关键词，自动生成竖屏/横屏短视频：AI 写文案、配音（TTS）、生成字幕、匹配素材画面、加背景音乐并完成剪辑。提供 Web 界面、API 和命令行。

## 安装 Skill
```bash
cp -r skills/moneyprinterturbo ~/.claude/skills/
```
之后对 Agent 说「用 MoneyPrinterTurbo 生成一个主题为 xxx 的视频」即可。

## 手动部署（以原仓库 README 为准）
**方式一：Docker（官方当前默认推荐 `docker-compose.release.yml`，直接拉取预构建镜像 `ghcr.io/harry0703/moneyprinterturbo:latest`）**
```bash
git clone https://github.com/harry0703/MoneyPrinterTurbo.git
cd MoneyPrinterTurbo
cp config.example.toml config.toml   # 填入你自己的大模型、素材站 API Key
docker compose -f docker-compose.release.yml up
```
浏览器打开 http://127.0.0.1:8501 。需要本地重新构建镜像时可用 `docker compose up`。

**方式二：pip 安装官方包（需 Python 3.11+）**

官方 PyPI 包名为 **[mpt](https://pypi.org/project/mpt/)**，由 harry0703 维护。
⚠️ PyPI 上名为 `MoneyPrinterTurbo` 的包由第三方维护，**不是官方包**，请勿安装。
```bash
python3 -m venv .venv && source .venv/bin/activate
python -m pip install mpt
mpt webui
```
