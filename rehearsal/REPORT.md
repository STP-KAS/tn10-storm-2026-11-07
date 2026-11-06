> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only. No txid, key, seed, IP, host, port, covenant id or wallet address.
>
> Dress rehearsal of the Saturday plan. Label **A** for the counts below.

# Dress rehearsal, Thu 5 Nov 2026

This is not the Saturday storm. Saturday stays **7 Nov 2026, 19:00–21:00 UTC (20:00–22:00 CET)**. The Saturday sender starts at 19:00 UTC and not before. Nothing in this folder moves that clock, the 1.2 rate, or the abort line of 2,500 coins and 18,000 usable tKAS.

The paste for Saturday is the sheet itself: [GO-BUILD](../go/GO-BUILD.md), [GO-MINI](../go/GO-MINI.md), [GO-BOT](../go/GO-BOT.md). Pasting one before Saturday does not start a sender.

## Shape

The run followed [plan/PLAN.md](../plan/PLAN.md) on a clock of its own. One desk sender. One relay, boson. Stagger 0. No phase offset. Heartbeat 900 ms. Offered rate **1.2** on f1, f2, f4 and f8. The Saturday gate decided f8 and the ramp. Miners off. Both nodes were synced on TN10 with 8 peers. The desk clock was within 1 ms of NTP. Genesis included all 8 families. Preflight passed the 2,500 coin and 18,000 usable line.

| | UTC | Desk local (CET, UTC+1) |
|---|---|---|
| Genesis | Thu 5 Nov 2026, **22:01:55** | **23:01:55** |
| Start, f1 | **22:07:00** | **23:07:00** |
| Last hop | **23:29:50** | Fri 6 Nov, **00:29:50** |
| Schedule end | **23:36:50** | **00:36:50** |
| Census | **23:46:58** | **00:46:58** |

The steps, measured from 22:07:00 UTC:

| Step | UTC | Families | Accepted /s | Slowest family |
|---|---|---:|---:|---:|
| f1 | 22:07–22:22 | 1 | 1.409 | 1.409 |
| f2 | 22:27–22:42 | 2 | 1.382 | 1.358 |
| f4 | 22:47–23:02 | 4 | 1.339 | 1.317 |
| f8 | 23:07–23:22 | 8 | 1.283 | 1.223 |
| r1 | 23:27:00–23:27:50 | 4 | 1.355 | 1.320 |
| r2 | 23:28:00–23:28:50 | 4 | 1.330 | 1.300 |
| r3 | 23:29:00–23:29:50 | 4 | 1.310 | 1.280 |

Gaps had no attempts. A few accepts from the step that just ended were timestamped in the first seconds of the next gap. r4 through r10 had no attempts.

## Gate

f4, 900 seconds, 4 families. An attempt in every second. First attempt at 0.02 s. Accepted 1.339 hop/s per family. Slowest family 1.317. No sender-off, pool-low, node-drop, or proc-exit. Landing 97.33%. The gate logged that landing and opened f8. Landing did not decide.

Every full minute of f1, f2 and f4 was at or above 1.14 on the slowest family. The worst of those minutes was f4 at 22:59 UTC, 1.233.

f8 ran. An attempt in every second, on every family. First attempt at 0.04 s. Accepted 1.283 hop/s per family. Slowest family over the 15 minutes was 1.223. Landing 98.33%. One full minute, 23:11 UTC, had a slowest family of 1.133. The other 14 minutes were at or above 1.14. The Saturday gate uses the whole step, not one minute, and this step stayed above 1.14.

| Family | f8 hops | Accepted /s |
|---|---:|---:|
| 1 | 1,212 | 1.347 |
| 2 | 1,189 | 1.321 |
| 3 | 1,172 | 1.302 |
| 4 | 1,163 | 1.292 |
| 5 | 1,137 | 1.263 |
| 6 | 1,131 | 1.257 |
| 7 | 1,133 | 1.259 |
| 8 | 1,101 | 1.223 |

The ramp offered 1.2, then 1.3, then 1.4, each for 50 seconds, four families. Acceptance went 1.355, then 1.330, then 1.310. The gains were −1.8% and −1.5%. Two gains under 3% stop the ramp. The gate wrote that stop at 23:29:53 UTC, after r3. The later steps stayed off. The last hop is 23:29:50 UTC.

## Accepted hops

18,637 hops. The mini's own counter matched 18,637 of 18,637. No duplicate id. None at or after the schedule end. Every hop had a header time.

The desk logged 18,637 ok submits, and each one has a hop row. Attempts 22,321. Rejected 3,684, of which 1,420 were already spent and 2,264 were orphan. The relay accepted 18,552 of the 18,637 ok submits and rejected 85.

Submit time to the accepting header, on all 18,637 hops: p50 583 ms, p95 1,037 ms, p99 1,244 ms.

Builder time on the ok submits inside the steps: p50 5 ms, p95 21 ms. Builder queue p50 1, p95 6, max 7. Submit call p50 1 ms, p95 3 ms.

No sender-off, pool-low, node-drop, proc-exit, or family-drop in the run.

## After the last hop

Sweeps at 75 s, 180 s and 360 s after the schedule end. The desk had 0 of ours at each sweep, and nothing to replace. The mini had 1 of ours at each sweep. That one had no live funding input, so the sweep did not replace it.

The census about 10 minutes after the schedule end was the same: desk 0, mini 1. A later read, at 00:00 UTC on 6 Nov, still showed that one transaction on the mini, and an empty desk mempool. It was not marked orphan. It did not stop the send, the gate, or the count.

## What Saturday still does

Saturday uses the clocks in [plan/PLAN.md](../plan/PLAN.md), not the clocks in this folder. Recount the lane before genesis. The abort line stays 2,500 coins and 18,000 usable tKAS. Family-id hashes, miner lines, and the NTP samples wait for Saturday, before 18:40 UTC.
