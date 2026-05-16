# nendb-dist

Built catalog snapshot consumed by the [nendb app](https://github.com/kakao-bart-lee/nendb).

- `catalog.db` — Room-compatible SQLite (FTS4 unicode61). Ships in the Android APK.
- `index.json` — `{ schema_version, generated_at, count, items: [{num, sha}] }`. The app diffs this against its bundled copy when the user hits "카탈로그 업데이트 확인".
- `items/<num>.json` — Per-SKU enriched record. Fetched only when sha mismatch.
- `catalog.json` — All items combined (debug/iOS use).

Built by `data-build/` in the nendb repo. Re-run `npm run build` there and copy `dist/*` here to publish a new snapshot.
