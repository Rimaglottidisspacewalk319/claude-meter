# Changelog

Notable changes to claude-meter, by date.

## 2026-03-29

- Color-coded CLI logging for every proxied request (model, tokens, utilization)
- Periodic status summaries via `--status-interval`
- Startup banner showing proxy address and plan tier
- `setup` subcommand to auto-configure shell (bash, zsh, fish)
- Live web dashboard served at `http://localhost:7735` with 5-second auto-refresh

## 2026-03-27

- Self-contained HTML dashboard generator (`dashboard.py`)
- `make dashboard` to publish standalone dashboard to GitHub Pages
- `--summary` flag for human-readable analysis output
- `export.py` for anonymized `share.json` generation
- `report.py` for matplotlib charts and markdown reports
- `install.sh` one-liner for building from source

## 2026-03-25

- Initial proxy: transparent pass-through for `api.anthropic.com`
- Raw JSONL capture under `~/.claude-meter/raw/` with header redaction
- SSE normalizer for streamed Claude responses with gzip handling
- Normalized JSONL output under `~/.claude-meter/normalized/`
- `backfill-normalized` command to derive normalized records from raw logs
- `anthropic-ratelimit-unified-*` header capture (5h, 7d, 7d_sonnet windows)
- Price-weighted usage comparison alongside raw token counts
- Filtered 5h estimate bands with interval-based budget estimation
- Per-model breakdown, reset detection, and time-series analysis
