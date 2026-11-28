# RecentBBP

Tracks bug bounty program scope assets — domains, wildcard domains, URLs, IPs, and CIDR ranges — added or updated **today (UTC)** in public bug bounty and VDP programs, read directly from each platform on a recurring schedule.

Out-of-scope items and non-network assets (mobile apps, app-store IDs, source repos, smart contracts, binaries, hardware, SaaS tenants, etc.) are excluded — only domains, wildcards, URLs, IPs, and CIDR ranges are tracked.

## Sources

Collected straight from the platforms (no third-party aggregators):

HackerOne, Intigriti, YesWeHack, Bugcrowd, Immunefi, HackenProof.

## Files

- `domains.txt` — master, append-only, deduplicated list of every in-scope domain / wildcard domain / URL seen across all runs. One asset per line, no other content.
- `ips.txt` — master, append-only, deduplicated list of every in-scope IP / CIDR range seen across all runs. One asset per line, no other content.
- `daily/YYYY-MM-DD-domains.txt` / `daily/YYYY-MM-DD-ips.txt` — only the assets first observed on that run's date (i.e. not already present in the master lists). Omitted for a date if nothing new was found.
- `daily/YYYY-MM-DD.jsonl` — the same new assets as that day's .txt files, one JSON object per line, recording which program each belongs to (`asset`, `type`, `program`, `handle`, `platform`, `kind`, `url`, `bounty`, `first_seen`). A day with no new assets has a single `{"run":…,"new":0}` line; a platform that failed adds a `{"run":…,"platform":…,"error":…}` line. November 2026 was backfilled (`"backfill":true`, date-only `first_seen`); assets that could not be matched to exactly one program have null program fields and `"unresolved":true`.
- `state/*.txt` — per-platform snapshots used for diffing (HackenProof).
- This README's log below — one dated entry per run, newest first, listing each program and how many assets it contributed (no asset values here; see the .txt files for those).

### 2026-11-28
No new assets.

### 2026-11-27
- RedStone Settle Smart Contracts, API, Webapp (BB - HackenProof) — 1 domain/URL
Total: 1 domain/URL

### 2026-11-26
- Ping Identity (BB - HackerOne) — 1 domain/URL
Total: 1 domain/URL
- HackerOne: check failed (1 handles errored: fiserv ); assets from it may be missing.

### 2026-11-25
- DANA Bug Bounty Program (BB - YesWeHack) — 1 domain/URL
- Nubank Brasil Managed Bug Bounty Program (BB - Bugcrowd) — 1 domain/URL
- Bitwarden (VDP - HackerOne) — 1 domain/URL
- John Deere (VDP - HackerOne) — 1 domain/URL
Total: 4 domains/URLs

### 2026-11-24
- KHealth (BB - HackerOne) — 2 domains/URLs, 2 Wildcards
- John Deere (VDP - HackerOne) — 2 domains/URLs
- Visa (BB - HackerOne) — 48 domains/URLs
- Bitwarden (VDP - HackerOne) — 9 domains/URLs
Total: 61 domains/URLs, 2 Wildcards

### 2026-11-23
- Equifax-vdp (VDP - HackerOne) — 1 Wildcard
- John Deere (VDP - HackerOne) — 3 domains/URLs
- The Walt Disney Company (VDP - HackerOne) — 1 domain/URL
- TransUnion LLC (VDP - HackerOne) — 1 domain/URL
- Visa (BB - HackerOne) — 1 domain/URL
Total: 6 domains/URLs, 1 Wildcard

### 2026-11-20
- Newegg (BB - HackerOne) — 1 domain/URL
- The Coca-Cola Company Vulnerability Disclosure Program (BB - Intigriti) — 145 Wildcards
- Fidelity (VDP - HackerOne) — 1 Wildcard
- John Deere (VDP - HackerOne) — 2 domains/URLs
- Visa (BB - HackerOne) — 1 domain/URL
- BOJA Consulting Bug Bounty (BB - Bugcrowd) — 1 domain/URL
Total: 5 domains/URLs, 146 Wildcards

### 2026-11-19
- Alohi (VDP - HackerOne) — 1 Wildcard
- GRW Trading FZE - Open Bug Bounty Program (BB - YesWeHack) — 1 Wildcard
- vidaXL Services - Open Bug Bounty Program (BB - YesWeHack) — 1 domain/URL, 3 Wildcards
- Majid Al Futtaim Customer Solutions (BB - Bugcrowd) — 11 domains/URLs
- Here Technologies (BB - Intigriti) — 2 domains/URLs
- John Deere (VDP - HackerOne) — 3 domains/URLs
- TransUnion LLC (VDP - HackerOne) — 1 domain/URL
- Unico IDtech (BB - HackerOne) — 2 domains/URLs
- DIB VDP (VDP - HackerOne) — 11 domains/URLs
Total: 31 domains/URLs, 5 Wildcards

### 2026-11-18
- John Deere (VDP - HackerOne) — 5 domains/URLs
- Visa (BB - HackerOne) — 2 domains/URLs
Total: 7 domains/URLs

### 2026-11-17
- Challenge 1126 (BB - Intigriti) — 1 domains/URLs
- Mondelēz International (VDP - HackerOne) — 1 domains/URLs
- Airtable (BB - HackerOne) — 3 domains/URLs, 2 Wildcard
- Posti Bug Bounty (BB - Intigriti) — 7 domains/URLs
- John Deere (VDP - HackerOne) — 1 domains/URLs
- Visa (BB - HackerOne) — 1 domains/URLs
Total: 14 domains/URLs, 2 Wildcard

### 2026-11-16
- Henkel (VDP - HackerOne) — 1 domains/URLs, 5 Wildcard
- BoursoBank Bug Bounty Program (BB - YesWeHack) — 4 domains/URLs
- Meesho (BB - HackerOne) — 3 domains/URLs
- Essity (VDP - HackerOne) — 1 domains/URLs
- John Deere (VDP - HackerOne) — 1 domains/URLs
Total: 10 domains/URLs, 5 Wildcard

### 2026-11-15
No new assets.

### 2026-11-13
- Essity (VDP - HackerOne) — 1 domains/URLs
- Vinted Bug Bounty (BB - Bugcrowd) — 4 domains/URLs, 1 Wildcard
- Deviniti (BB - Bugcrowd) — 1 domains/URLs
Total: 6 domains/URLs, 1 Wildcard

### 2026-11-12
- Moneytree KK (BB - Bugcrowd) — 1 domains/URLs
- 3DS OUTSCALE (BB - YesWeHack) — 1 domains/URLs
Total: 2 domains/URLs

### 2026-11-11
- Superbet (BB - HackerOne) — 1 Wildcard
- Unico IDtech (BB - HackerOne) — 5 domains/URLs
- Hilton (BB - HackerOne) — 1 Wildcard
- Equifax-vdp (VDP - HackerOne) — 1 Wildcard
Total: 5 domains/URLs, 3 Wildcard

### 2026-11-10
- Bitpanda Ongoing Bug Bounty (BB - Bugcrowd) — 1 domains/URLs
- Shopify (BB - HackerOne) — 3 domains/URLs, 2 Wildcard
Total: 4 domains/URLs, 2 Wildcard

### 2026-11-09
- Canada Post - Responsible Disclosure Program (BB - Intigriti) — 2 Wildcard
- John Deere (VDP - HackerOne) — 2 domains/URLs
- Mars (VDP - HackerOne) — 1 domains/URLs
- CBRE (VDP - HackerOne) — 2 domains/URLs
Total: 5 domains/URLs, 2 Wildcard

### 2026-11-07
- Ping Identity (BB - HackerOne) — 1 domains/URLs
Total: 1 domains/URLs

### 2026-11-06
- Bybit Fintech Ltd (BB - HackerOne) — 6 domains/URLs
- Anduril Industries (BB - HackerOne) — 1 domains/URLs
- Henkel (VDP - HackerOne) — 3 Wildcard
- Moneytree KK (BB - Bugcrowd) — 1 domains/URLs
- YesWeHack Dojo (BB - YesWeHack) — 1 domains/URLs
- Braze, Inc. (BB - HackerOne) — 1 domains/URLs
- MOD Supply Chain VDP (VDP - HackerOne) — 1 IP/CIDR
Total: 10 domains/URLs, 1 IP/CIDR, 3 Wildcard

### 2026-11-05
- Stripe (BB - HackerOne) — 3 domains/URLs
- John Deere (VDP - HackerOne) — 2 domains/URLs
- hostinger (BB - HackerOne) — 1 domains/URLs
- Judge.me (BB - HackerOne) — 1 domains/URLs
- Credit Karma (BB - HackerOne) — 1 Wildcard
Total: 7 domains/URLs, 1 Wildcard

### 2026-11-04
- Mondelēz International (VDP - HackerOne) — 1 domains/URLs
- Remitly (BB - HackerOne) — 1 domains/URLs
- John Deere (VDP - HackerOne) — 1 domains/URLs
- Henkel (VDP - HackerOne) — 10 Wildcard
- Resolution (BB - Bugcrowd) — 1 domains/URLs
Total: 4 domains/URLs, 10 Wildcard

### 2026-11-03
- Crypto.com (BB - HackerOne) — 3 domains/URLs
- OpenAI (BB - Bugcrowd) — 1 domains/URLs
- John Deere (VDP - HackerOne) — 5 domains/URLs
- HARMAN International - Web Applications (BB - YesWeHack) — 67 domains/URLs
- Infomaniak Bug Bounty program (BB - YesWeHack) — 2 domains/URLs
- Cvent Bug Bounty (BB - Bugcrowd) — 1 domains/URLs
- Bugcrowd: 1 program (cms-bbpublic) returned HTTP 404 for its changelog and was not checked.
Total: 79 domains/URLs

### 2026-11-02
No new assets.
- Bugcrowd: 1 program (cms-bbpublic) returned HTTP 404 for its changelog and was not checked.

### 2026-11-01
No new assets.
- Bugcrowd: 1 program (cms-bbpublic) returned HTTP 404 for its changelog and was not checked.

### 2026-10-31
No new assets.
- Bugcrowd: 1 program (cms-bbpublic) returned HTTP 404 for its changelog and was not checked.

### 2026-10-30
- 1win (BB - HackerOne) — 6 domains/URLs
- SIX Group (BB - HackerOne) — 1 domains/URLs
- StonikByte (BB - Bugcrowd) — 7 domains/URLs
- CoW Protocol (BB - Immunefi) — 2 domains/URLs
- Whitechain (BB - HackenProof) — 4 domains/URLs
- Bugcrowd: 1 program (cms-bbpublic) returned HTTP 404 for its changelog and was not checked.
Total: 20 domains/URLs

### 2026-10-29
- MTN Group (VDP - HackerOne) — 3 domains/URLs
Total: 3 domains/URLs

### 2026-10-28
- Wealthsimple (BB - HackerOne) — 1 Wildcard
- Water-Link (BB - Intigriti) — 14 domains/URLs, 2 Wildcard
- Water-Link VDP (BB - Intigriti) — 1 domains/URLs, 1 Wildcard
- OTTO.DE Bug Bounty (BB - YesWeHack) — 1 domains/URLs
- DevAcrobats (BB - Bugcrowd) — 1 domains/URLs
- Majid Al Futtaim Lifestyle (BB - Bugcrowd) — 1 domains/URLs
- Moneytree KK (BB - Bugcrowd) — 1 domains/URLs
- ZMO Exchange (BB - HackenProof) — 1 domains/URLs
- HackenProof: 1 program (Meest Poshta Mobile) returned HTTP 500 and was not checked.
Total: 19 domains/URLs, 3 Wildcard

### 2026-10-27
- Cloudflare Public Bug Bounty (BB - HackerOne) — 1 domains/URLs
- Zurich Insurance (VDP - HackerOne) — 1 Wildcard
- KOHO (BB - HackerOne) — 4 domains/URLs
- John Deere (VDP - HackerOne) — 2 domains/URLs
- Visa (BB - HackerOne) — 1 domains/URLs
- Bose (VDP) (VDP - HackerOne) — 1 domains/URLs, 1 Wildcard
- Henkel (VDP - HackerOne) — 9 domains/URLs
- Thales Cyber Security Products Bug Bounty (BB - Bugcrowd) — 2 domains/URLs
- OpenAI (BB - Bugcrowd) — 1 domains/URLs
- ENS (BB - Immunefi) — 1 domains/URLs
Total: 22 domains/URLs, 2 Wildcard

### 2026-10-26
- Ferrero (VDP - HackerOne) — 70 domains/URLs
- John Deere (VDP - HackerOne) — 2 domains/URLs
Total: 72 domains/URLs

### 2026-10-25
No new assets.

### 2026-10-24
- Exodus (BB - HackerOne) — 1 domains/URLs
Total: 1 domains/URLs

### 2026-10-23
- Arkose Labs (BB - HackerOne) — 3 domains/URLs
- Goldman Sachs (BB - HackerOne) — 1 Wildcard
- John Deere (VDP - HackerOne) — 1 domains/URLs
- Supabase (VDP - HackerOne) — 1 domains/URLs
- Nexuzhealth Web PACS (BB - Intigriti) — 1 domains/URLs
- Storebrand Responsible Disclosure (BB - Intigriti) — 1 Wildcard
Total: 6 domains/URLs, 2 Wildcard
