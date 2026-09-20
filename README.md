# RecentBBP

Tracks bug bounty program scope assets — domains, wildcard domains, URLs, IPs, and CIDR ranges — newly added to public bug bounty and VDP program scopes, aggregated on a recurring schedule from free, open-source scope-data sources (arkadiyt/bounty-targets-data, bbscope.com, FireBounty, Chaos, disclose.io).

Out-of-scope items and non-network assets (mobile apps, source repos, hardware, SaaS tenants, etc.) are excluded — only domains, wildcards, URLs, IPs, and CIDR ranges are tracked.

## Files

- `domains.txt` — master, append-only, deduplicated list of every in-scope domain / wildcard domain / URL seen across all runs. One asset per line, no other content.
- `ips.txt` — master, append-only, deduplicated list of every in-scope IP / CIDR range seen across all runs. One asset per line, no other content.
- `daily/YYYY-MM-DD-domains.txt` / `daily/YYYY-MM-DD-ips.txt` — only the assets first observed on that run's date (i.e. not already present in the master lists). Omitted for a date if nothing new was found.
- This README's log below — one dated entry per run, newest first, listing each program and how many assets it contributed (no asset values here; see the .txt files for those).

### 2026-09-20
No new assets.

### 2026-09-19
- TheFork — 13 domains/URLs
- Dell Technologies Application Bug Bounty — 5 domains/URLs
- TransUnion LLC — 4 domains/URLs
- Opus Guard Marketplace — 4 domains/URLs
- OpenSea — 3 domains/URLs
- Hostinger — 3 domains/URLs
- John Deere — 2 domains/URLs
- codecentric Marketplace Bug Bounty — 1 domains/URLs
- Pexels — 1 domains/URLs
- aelbox Marketplace Bug Bounty — 1 domains/URLs
- Infomaniak Bug Bounty program — 1 domains/URLs
- Driessen Vulnerability Disclosure Program — 1 domains/URLs
Total: 39 domains/URLs

### 2026-09-18
- Uniti — 13 domains/URLs
- Faraday, Inc. — 4 domains/URLs
- Expedia Group Bug Bounty — 2 domains/URLs
- Infomaniak Bug Bounty program — 5 domains/URLs
- TrueLayer — 7 domains/URLs
- Venly — 7 domains/URLs
- Posten Bring Responsible Disclosure — 5 domains/URLs
Total: 43 domains/URLs

### 2026-09-17
- John Deere — 2 domains/URLs
- d-you App & German EUDI Wallet Ecosystem — 4 domains/URLs
- Flutter UK&I — 1 domains/URLs
- GULP — 4 domains/URLs
Total: 11 domains/URLs

### 2026-09-16
- John Deere — 2 domains/URLs
- Lightspeed Retail — 4 domains/URLs
- Contentsquare Bug Bounty Program — 4 domains/URLs
- Global Payments — 5 domains/URLs
Total: 15 domains/URLs

### 2026-09-15
- Superbank - Public Bug Bounty Program — 4 domains/URLs
- TrueLayer VDP — 6 domains/URLs
- ADAC Vulnerability Disclosure Program — 3 IP/CIDR
- MercadoLibre — 1 domains/URLs
- Superbet — 1 domains/URLs
- Bolt Technology OÜ — 1 domains/URLs
Total: 13 domains/URLs, 3 IP/CIDR

### 2026-09-14
No new assets.

_Sources: bbscope.com and arkadiyt/bounty-targets-data flagged SEEK and Upwork as new Bugcrowd launches, but without live access to Bugcrowd's own platform this could not be independently confirmed, so both were pulled back out as false positives (same bar as 2026-09-10's held-back Bugcrowd candidates). 3 Wyze "added" events (already in the prior snapshot), an Atlassian-Marketplace listing URL, and 3 GitHub repo links were discarded as not new/out of scope. Chaos and disclose.io: 0 new; FireBounty's 10 TUI ids were stale (2026-06-22 crawl)._

### 2026-09-13
No new assets.

### 2026-09-12
- Superbet — 1 domains/URLs
Total: 1 domains/URLs

### 2026-09-11
- Treasury Board of Canada Secretariat/Secrétariat du Conseil du Trésor du Canada — 1 domains/URLs
- BMC — 1 domains/URLs
- Tempo-Team — 4 domains/URLs
- Yacht — 1 domains/URLs
- Salto Vulnerability Disclosure — 1 domains/URLs
Total: 8 domains/URLs

_Sources: bbscope.com and arkadiyt/bounty-targets-data cross-checked ~40 candidates; live checks confirmed BMC, Tempo-Team, and Yacht as genuine new Intigriti launches and Salto's `*.gantner.cloud` as a real addition to an existing program. 34 Bugcrowd marketplace-listing URLs, a GitHub link, and Posti's re-flagged churn were discarded as out of scope or not new. Chaos and disclose.io: 0 new; FireBounty returned the same stale TUI ids (crawled 2026-06-22)._

### 2026-09-10
- Expedia Group — 16 domains/URLs
Total: 16 domains/URLs

_Sources: bbscope.com and arkadiyt/bounty-targets-data flagged 76 candidates across 13 programs; HackerOne's public `created_at` timestamps confirmed only Expedia Group's 16 assets as genuinely inside the 24h window, filtering out stale Scopely/Expedia/Global Payments entries. 44 Bugcrowd candidates couldn't be re-verified live (no public scope API) so were held back. Chaos and disclose.io: 0 new; FireBounty's 10 TUI ids were stale (2026-06-22 crawl)._

### 2026-09-09
- TransUnion LLC — 1 domains/URLs
- MoonPay — 1 domains/URLs
- Bitso Managed Bug Bounty Engagement — 1 domains/URLs
Total: 3 domains/URLs

_Sources: arkadiyt/bounty-targets-data flagged 16 candidates; bbscope.com's live event stream showed Quizlet and SoundCloud's 9 assets re-firing as churn (not new) and Taxwell's 4 as pre-existing "updated" events, leaving only TransUnion, MoonPay, and Bitso's 3 assets confirmed genuinely new. Chaos and disclose.io: 0 new; FireBounty returned the same stale TUI ids as 2026-09-08._

### 2026-09-08
- Weblate — 1 domains/URLs
- MercadoLibre — 3 domains/URLs
- Semrush — 1 domains/URLs
- Randstad — 3 domains/URLs
Total: 8 domains/URLs

_Sources: arkadiyt/bounty-targets-data flagged 14 candidates; `velocitize.com` was dropped as now out of scope live, and 5 WP Engine assets were dropped as duplicates of the 2026-09-04 entry. Randstad's 3 were confirmed live on Intigriti; Weblate/MercadoLibre/Semrush rely on arkadiyt's snapshot diff alone (HackerOne has no public scope API). Chaos and disclose.io: 0 new; FireBounty's 10 TUI ids were stale (2026-06-22 crawl)._

### 2026-09-07
- Basecamp — 1 domains/URLs
Total: 1 domains/URLs

_Sources: bbscope.com and arkadiyt/bounty-targets-data agree on 1 new asset, `app.fizzy.do` on Basecamp, corroborated by Basecamp's own "Introducing Fizzy" launch announcement. Chaos and disclose.io: 0 new; FireBounty still a first run, no assets attributed._

### 2026-09-06
No new assets.

_Sources: bbscope.com, arkadiyt/bounty-targets-data, Chaos, and disclose.io all checked — 0 new assets or programs this window. FireBounty still a first run, no assets attributed._

### 2026-09-05
- John Deere — 2 domains/URLs
Total: 2 domains/URLs

_Sources: arkadiyt/bounty-targets-data and bbscope.com agree on 2 new John Deere domains. A flagged DataCamp "new program" was discarded as an already-established program (2,119 submissions) newly tracked, not new scope. Chaos and disclose.io: 0 new; FireBounty still a first run._

### 2026-09-04
- WP Engine Bug Bounty — 6 domains/URLs
- John Deere — 5 domains/URLs
- Fifth Third Bank VDP — 2 domains/URLs
- T Mobile — 1 domains/URLs
Total: 14 domains/URLs

_Sources: arkadiyt/bounty-targets-data confirmed these 14 via real snapshot diff. bbscope.com's other 32 reported additions were cross-checked against the snapshot and found unchanged (re-fired, not new) — dropped. Chaos and disclose.io: 0 new; FireBounty still a first run._

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
