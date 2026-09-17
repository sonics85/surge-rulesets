# surge-rulesets

Auto-generated Surge-format rule-sets, refreshed daily via GitHub Actions.

## Files

- `ru-asn-prefixes.list` — IPv4 + IPv6 CIDR prefixes for all RU autonomous systems (RIPE NCC).
- `mirror/` — verbatim copies of the three upstream lists the Surge profile also consumes,
  refreshed daily so every rule-set has a single origin that can be mirrored off GitHub
  in one move: `proxy-from-ru.list`, `inside-clashx.lst`, `community.lst`.

## Source

Upstream: [mrixs/ru_asn_prefixes](https://github.com/mrixs/ru_asn_prefixes) (WTFPL).
This repo wraps each line with `IP-CIDR,…,no-resolve` / `IP-CIDR6,…,no-resolve` so Surge consumes it directly.

## Use in Surge

```
RULE-SET,https://raw.githubusercontent.com/sonics85/surge-rulesets/main/ru-asn-prefixes.list,RU
```

## Refresh schedule

- `update.yml` — daily at 03:30 UTC (after upstream's 02:00 UTC update).
- `mirror-upstream.yml` — daily at 03:45 UTC; fails loudly if a list comes back short.
