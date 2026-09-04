# RecentBBP

Tracks bug bounty program scope assets — domains, wildcard domains, URLs, IPs, and CIDR ranges — newly added to public bug bounty and VDP program scopes, aggregated on a recurring schedule from free, open-source scope-data sources (arkadiyt/bounty-targets-data, bbscope.com, FireBounty, Chaos, disclose.io).

Out-of-scope items and non-network assets (mobile apps, source repos, hardware, SaaS tenants, etc.) are excluded — only domains, wildcards, URLs, IPs, and CIDR ranges are tracked.

## Files

- `domains.txt` — master, append-only, deduplicated list of every in-scope domain / wildcard domain / URL seen across all runs. One asset per line, no other content.
- `ips.txt` — master, append-only, deduplicated list of every in-scope IP / CIDR range seen across all runs. One asset per line, no other content.
- `daily/YYYY-MM-DD-domains.txt` / `daily/YYYY-MM-DD-ips.txt` — only the assets first observed on that run's date (i.e. not already present in the master lists). Omitted for a date if nothing new was found.
- This README's log below — one dated entry per run, newest first, listing each program and how many assets it contributed (no asset values here; see the .txt files for those).

### 2026-09-04
- WP Engine Bug Bounty — 6 domains/URLs
- John Deere — 5 domains/URLs
- Fifth Third Bank VDP — 2 domains/URLs
- T Mobile — 1 domains/URLs
Total: 14 domains/URLs

_Sources: arkadiyt/bounty-targets-data (24h git-history diff — the only source that verifies changes against real snapshots) confirms these 14. bbscope.com's `since=` parameter does not actually filter server-side (it returned events back to Aug 12 for a 1-day query) and its per-asset "added" events on Bugcrowd programs turned out to re-fire for scope that hadn't changed: cross-checking bbscope's other 32 reported additions (Intercom, Binance, OpenSea, Petpooja VDP Pro, CCData MBB OG, Acorns) against bounty-targets-data's 24h-old snapshot showed those exact targets, and in most cases the exact program's full in-scope list, byte-for-byte unchanged — so they were dropped as false positives rather than recorded as new. Chaos and disclose.io checked, no new programs/domains today. FireBounty was reachable but reported a first run again (no snapshot persisted across sessions), so no assets are attributed to today from it._

### 2026-09-03
- Monash Mbb — 41 domains/URLs
- Kinepolis Group — 39 domains/URLs
- Semtech — 37 domains/URLs
- Usdot Vdp — 18 domains/URLs
- Hypixel Studios Mbb Og — 5 domains/URLs
- Hemi — 3 domains/URLs
- John Deere — 2 domains/URLs
- Treasury Board of Canada Secretariat/Secrétariat du Conseil du Trésor du Canada — 2 domains/URLs
Total: 147 domains/URLs

_Sources: bbscope.com (events timestamped in the last 24h across HackerOne, Bugcrowd, Intigriti, YesWeHack) and arkadiyt/bounty-targets-data (24h git-history diff). Chaos and disclose.io checked, no new programs/domains today. FireBounty was reachable but reported a first run again (no snapshot persisted across sessions), so no assets are attributed to today from it — same as 2026-09-02._

### 2026-09-02
- Adobe Public — 18 domains/URLs
- Nationalaustraliabankog — 15 domains/URLs
- GetYourGuide VDP — 2 domains/URLs
- Coalition, Inc. — 1 domains/URLs
- Fivetran Mbb Og — 1 domains/URLs
Total: 37 domains/URLs

_Sources: bbscope.com (events timestamped today across HackerOne, Bugcrowd, Intigriti, YesWeHack) and arkadiyt/bounty-targets-data (24h git-history diff). Chaos and disclose.io checked, no new programs/domains today. FireBounty was reachable and a baseline snapshot was stored, but as a first run it has no dated diff yet, so no assets are attributed to today from it — future runs will diff against this snapshot._

### 2026-09-01
- Essity — 445 domains/URLs
- Visa — 6 domains/URLs
- Mondelēz International — 5 domains/URLs
- CBRE — 4 domains/URLs
- SBB - Swiss Federal Railways — 3 domains/URLs
- Water-Link — 3 domains/URLs
- Agoda Public — 2 domains/URLs
- DECATHLON — 2 domains/URLs
- John Deere — 2 domains/URLs
- toom Baumarkt GmbH - Webshop — 2 domains/URLs
- Adobe Public — 1 domains/URLs
- Chime Managed Bug Bounty Engagement — 1 domains/URLs
- Cyber Security Coalition — 1 domains/URLs
- Kaseya — 1 domains/URLs
- LATAM Airlines — 1 domains/URLs
- OST Consulting SRL Marketplace Managed Bug Bounty Engagement — 1 domains/URLs
- VFS Global Bug Bounty Program — 1 domains/URLs
- YesWeHack Dojo — 1 domains/URLs
Total: 482 domains/URLs

_Sources: arkadiyt/bounty-targets-data (30-day window; domains, wildcards, and in-scope URLs across HackerOne, Bugcrowd, Intigriti, YesWeHack, Federacy — no new IPs/CIDRs this window). Chaos and disclose.io checked, no new programs/domains in this window. bbscope.com and firebounty.com were unreachable from this environment (network egress blocked)._

### 2026-08-31
- KKR-VDP — 47 domains/URLs
- NBA Public Bug Bounty — 43 domains/URLs
- 8x8 — 6 domains/URLs
- Water-Link — 4 domains/URLs
- John Deere — 3 domains/URLs
- Visa — 2 domains/URLs
Total: 105 domains/URLs

_Sources: arkadiyt/bounty-targets-data (30-day window). Chaos and disclose.io checked, no new programs/domains in this window. bbscope.com and firebounty.com were unreachable from this environment (network egress blocked)._

### 2026-08-30
- TrueLayer VDP — 1 domains/URLs
Total: 1 domains/URLs

_Sources: arkadiyt/bounty-targets-data (30-day window). Chaos and disclose.io checked, no new programs/domains in this window. bbscope.com and firebounty.com were unreachable from this environment (network egress blocked)._

### 2026-08-29
- John Deere — 1 domains/URLs
Total: 1 domains/URLs

_Sources: arkadiyt/bounty-targets-data (30-day window). Chaos and disclose.io checked, no new programs/domains in this window. bbscope.com and firebounty.com were unreachable from this environment (network egress blocked)._

### 2026-08-28
- 8x8 — 1 domains/URLs
- Aiven Managed Bug Bounty — 1 domains/URLs
- Alshaya — 1 domains/URLs
- Assa Abloy Americas — 21 domains/URLs
- Axel Springer National Media & Tech — 1 domains/URLs
- Box BB — 10 domains/URLs
- Challenge 0826 — 1 domains/URLs
- Coinbase — 1 domains/URLs
- Crypto.com — 2 domains/URLs
- Cyber Security Coalition — 1 domains/URLs
- Deezer Bug Bounty Program — 10 domains/URLs
- Dutch Lottery VDP — 8 domains/URLs
- Equifax-vdp — 3 domains/URLs
- Essity — 333 domains/URLs
- European Space Agency (ESA) VDP — 52 domains/URLs
- Exodus — 11 domains/URLs
- GOJEK - Public Bounty Program — 1 domains/URLs
- Henkel — 4 domains/URLs
- Intergamma — 24 domains/URLs
- John Deere — 27 domains/URLs
- Kaseya — 1 domains/URLs
- Klarna — 4 domains/URLs
- LATAM Airlines — 1 domains/URLs
- Libelle — 1 domains/URLs
- Majid Al Futtaim Customer Solutions — 3 domains/URLs
- Majid Al Futtaim Properties — 12 domains/URLs
- Mars — 2 domains/URLs
- Mondelēz International — 341 domains/URLs
- MoonPay — 5 domains/URLs
- MTN Group — 1 domains/URLs
- NBA Public Bug Bounty — 85 domains/URLs
- OST Consulting SRL Marketplace Managed Bug Bounty Engagement — 1 domains/URLs
- OURA Vulnerability Disclosure Program — 1 domains/URLs
- Posti Bug Bounty — 41 domains/URLs
- PRISM — 19 domains/URLs
- Salto Vulnerability Disclosure — 32 domains/URLs
- Spacelift VDP — 3 domains/URLs
- Superhuman (formerly Grammarly) — 1 domains/URLs
- toom Baumarkt GmbH - Webshop — 2 domains/URLs
- TransUnion LLC — 7 domains/URLs
- Treasury Board of Canada Secretariat/Secrétariat du Conseil du Trésor du Canada — 5 domains/URLs
- TrueLayer VDP — 5 domains/URLs
- Varonis — 4 domains/URLs
- Veeam — 1 domains/URLs
- VFS Global Bug Bounty Program — 1 domains/URLs
- Visa — 47 domains/URLs
- Visma — 4 domains/URLs
- Vodafone Oman — 5 domains/URLs
- X / xAI — 5 domains/URLs
Total: 1153 domains/URLs

_Sources: arkadiyt/bounty-targets-data (30-day window). Chaos and disclose.io checked, no new programs/domains in this window. bbscope.com and firebounty.com were unreachable from this environment (network egress blocked)._
