# Hosting retirement status — 2026-11-06

This is the status recorded during the domain migration. It distinguishes completed dedicated-backend and DNS retirement from Vercel-only cleanup. Retired hostnames have no replacement on `skylar.sh`. References below can be external dependencies; they do not imply this repository owns every service.

| Endpoint | Verified status |
|---|---|
| `arena.skylarenns.com` | DNS record removed and Vercel custom-domain binding/alias absent. Dedicated backend shutdown is not established by those operations; preserve any retained shared service. No replacement hostname. |
| `arenaapi.skylarenns.com` | DNS record removed and Vercel custom-domain binding/alias absent. Dedicated backend shutdown is not established by those operations; preserve any retained shared service. No replacement hostname. |

## Documentation and deployment examples

The original URLs in source, environment examples and historical operational instructions are retained for provenance and rollback. They are not an instruction to recreate a retired public endpoint. Do not substitute the skylar.sh suffix for retirement-listed services. Local development instructions remain useful; hosting claims must be interpreted using the endpoint status above.

Migration-listed external dependencies still require their own verified cutover. Keep their legacy addresses while authentication, callbacks and cross-service behavior are being checked. Personal website/email addresses and explicitly retained applications stay on skylarenns.com.

No repository, database, recording, volume or configuration was deleted by this documentation change. Vercel project deletion is not implied by removal of its custom-domain binding.

## Evidence and rollback

The operator migration bundle contains `migration/retirement-results.md`, `migration/cloudflare/retired-dns-ledger.ndjson`, and `migration/vercel-retirement-ledger.json`. These are operational evidence paths, not files claimed to exist in this repository. Dedicated service/container originals and rollback commands are recorded separately in `migration/retirement-execution.json` and `migration/retirement-containers-execution.json`; DNS and Vercel snapshots remain separate. Restore only the exact intended service and dependency state during a deliberate rollback.

Later verified update (2026-11-06): retirement DNS cleanup now covers 66 explicitly retired hostnames. This does not broaden dedicated-service shutdown claims; the migration operator preserves shared processes and state. The core canonical platform deployment was rolled back, so new API source references must not be treated as completed production cutover.
