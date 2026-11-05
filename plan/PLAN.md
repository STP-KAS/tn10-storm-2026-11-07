> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only.

# Saturday steps

Window: **Sat 7 Nov 2026, 19:00–21:00 UTC (20:00–22:00 CET).**

One sender, the desk, from the first second of each step. The mini counts. Rate **1.2** accepted hop/s per family on f1, f2, f4 and f8. The gate that opens f8 is the one in [desk-saturday](https://github.com/STP-KAS/tn10-storm/tree/main/desk-saturday): an attempt in every second, acceptance at least 1.14 per family, no sender-off, pool-low, node-drop or proc-exit. Landing percent is logged and does not open or close f8.

| Step | UTC | CET | Families | Rate |
|---|---|---|---:|---:|
| f1 | 19:00–19:15 | 20:00–20:15 | 1 | 1.2 |
| gap | 19:15–19:20 | 20:15–20:20 | 0 | 0 |
| f2 | 19:20–19:35 | 20:20–20:35 | 2 | 1.2 |
| gap | 19:35–19:40 | 20:35–20:40 | 0 | 0 |
| f4 | 19:40–19:55 | 20:40–20:55 | 4 | 1.2 |
| gap | 19:55–20:00 | 20:55–21:00 | 0 | 0 |
| f8 | 20:00–20:15 | 21:00–21:15 | 8 | 1.2, only if f4 is clean |
| gap | 20:15–20:20 | 21:15–21:20 | 0 | 0, only if f8 ran |
| ramp | 20:20–20:30 | 21:20–21:30 | 4 | 1.2 then +0.1, ten steps of 50 s on / 10 s off |

If f4 is not clean, f8 is skipped and the same ramp starts at 20:00 UTC (21:00 CET).

The ramp stops on two gains in a row under 3%. The listed top is 2.1. The 5 Nov holds and the earlier ramp were already flat near 1.3 accepted/s per family, so this ramp is expected to stop within a step or two.

Per complete UTC minute, if the rate holds, our own addition is about 1.2, 2.4, 4.8, then 9.6 hop/s, and then the ramp. Gaps and 20:30–21:00 UTC should show base load and none of our hops.

Checks at 18:40 UTC (19:40 CET): both nodes synced on TN10, peers at least 8, clocks within 80 ms, miners off, family-id hashes delivered, boson answers, sender key at least 2,500 coins and 18,000 usable tKAS. A miss aborts. No hop is sent early.

Genesis at 18:55 UTC (19:55 CET), eight families. The mini's counter goes on at 18:58 UTC and off at 21:00 UTC.

Private submit times stay off this repo. After the run the public numbers are p50, p95 and p99 of submit to accepting header, and the accepted hops per family per step.
