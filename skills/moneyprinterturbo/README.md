# MoneyPrinterTurbo（第三方）

> 本目录为第三方项目的介绍与安装指引，**非本仓库原创**。

- 原作者：[harry0703](https://github.com/harry0703)
- 来源：https://github.com/harry0703/MoneyPrinterTurbo
- 许可证：MIT（原文见本目录 [LICENSE](LICENSE)，版权归原作者所有）
- 参考版本：commit `4318f3a`（2026-11-01）

## 简介
输入一个主题或关键词，自动生成竖屏/横屏短视频：AI 写文案、配音（TTS）、生成字幕、匹配素材画面、加背景音乐并完成剪辑，适合抖音、视频号、TikTok、Reels、Shorts。提供 Web 界面、API 和命令行。

## 安装与使用
本目录未复制源码（原项目自带的字体、音乐素材可能有各自的授权），请直接从原仓库获取：

```bash
git clone https://github.com/harry0703/MoneyPrinterTurbo.git
cd MoneyPrinterTurbo
cp config.example.toml config.toml   # 填入你自己的大模型 API Key、素材站 Key
# 方式一：Docker
docker compose up
# 方式二：本地（需 Python 与 ImageMagick/ffmpeg，详见原 README）
pip install -r requirements.txt
sh webui.sh
```
启动后浏览器打开 WebUI（默认 http://localhost:8501）。详细配置以原仓库 README 为准。
