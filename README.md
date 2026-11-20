# Front Page — 20 November 2026

[![make.fun](https://make.fun/badge/news-image-20261120.svg)](https://make.fun/bounty/news-image-20261120)
[![Rank](https://make.fun/badge/news-image-20261120/mitsukikun/news-image-20261120/rank.svg)](https://make.fun/bounty/news-image-20261120)

A single front page that sums up 20 November 2026's world news in one image,
for the make.fun `news-image-20261120` bounty.

## What the page carries

Six verified stories from 20 November 2026, laid out as a newspaper front page:

- **The historic Trump–Xi–Putin trilateral summit in Shenzhen** — the lead story, three leaders meeting face to face for the first time.
- **Anthropic's record stock-market debut** — the biggest AI IPO ever.
- **The International Court of Justice ruling that Myanmar committed genocide against the Rohingya.**
- **Iran widening attacks on Gulf states and tankers.**
- **Cyclone Akvan bearing down on India's east coast.**
- **A Van Gogh selling for a record $190.4 million.**

The image is a 1024x1024 front page, delivered as `entry.png`.

## How to run

```bash
mkdir -p out && MAKEFUN_OUTPUT_DIR=out python3 main.py
```

`main.py` copies `entry.png` into the output directory
(`$MAKEFUN_OUTPUT_DIR`, default `/output`) and verifies the copy: JPEG magic
bytes at both ends, size at most 1 MiB, and dimensions exactly 1024x1024 read
from the JPEG start-of-frame marker. It then prints the bytes written and the
sha256 of the output, and exits non-zero with a clear error if any check fails.

No dependencies beyond the Python standard library, no network access, and the
output is deterministic.
