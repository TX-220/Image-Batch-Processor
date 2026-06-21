# Image Batch Processor

**Batch processor for images & videos** — metadata stripping, renaming, compression (WebP + H.265), resizing, trimming, and audio muting. Includes both powerful CLI and a simple Tkinter GUI.

**This was an experimental project developed with Claude (Haiku). Later improved significantly with Grok.**

## Quick Start

```bash
git clone https://github.com/TX-220/image-batch-tool.git
cd image-batch-tool
pip install -r requirements.txt
python image_batch.py --help
python image_batch.py --gui
```

## Key Features

- Strip **all** metadata from images
- Bulk rename with pattern matching
- Image compression to WebP (quality or target file size)
- Video compression to H.265 (CRF + preset, optional mute)
- Resize images and videos
- Video trim (start/end)
- Full dry-run support + recursive mode
- `--overwrite` (default: safe `_suffix` files) and `--delete-ext` options
- Strong safety for video same-dir operations

See the full README below for details, warnings, and examples.

## Important Warnings

**Always use `--dry-run` first.**

See the detailed warnings in the sections below about `--overwrite`, `--delete-ext`, and video processing safety.

## Installation

```bash
pip install Pillow tqdm
# ffmpeg required for video features:
# sudo apt install ffmpeg
```

## Usage (CLI)

```bash
python image_batch.py --dir ./my-media --action compress --quality 80 --recursive --dry-run
```

See full examples and options in the sections below.

## GUI

```bash
python image_batch_gui.py
# or
python image_batch.py --gui
```

## License

MIT — see [LICENSE](LICENSE).

TX-220 — Concept, design, direction.  
Grok (xAI) — Implementation.
