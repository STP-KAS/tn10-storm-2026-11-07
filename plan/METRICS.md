> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only.

# Metrics

The headline is accepted hops per second, per family, over each full step, and the same number per complete UTC minute.

If the 1.2 hold stands, our own addition is about:

| Families | Hop/s |
|---:|---:|
| 1 | 1.2 |
| 2 | 2.4 |
| 4 | 4.8 |
| 8 | 9.6 |

The outside count buckets by block time, per UTC minute. Base load stays in that network total. Gaps, and 20:30–21:00 UTC, should show that base load and none of our hops.

After the window the public numbers are p50, p95 and p99 of submit time to the accepting header, plus the accepted hops per family per step. The submit rows stay private. See [LOGGING.md](../go/LOGGING.md).
