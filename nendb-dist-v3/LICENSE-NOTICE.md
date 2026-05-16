# LICENSE-NOTICE — `nendb-dist-v3`

This snapshot is a derivative work assembled from three upstream sources. The
catalog inherits the most restrictive license among them.

## Upstream sources

### 1. nendoroid-heaven.com (Ossie & Ilona)

- License: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) (Attribution-NonCommercial 4.0 International)
- Used for: official Nendoroid number, series/character classification, release year, `nh_type` tag, fallback images
- **Modifications:** transformed from per-page HTML detail pages into the nendb v3 catalog schema (SQLite + per-SKU JSON), filtered, normalized, and merged with metadata from the other two sources

### 2. NendoroidDB (KhoraLee)

- Source: [github.com/KhoraLee/NendoroidDB](https://github.com/KhoraLee/NendoroidDB)
- License: unspecified (the repo carries no LICENSE file; cloning + forking is permitted by GitHub ToS)
- Used for: multilingual metadata (en / ja / ko names and series), variant grouping seed, accessory master, original list price (JPY)
- nendb pulls through the [kakao-bart-lee/NendoroidDB](https://github.com/kakao-bart-lee/NendoroidDB) fork
- Outreach to the original author about explicit redistribution terms is in progress

### 3. Good Smile Company global site (goodsmile.com)

- Nendoroid® is a registered trademark of Good Smile Company, Inc.
- Rights to all product images, copy, and SKU metadata are retained by GSC
- nendb scrapes only publicly-served JSON-LD and rendered HTML, and renders the official site as the authoritative source for any purchase action
- Treatment: rights-retained, tolerated for non-commercial fan-app use — not licensed

## What this means for you

This catalog snapshot may be used **only for non-commercial purposes** consistent with:

- CC BY-NC 4.0 (the most permissive license in the stack)
- Good Smile Company's trademark and image rights

The following are **not** permitted:

- Commercial redistribution
- Repackaging as an API or data product
- Use in any product or service that competes with or imitates Good Smile Company offerings
- Claiming official affiliation with or sponsorship by Good Smile Company

## Contact

- Data corrections, attribution requests, or license inquiries: bart.lee@kakaocorp.com
- Source-data rights-holders (especially KhoraLee or Good Smile Company): the email above, or open an issue on [github.com/kakao-bart-lee/nendb](https://github.com/kakao-bart-lee/nendb/issues), to request take-down, correction, or expanded attribution

The end-user-facing version of this notice lives in the nendb app's Settings → Attribution screen, and in the nendb repo's `docs/ATTRIBUTION.md`.
