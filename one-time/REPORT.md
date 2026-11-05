> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only. No txid, key, seed, IP, host, port, covenant id or wallet address.
>
> One-time test, for later review by Pulse, initiated by this desk (STP), to see what happens. Label **A** for the counts below.

# One-time load, Thu 5 Nov 2026

This is not the Saturday storm. Saturday stays **7 Nov 2026, 19:00–21:00 UTC (20:00–22:00 CET)**. The Saturday sender starts at 19:00 UTC and not before. Nothing in this folder moves that clock, the 1.2 rate, or the abort line of 2,500 coins and 18,000 usable tKAS.

## Shape

| | UTC | Desk local (CET, UTC+1) |
|---|---|---|
| Start | Thu 5 Nov 2026, **17:29:46** | **18:29:46** |
| End | **18:14:46** | **19:14:46** |

2,700 seconds. 32 families from the first second. One desk sender. Offered rate **1.2** accepted hop/s per family, held for the whole window. One relay, boson. Stagger 0. No phase offset. Heartbeat 900 ms. Miners off. The desk clock was within 1 ms of NTP. Genesis included all 32 families. Preflight passed.

Before the window the sender key was topped up with 320 coins of 500 tKAS, and the 24 new family keys each received one genesis coin of 20 tKAS. Usable on the sender key at the start was 216,277 tKAS.

## Accepted hops

91,424 hops in the window. The mini's own counter matched 91,424 of 91,424.

The desk logged 91,456 ok submits. 32 of those have no hop row. The counted set is the 91,424.

| | per family |
|---|---:|
| Slowest | **1.037**/s |
| Average | 1.058/s |
| Fastest | 1.100/s |
| All 32 together | 33.86/s |

The pass line used on the Saturday plan is 1.14. Every one of the 44 full minutes was under it. The worst full minute was **0.833**/s, at 18:00 UTC (19:00 CET). The same floor, 0.833, came again at 18:01. The last full minute, 18:13, was 0.983. No family stopped.

The 8-family hold earlier the same day was slowest at 1.260/s. This window's slowest family was 1.037/s. Total acceptance was higher. Per-family acceptance was lower.

Union landing 99.67% (9 empty seconds of 2,700). That is the same union score as the holds. It is a score. On Saturday it does not open or close a step.

Submit time to the accepting header, on 91,416 of the 91,424 hops: p50 718 ms, p95 1,326 ms, p99 1,683 ms. Eight hops had no header time.

Attempts: 127,264. Ok 91,456. Rejected 35,808, of which 21,889 were already spent and 13,919 were orphan. The relay accepted 91,333 of the 91,456 ok submits and rejected 123.

An attempt landed in every second for families 1–22 and 27. The other families missed 1 to 4 seconds each. Across 32 × 2,700 family-seconds, 24 seconds had no attempt.

Builder time on the ok submits: p50 5 ms, p95 14 ms. Builder queue p50 5, p95 17, max 61. Submit call p50 under 1 ms, p95 1 ms.

The 14-second head and the 46-second tail hold 2,088 hops between them. Those clips are not full minutes.

### Per family, whole window

| Family | Hops | Accepted /s |
|---|---:|---:|
| 1 | 2,969 | 1.100 |
| 2 | 2,942 | 1.090 |
| 3 | 2,898 | 1.073 |
| 4 | 2,869 | 1.063 |
| 5 | 2,890 | 1.070 |
| 6 | 2,827 | 1.047 |
| 7 | 2,846 | 1.054 |
| 8 | 2,831 | 1.049 |
| 9 | 2,886 | 1.069 |
| 10 | 2,834 | 1.050 |
| 11 | 2,850 | 1.056 |
| 12 | 2,846 | 1.054 |
| 13 | 2,907 | 1.077 |
| 14 | 2,801 | 1.037 |
| 15 | 2,873 | 1.064 |
| 16 | 2,863 | 1.060 |
| 17 | 2,863 | 1.060 |
| 18 | 2,825 | 1.046 |
| 19 | 2,870 | 1.063 |
| 20 | 2,872 | 1.064 |
| 21 | 2,854 | 1.057 |
| 22 | 2,821 | 1.045 |
| 23 | 2,803 | 1.038 |
| 24 | 2,822 | 1.045 |
| 25 | 2,833 | 1.049 |
| 26 | 2,841 | 1.052 |
| 27 | 2,877 | 1.066 |
| 28 | 2,831 | 1.049 |
| 29 | 2,854 | 1.057 |
| 30 | 2,808 | 1.040 |
| 31 | 2,845 | 1.054 |
| 32 | 2,873 | 1.064 |

### Slowest family in each full minute

A full minute is 60 seconds. The first full minute starts 17:30:00 UTC. The number is that minute's slowest family, in accepted hop/s. CET is one hour later.

| UTC | Floor |
|---|---:|
| 17:30 | 0.983 |
| 17:31 | 1.033 |
| 17:32 | 0.967 |
| 17:33 | 1.000 |
| 17:34 | 1.017 |
| 17:35 | 0.933 |
| 17:36 | 1.067 |
| 17:37 | 0.933 |
| 17:38 | 1.000 |
| 17:39 | 1.000 |
| 17:40 | 0.983 |
| 17:41 | 1.017 |
| 17:42 | 0.983 |
| 17:43 | 1.017 |
| 17:44 | 0.950 |
| 17:45 | 1.000 |
| 17:46 | 0.950 |
| 17:47 | 1.067 |
| 17:48 | 0.983 |
| 17:49 | 0.983 |
| 17:50 | 1.000 |
| 17:51 | 1.017 |
| 17:52 | 1.067 |
| 17:53 | 1.067 |
| 17:54 | 1.067 |
| 17:55 | 1.017 |
| 17:56 | 1.050 |
| 17:57 | 0.900 |
| 17:58 | 0.883 |
| 17:59 | 0.850 |
| 18:00 | 0.833 |
| 18:01 | 0.833 |
| 18:02 | 0.867 |
| 18:03 | 0.900 |
| 18:04 | 0.867 |
| 18:05 | 0.867 |
| 18:06 | 0.933 |
| 18:07 | 0.933 |
| 18:08 | 0.867 |
| 18:09 | 0.900 |
| 18:10 | 0.900 |
| 18:11 | 0.950 |
| 18:12 | 0.967 |
| 18:13 | 0.983 |

16 of these 44 minutes were under 0.95. 27 were under 1.00. All 44 were under 1.14.

## Pool

The sender's low-pool line is 100 coins. It logged that line through the second half of the window. The sender stayed up. There was no sender-off, no family-drop, no node-drop, and no proc-exit. Of the 5-second samples inside the window, 37 were under 100 coins and one was 18.

After the window the 320 funding coins were still on the sender key, each still above 100 tKAS. Usable on them was 122,357 tKAS. Each hop also leaves a 1 tKAS token output on that same key. The pool ignores an output at or under 3 tKAS. One read of the key returned 11,430 entries, including all 320 funding coins. The token outputs fill the rest of that read, and the call stopped there.

Sweeps at 75 seconds, 180 seconds and 360 seconds after the end found 0 of ours on the desk and 0 of ours on the mini, and replaced nothing. At 10 minutes after the end the mempool census was 0 of ours on the desk and 0 of ours on the mini.

## What this does not change

Saturday is unchanged. One sender. Rate 1.2. Steps of 1, then 2, then 4, then 8 if 4 is clean. The 99% landing score stays a score. This 32-family load is the side test it says it is.
