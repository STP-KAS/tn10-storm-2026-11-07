> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only.

# Desk

The desk is the only sender.

- Before 18:40 UTC (19:40 CET): node synced on TN10, peers at least 8, clock within 80 ms, miners off, relay answers, lane at least 2,500 coins and 18,000 usable tKAS.
- 18:55 UTC (19:55 CET): genesis for 8 families.
- 19:00 UTC (20:00 CET): sender on, rate 1.2, the steps in [../plan/PLAN.md](../plan/PLAN.md).
- Do not start the sender before 19:00 UTC.
- Do not add a second sender. Do not add a phase offset.
- Family ids stay in a private file. Deliver the hashes before 18:40 UTC. Do not commit them.
- Submit times stay private. Publish percentiles after the window, not the rows.
