# CUPL RWXY Notice Watch

[中文说明](README.zh-CN.md)

An unofficial daily archive and static dashboard for public notices from the School of Humanities of China University of Political Science and Law.

![Dashboard demo](assets/frontend-desktop.png)

## Why this exists

The School of Humanities publishes party-building notices, graduate training updates, academic activities, faculty awards, and school news across public pages. This project turns those pages into structured, searchable, exportable data with a clean static dashboard.

## Target site

- Site: CUPL School of Humanities
- Official homepage: https://rwxy.cupl.edu.cn/
- Notice page: https://rwxy.cupl.edu.cn/index/tzgg.htm
- News page: https://rwxy.cupl.edu.cn/index/xydt.htm
- Disclaimer: unofficial project. It only archives public web pages and does not represent CUPL.

## Quick start

```bash
python3 scraper.py 3
python3 -m http.server 8000
```

Open `http://localhost:8000` to view the dashboard.

## Data outputs

- `data/notices.json`: merged notice archive
- `data/notices.csv`: spreadsheet-friendly export
- `data/history/YYYY-MM-DD.json`: daily crawl snapshot
- `data/meta.json`: site, update time, section and count metadata

Each record includes `title`, `date`, `url`, `summary`, `section`, `source_url`, `first_seen_at`, and `last_seen_at`.

## Automation

The repository includes GitHub Actions workflow examples under `.github/workflows/` for daily crawl and data commit. If the workflow files are not visible in the remote repository, the publishing token needs GitHub `workflow` write permission.

## Roadmap

- Add more CUPL schools into a cross-site index.
- Add RSS/Atom export for notice subscriptions.
- Add change detection for edited notices.
- Publish a GitHub Pages dashboard.

## License

MIT
