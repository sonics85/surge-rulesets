# surge-rulesets

Auto-generated Surge-format rule-sets, refreshed daily via GitHub Actions.

## Files

- `ru-asn-prefixes.list` — IPv4 + IPv6 CIDR prefixes for all RU autonomous systems (RIPE NCC).

## Source

Upstream: [mrixs/ru_asn_prefixes](https://github.com/mrixs/ru_asn_prefixes) (WTFPL).
This repo wraps each line with `IP-CIDR,…,no-resolve` / `IP-CIDR6,…,no-resolve` so Surge consumes it directly.

## Use in Surge

```
RULE-SET,https://raw.githubusercontent.com/sonics85/surge-rulesets/main/ru-asn-prefixes.list,RU
```

## Refresh schedule

GitHub Action runs daily at 03:30 UTC (after upstream's 02:00 UTC update).
