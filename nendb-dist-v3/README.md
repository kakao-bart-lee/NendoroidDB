# nendb-dist-v3

Built catalog snapshot consumed by the [nendb app](https://github.com/kakao-bart-lee/nendb).

**Schema v3** (2026-05-17): drops `name_zh`, `series_zh`, `specs_text_zh`, `gsc_url_zh`. SQLite FTS4 `unicode61` cannot tokenize a space-less han string, so the columns were unsearchable. See the nendb repo for the v2 → v3 migration write-up.

- `catalog.db` — Room-compatible SQLite (`PRAGMA user_version = 3`, FTS4 unicode61). Ships in the Android APK as `assets/catalog/catalog.db`.
- `index.json` — `{ schema_version: 3, generated_at, count, items: [{num, sha}] }`. The app diffs this against its bundled copy when the user hits "카탈로그 업데이트 확인".
- `items/<num>.json` — Per-SKU enriched record. Fetched only when the `sha` mismatch indicates a content change.
- `catalog.json` — All items combined (debug/iOS use).

Built by `data-build/` in the nendb repo. Re-run `npm run build` there and copy `dist/*` here to publish a new snapshot.

Older schemas live next door — `nendb-dist-v1/` is the v1 (NendoroidDB-only seed) snapshot kept around for archived app installs. New app versions read from this `nendb-dist-v3/` directory.

See [LICENSE-NOTICE.md](./LICENSE-NOTICE.md) for upstream source attribution (NendoroidDB, nendoroid-heaven, GSC).
