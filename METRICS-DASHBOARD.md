# Pattern Catalog — Metrics Dashboard

A minimal, self-hosted GitHub-Pages dashboard that tracks how the Pattern Catalog is being downloaded and viewed.

## What it tracks

| Metric                        | Source                              | Window         |
|------------------------------|-------------------------------------|----------------|
| Release-asset downloads      | `GET /repos/.../releases`           | Cumulative     |
| Repo views & unique visitors | `GET /repos/.../traffic/views`      | Last 14 days   |
| Clones & unique cloners      | `GET /repos/.../traffic/clones`     | Last 14 days   |
| Top referrers                | `GET /repos/.../traffic/popular/referrers` | Last 14 days |
| Stars, forks, watchers       | `GET /repos/...`                    | Cumulative     |

Daily totals beyond 14 days are reconstructed from the locally accumulated snapshots in `_metrics/snapshots.json`.

## Files

```
.github/workflows/metrics-snapshot.yml   # Daily cron job
_metrics/current.json                    # Latest snapshot (overwritten daily)
_metrics/snapshots.json                  # Append-only history
docs/dashboard/index.html                # Static dashboard (vanilla JS, no build)
```

## Setup

### 1. Put the files in your repo

Copy the four files above into the same paths in your repository, keeping the directory structure intact.

### 2. Enable GitHub Pages

In **Settings → Pages**, set:

- **Source**: `Deploy from a branch`
- **Branch**: `main` (or whichever branch holds these files)
- **Folder**: `/docs`

Your dashboard will be available at:

```
https://<your-username>.github.io/<repo-name>/dashboard/
```

### 3. Run the workflow once manually

The cron runs at 06:00 UTC daily, but you'll want a snapshot immediately:

1. Open the **Actions** tab in your repo.
2. Select **metrics-snapshot** in the left sidebar.
3. Click **Run workflow** → **Run workflow**.

The workflow takes ~10 seconds. When it finishes, it commits `current.json` and `snapshots.json` to `_metrics/`. Reload the dashboard.

### 4. (Optional) Adjust the cron schedule

The default is daily at 06:00 UTC. Edit the `cron` line in `metrics-snapshot.yml` if you want it more or less often. GitHub allows down to 5-minute granularity, but daily is plenty for book-traffic data — GitHub's own traffic counters update at most hourly.

## How it works

The dashboard is a static HTML file with vanilla JavaScript. It fetches the two JSON files from the repo using relative paths and renders six cards:

1. **Total downloads** — cumulative across all release assets, plus per-asset breakdown
2. **Downloads over time** — sparkline built from accumulated snapshots
3. **Views (14d)** — from GitHub's traffic API, plus daily sparkline
4. **Stars** — cumulative, with historical sparkline
5. **Top referrers (14d)** — where readers are coming from
6. **Clones (14d)** — for source-of-truth clones, not asset downloads

No frameworks, no build step, no external dependencies. The CSS uses parchment-tone palette in light mode and a dark variant via `prefers-color-scheme`.

## Why this approach

- **No backend.** Pages serves the static HTML; Actions writes the JSON; the browser does the rest.
- **No third-party analytics.** Everything stays inside GitHub.
- **No secrets to manage.** The workflow uses the built-in `GITHUB_TOKEN`.
- **Accumulates history.** GitHub truncates traffic to 14 days; snapshotting daily gives you arbitrarily long history.
- **Survives forks.** Anyone forking the repo gets their own dashboard automatically, with their own data.

## Limitations (be honest)

- **Browser views of files in the repo are not tracked per file.** GitHub doesn't expose this.
- **PDF/EPUB reads inside the browser are not tracked.** Only *downloads* of release assets are counted — once a reader has the file, the dashboard can't see what they do with it.
- **The 14-day traffic window is unique-visitor-counted *per day*, not deduplicated across the period.** A reader who visits on three different days counts as three uniques over 14 days but one unique per day. GitHub's own counters work the same way.
- **The dashboard is public** (it's a GitHub Page from a public repo). If you don't want the world to see your download counts, either keep the repo private (Pages still works on private repos with a Pro plan) or skip the dashboard and read the JSON privately.
