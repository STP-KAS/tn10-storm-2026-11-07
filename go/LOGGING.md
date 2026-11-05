> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only.

# Logging

Public files land under [logs/](../logs/README.md) after 21:00 UTC (22:00 CET). Until then that folder stays empty.

What may be published:

- accepted hops per family per step
- the same number per complete UTC minute
- p50, p95 and p99 of submit time to the accepting header
- NTP offsets in milliseconds, with the UTC time, and nothing else
- one miner line per machine: `MINERS <machine> n=<count>`

What stays off this repo: txids, keys, seeds, addresses, IPs, hosts, ports, covenant ids, and the private submit rows. The mini's accepted-id file stays on the mini.
