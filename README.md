# RecentBBP

Tracks bug bounty program scope assets — domains, wildcard domains, URLs, IPs, and CIDR ranges — newly added to public bug bounty and VDP program scopes, aggregated on a recurring schedule from free, open-source scope-data sources (arkadiyt/bounty-targets-data, bbscope.com, FireBounty, Chaos, disclose.io).

Out-of-scope items and non-network assets (mobile apps, source repos, hardware, SaaS tenants, etc.) are excluded — only domains, wildcards, URLs, IPs, and CIDR ranges are tracked.

## Files

- `domains.txt` — master, append-only, deduplicated list of every in-scope domain / wildcard domain / URL seen across all runs. One asset per line, no other content.
- `ips.txt` — master, append-only, deduplicated list of every in-scope IP / CIDR range seen across all runs. One asset per line, no other content.
- `daily/YYYY-MM-DD-domains.txt` / `daily/YYYY-MM-DD-ips.txt` — only the assets first observed on that run's date (i.e. not already present in the master lists). Omitted for a date if nothing new was found.
- This README's log below — one dated entry per run, newest first, listing each program and how many assets it contributed (no asset values here; see the .txt files for those).

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
