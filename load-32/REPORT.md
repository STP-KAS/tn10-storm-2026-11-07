> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only. No txid, key, seed, IP, host, port, covenant id or wallet address.
>
> Another 32-family load, initiated by this desk (STP). Label **A** for the counts below.

# 32-family load, night of 6 Nov 2026

This is not the Saturday storm. Saturday stays **7 Nov 2026, 19:00–21:00 UTC (20:00–22:00 CET)**. The Saturday sender starts at 19:00 UTC and not before. Nothing in this folder moves that clock, the 1.2 rate, or the abort line of 2,500 coins and 18,000 usable tKAS.

The Friday check in [precheck/](../precheck/DESK.md) is the two Saturday-shaped rounds. This load came after both of those rounds were clean. It is the same shape as the [5 Nov load](../one-time/REPORT.md).

## Shape

| | UTC | Desk local (CET, UTC+1) |
|---|---|---|
| Start | Fri 6 Nov 2026, **23:57** | Sat 7 Nov, **00:57** |
| End | Sat 7 Nov, **00:42** | **01:42** |

2,700 seconds. 32 families from the first second. One desk sender. Offered rate **1.2** accepted hop/s per family, held for the whole window. One relay, boson. Stagger 0. No phase offset. Heartbeat 900 ms. Miners off. The desk clock was about 3 ms off NTP. Genesis included all 32 families. Preflight passed. The fee was not raised.

## Accepted hops

93,289 hops in the window. The desk's read of the mini node matched 93,289 of 93,289. No duplicate. None at or after the end.

| | per family |
|---|---:|
| Slowest | **1.047**/s, family 30, 2,828 hops |
| Average | 1.080/s |
| Fastest | 1.149/s, family 1, 3,101 hops |
| All 32 together | 34.55/s |

The pass line used on the Saturday plan is 1.14. The slowest family over this window was under it. The fastest family over the whole window was just over it. Every one of the 45 full minutes had a slowest family under 1.14. The worst full minute was **0.933**/s, at 23:58 UTC (00:58 CET). Three full minutes were under 0.95. Twenty-five were under 1.00. The best full minute was 1.083/s, at 00:11 UTC. No family stopped.

On 5 Nov the same shape accepted 33.86/s, slowest family 1.037/s, worst full minute 0.833/s. Tonight was a little higher and a little steadier. The per-family ceiling did not move up to the offered 1.2.

The desk logged 93,317 ok submits in the window. 93,289 of them are the hop rows above. Attempts 127,238. Rejected 33,921, of which 20,890 were already spent and 13,031 were orphan. Those rejects are the families contending. They are not a fee miss.

Union landing 99.67% (9 empty seconds of 2,700). That is a score. On Saturday it does not open or close a step.

Submit time to the accepting header, on 93,281 hops: p50 708 ms, p95 1,274 ms, p99 1,564 ms. Eight hops had no header time.

Builder time on the ok submits: p50 13 ms, p95 69 ms. Builder queue p50 6, p95 17, max 62. Submit call p50 1 ms, p95 3 ms. The builder was busier than on 5 Nov. It was not the ceiling. The ceiling was still how many hops the network accepted per family.

## Node and coordinator

No family drop. No stall. No sender-off, pool-low, node-drop, or proc-exit. The desk node and the tunnel were still up at the census.

Sweeps at 75 s, 180 s and 360 s after the end found nothing to replace. The census about 10 minutes after the end was 0 of ours on the desk and 0 on the mini node.

## What this does not change

Saturday is still 8 families at 1.2, with f8 only if f4 is clean. This window shows what 32 families do. It does not raise Saturday's rate.
