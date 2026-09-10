# RecentBBP

Tracks bug bounty program scope assets — domains, wildcard domains, URLs, IPs, and CIDR ranges — newly added to public bug bounty and VDP program scopes, aggregated on a recurring schedule from free, open-source scope-data sources (arkadiyt/bounty-targets-data, bbscope.com, FireBounty, Chaos, disclose.io).

Out-of-scope items and non-network assets (mobile apps, source repos, hardware, SaaS tenants, etc.) are excluded — only domains, wildcards, URLs, IPs, and CIDR ranges are tracked.

## Files

- `domains.txt` — master, append-only, deduplicated list of every in-scope domain / wildcard domain / URL seen across all runs. One asset per line, no other content.
- `ips.txt` — master, append-only, deduplicated list of every in-scope IP / CIDR range seen across all runs. One asset per line, no other content.
- `daily/YYYY-MM-DD-domains.txt` / `daily/YYYY-MM-DD-ips.txt` — only the assets first observed on that run's date (i.e. not already present in the master lists). Omitted for a date if nothing new was found.
- This README's log below — one dated entry per run, newest first, listing each program and how many assets it contributed (no asset values here; see the .txt files for those).

### 2026-09-10
- Expedia Group — 16 domains/URLs
Total: 16 domains/URLs

_Sources: bbscope.com (reachable, 24h window by real event timestamps — `since=1d`/`since=today` params still unreliable server-side) surfaced 114 in-window "added"/in-scope events across 13 programs; after dropping mobile/hardware/non-asset rows, 76 candidate domains/URLs remained. arkadiyt/bounty-targets-data (git-history diff, base 2026-09-09 → head 2026-09-10) independently corroborated the bulk of these plus flagged Scopely as a new program. Chaos and disclose.io: 0 new programs/domains. FireBounty: reachable, first run in this environment (no persisted snapshot) returned 10 candidate TUI-group subdomains, but a live spot-check of one entry (`www.fritidsresor.se`) showed it was published to FireBounty on 2026-06-22, not today — all 10 discarded as unconfirmed. Every surviving candidate was then checked against its live platform. HackerOne programs (Essity, ABB, John Deere, Expedia Group, Scopely, Global Payments) were queried directly via HackerOne's public structured-scope data, which carries real per-asset `created_at` timestamps — this caught several aggregator false positives (Scopely's 3 wildcards from 2017–2020, Expedia's `*.hotwire.com`/`*.expediacruises.com`/`www.expediacruises.com`/`www.expediapartnercentral.com` with old `created_at`, `*.tigets.com`/`www.tigets.com` a typo'd duplicate no longer in live scope, Global Payments' `globalpayments.com` an `OTHER`-type company-name entry from 2021), leaving only 16 of Expedia's 22 candidates with `created_at` genuinely inside the last 24h. Essity (2) and ABB/John Deere (3) were initially kept on two-source agreement alone (bbscope timestamp + arkadiyt git-diff) without a confirmed live `created_at` — on review this wasn't a strong enough bar, and Essity/ABB/John Deere are VDP programs (no bounty) besides, so all 5 were pulled back out. Bugcrowd programs (codeclou, THG, maffashion, OpenAI, SimpliSafe — 44 candidate assets) have no public unauthenticated scope API or embedded page data (JS-rendered SPA) so could not be independently re-verified against the live platform at all; rather than publish them on the aggregator's unconfirmed diff alone, all 44 were pulled back out pending a verification method that can actually check Bugcrowd's live scope. `/engagements/umbrella-demo-vdp-pro`'s `www.umbrella.corp` was discarded as a Bugcrowd demo/practice program, not a real target. Net result: only Expedia Group's 16 assets meet both bars — confirmed live `created_at` inside the last 24h, and a paid bounty (not VDP) program._

### 2026-09-09
- TransUnion LLC — 1 domains/URLs
- MoonPay — 1 domains/URLs
- Bitso Managed Bug Bounty Engagement — 1 domains/URLs
Total: 3 domains/URLs

_Sources: arkadiyt/bounty-targets-data (24h git-history diff, base 2026-09-08 → head 2026-09-09) surfaced 16 candidate assets across 6 programs plus 3 candidate new-program flags (Brave, Quizlet, SoundCloud). bbscope.com was reachable but its free-tier `updates` API is now masking the `target` field on most `added`/in-scope events with block-character placeholders (paywalled) — unusable for asset values, though program/category/timestamp metadata still comes through unmasked on a subset of records, which was enough to cross-check freshness. Per-asset verification against that live bbscope event stream: Quizlet's `*.quizlet.com` and all 8 SoundCloud assets showed the exact same "added" events re-firing identically every ~3 hours paired with a "removed PROGRAM" event each cycle — the same re-parse/churn artifact this repo has discarded before, not real new scope, so both programs (9 assets) were discarded; Taxwell VDP's 4 assets (`1040.com`, `securefilepro.com`, `taxwell.com`, `taxwell.org`) showed as "updated" events, not "added", so pre-existing scope, discarded. The remaining 3 — TransUnion's `administracionpreaprobadomovil.cifin.co`, MoonPay's `*.swaps.xyz`, and Bitso's `onchain.cc` — each showed a single non-repeating "added"+"in" event on bbscope independently corroborating arkadiyt's snapshot diff, and were kept. Brave's "new program" flag carried no domain/URL assets (only app-store/binary/code categories), so nothing to add there. Chaos and disclose.io checked, no new programs/domains today. FireBounty was reachable but returned the same TUI-group feed ids already checked and discarded in the 2026-09-08 entry (stale, last crawled 2026-06-22) — no new IDs above that range._

### 2026-09-08
- Weblate — 1 domains/URLs
- MercadoLibre — 3 domains/URLs
- Semrush — 1 domains/URLs
- Randstad — 3 domains/URLs
Total: 8 domains/URLs

_Sources: bbscope.com (reachable, `since=today`, 0 new additions — 2 program removals only) and arkadiyt/bounty-targets-data (24h git-history diff, base 2026-09-07 → head 2026-09-08) checked. arkadiyt's diff surfaced 14 candidate assets across 5 programs; after verification each was checked against its actual platform: `velocitize.com` (WP Engine, Intigriti) was discarded — the live program page now marks it explicitly out of scope/no bounty. Five more (`makeshift.film`, `payments.wpengine.com`, `torquemag.io`, `*.localwp.com`, `*.nitropack.io`, all WP Engine) were discarded as duplicates already recorded in this repo's 2026-09-04 entry, not new today. The remaining 8 — Weblate's `hosted.weblate.org`, MercadoLibre's `www.ipbooster.com`/`*.mercadolibre.com.ve`/`*.tucarro.com.ve`, Semrush's `www.semrush.com`, and Randstad's 3 wildcards — were kept; Randstad's 3 were independently confirmed live and in-scope on Intigriti, while the HackerOne-hosted ones (Weblate, MercadoLibre, Semrush) could not be re-verified live since HackerOne's program pages are JS-rendered SPAs with no accessible public scope API, so they rely on arkadiyt's official-API snapshot diff alone. Chaos and disclose.io checked, no new programs/domains today. FireBounty was reachable and returned 10 candidate TUI-group subdomains, but its local diff snapshot doesn't persist across sessions in this environment (first run again) and a live spot-check of one entry showed the underlying program was last crawled/dated 2026-06-22 — not today — so all 10 were discarded as unconfirmed._

### 2026-09-07
- Basecamp — 1 domains/URLs
Total: 1 domains/URLs

_Sources: bbscope.com (reachable; `since=1d` still non-functional server-side — 40 pages fetched, newest real timestamp 2026-09-06T17:47:27Z, 0 events dated 2026-09-07 itself) and arkadiyt/bounty-targets-data (24h git-history diff, base 2026-09-06 → head 2026-09-07) independently agree on 1 new asset: `app.fizzy.do` on Basecamp's HackerOne program. Corroborated against Basecamp's public "Introducing Fizzy" product announcement (a newly launched 37signals product), supporting that this is genuinely new scope rather than newly-tracked pre-existing scope. Chaos and disclose.io checked, no new programs/domains today. FireBounty was reachable but is still a first run in this environment (no snapshot persisted across sessions), so no assets are attributed to it today._

### 2026-09-06
No new assets.

_Sources: bbscope.com (reachable, `since=1d` still non-functional server-side, filtered by real event timestamps — only one in-window event, a GitHub repo, out of scope), arkadiyt/bounty-targets-data (24h git-history diff, base 2026-09-05 → head 2026-09-06, 0 new assets/programs), Chaos and disclose.io (no new programs/domains). FireBounty was reachable but is still a first run in this environment (no snapshot persisted across sessions), so no assets are attributed to it today._

### 2026-09-05
- John Deere — 2 domains/URLs
Total: 2 domains/URLs

_Sources: arkadiyt/bounty-targets-data (24h git-history diff, base 2026-09-04 → head 2026-09-05) confirmed 2 new John Deere domains, cross-checked against the live snapshot (in_scope count 2017→2019, both new targets present) — bbscope.com independently logged the same 2 assets with real add timestamps, agreeing across two sources. arkadiyt also flagged a new program, DataCamp (Intigriti, 9 domain/wildcard assets), but the live Intigriti program page shows 2,119 submissions and €80,000 in payouts already — an established program, not a new one — so those 9 assets were discarded as pre-existing scope that bounty-targets-data only just started tracking, not new scope. bbscope.com's `since=1d` parameter is still non-functional server-side (fetched pages topped out at 2026-09-04T15:52Z with 1036 total pages available), so it was used only to corroborate arkadiyt's finds, not as a standalone source. Chaos and disclose.io checked, no new programs/domains today. FireBounty was reachable but is still a first run in this environment (no snapshot persisted across sessions), so no assets are attributed to it today._

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
