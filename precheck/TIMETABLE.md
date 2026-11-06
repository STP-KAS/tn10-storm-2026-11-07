> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only.
>
> Friday 6 Nov 2026. This check is for Saturday. It is not the Saturday window.

# Timetable

One desk sender. The mini counts on its own node and does not send. Rate **1.2** on f1, f2, f4 and f8. The Saturday gate opens f8: an attempt in every second, acceptance at least 1.14 per family, no sender-off, pool-low, node-drop or proc-exit. Landing percent is logged and does not decide.

A round is clean when f4 opens f8, every counted step holds at least 1.14 per family over the whole step, and nothing fires those faults. One low minute is written down. It does not by itself fail the step.

| | UTC | CET (UTC+1) |
|---|---|---|
| Mini counter on | Fri 6 Nov, **19:49** | **20:49** |
| Round 1 sends | **19:51–21:20:50** | **20:51–22:20** |
| Round 2 sends | **22:01–23:30:50** | **23:01–00:30** |
| Mini counter off | Sat 7 Nov, **08:00** | **09:00** |

Leave the counter on through both rounds. Round 2 starts only if round 1 is clean. If a round is not clean, it is fixed and run again. This page is updated before the new clock, and the mini does not need a new paste while its counter is still on.

The mini counter stays up until **Sat 7 Nov 2026, 08:00 UTC (09:00 CET)**. That covers a rerun of round 1 or round 2. It is not the Saturday count. Saturday still starts its own counter at 18:58 UTC.

The steps inside each round, from that round's start:

| Step | From start | Families | Rate |
|---|---|---:|---:|
| f1 | 0–15 min | 1 | 1.2 |
| gap | 15–20 min | 0 | 0 |
| f2 | 20–35 min | 2 | 1.2 |
| gap | 35–40 min | 0 | 0 |
| f4 | 40–55 min | 4 | 1.2 |
| gap | 55–60 min | 0 | 0 |
| f8 | 60–75 min | 8 | 1.2, only if f4 is clean |
| gap | 75–80 min | 0 | 0 |
| ramp | 80–90 min | 4 | 1.2 then +0.1, 50 s on / 10 s off |

The ramp stops on two gains in a row under 3%.

An earlier arm the same evening was halted at 19:13 UTC. The mini prompt was not in. Those minutes are not a round.
