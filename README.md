# Douyin Video Fetch（抖音视频下载）

OpenClaw 技能：支持通过 URL 或 `video_id` 下载抖音视频，支持批量任务与 JSON 结构化输出。

## 功能

- 按抖音视频 URL 下载
- 按 `video_id` 下载
- 支持批量输入（文件）
- 默认按 `video_id` 自动命名
- 支持 `--json` 输出，方便接入自动化流程

## 依赖

- Python 3.10+
- `playwright`
- `aiohttp`
- Playwright Chromium

安装依赖：

```bash
pip install playwright aiohttp
playwright install chromium
```

## 用法

在当前技能目录下执行：

```bash
python scripts/fetch_video.py "https://www.douyin.com/video/7599980362898427178"
```

按 `video_id` 下载：

```bash
python scripts/fetch_video.py 7599980362898427178
```

批量下载（每行一个 URL 或 `video_id`）：

```bash
python scripts/fetch_video.py --file input.txt --output-dir ./downloads/douyin
```

输出 JSON 结果：

```bash
python scripts/fetch_video.py --file input.txt --output-dir ./downloads/douyin --json
```

## 输出约定

- 默认输出目录：`downloads`
- 文件名：`<video_id>.mp4`

## 说明

- 该仓库是 OpenClaw Skill 源码仓库。
- 技能元信息与调用说明见 `SKILL.md`。

---

# English (Short)

OpenClaw skill for downloading Douyin videos by URL or `video_id`, with batch mode and JSON output.

- Script: `scripts/fetch_video.py`
- Skill metadata: `SKILL.md`
