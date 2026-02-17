# Douyin Video Fetch

OpenClaw Skill for downloading Douyin videos to local files (watermark-free when source is available).

## What it does

- Download by Douyin video URL
- Download by `video_id`
- Batch download from input file
- Auto naming by `video_id`
- JSON result output for pipeline integration

## Requirements

- Python 3.10+
- `playwright`
- `aiohttp`
- Chromium for Playwright

Install dependencies:

```bash
pip install playwright aiohttp
playwright install chromium
```

## Usage

From this skill directory:

```bash
python scripts/fetch_video.py "https://www.douyin.com/video/7599980362898427178"
```

By `video_id`:

```bash
python scripts/fetch_video.py 7599980362898427178
```

Batch mode (one URL or `video_id` per line):

```bash
python scripts/fetch_video.py --file input.txt --output-dir ./downloads/douyin
```

JSON output:

```bash
python scripts/fetch_video.py --file input.txt --output-dir ./downloads/douyin --json
```

## Output

- Default output dir: `downloads`
- File name: `<video_id>.mp4`

## Skill file

See `SKILL.md` for OpenClaw skill metadata and quick instructions.
