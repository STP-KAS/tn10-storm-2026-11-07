> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only.

# Two plans

Saturday's sheet does not move. Plan 1 is that sheet. Plan 2 is the same sheet, then one load after the counter is off. Plan 2 runs only if the outside counter wants it.

Pasting a sheet before its own clock does not start a sender and does not start a counter.

## Plan 1

The window already under review.

| | UTC | Desk local (CET, UTC+1) |
|---|---|---|
| Checks | Sat 7 Nov 2026, **18:40** | **19:40** |
| Genesis | **18:55** | **19:55** |
| Counter on | **18:58** | **19:58** |
| START | **19:00** | **20:00** |
| Sends finished | **20:30** | **21:30** |
| Counter off | **21:00** | **22:00** |

One sender, the desk, on from the first second of each step. 1 family, then 2, then 4, then 8 if 4 is clean. One rate, **1.2** accepted hop/s per family. Pass line **1.14**. Landing is written down. It does not open or close the 8-family step. The ramp is 10 minutes, steps of 0.1 from 1.2 to 2.1, 50 seconds on and 10 seconds off, and it stops when two gains in a row are under 3%.

The steps are in [PLAN.md](PLAN.md). The pastes are [GO-BUILD](../go/GO-BUILD.md), [GO-MINI](../go/GO-MINI.md) and [GO-BOT](../go/GO-BOT.md). The box takes one NTP sample. It does not send and it does not count.

If plan 2 is declined, use these sheets and ignore [after/](../after/README.md).

## Plan 2

Plan 1, unchanged, through 21:00 UTC. Then one 32-family load. The write-up, the reason, and the target are in [after/](../after/README.md).

| | UTC | Desk local (CET, UTC+1) |
|---|---|---|
| Target start | **21:15** | **22:15** |
| Target end | **22:00** | **23:00** |

45 minutes. 32 families from the first second. The same 1.2 offer. One sender. The mini counts what lands. The start slips later the same Saturday if the 21:10 census still shows Saturday hops. It does not start before 21:15 UTC and it does not start after 23:00 UTC.

The pastes are [after/GO-BUILD.md](../after/GO-BUILD.md) and [after/GO-MINI.md](../after/GO-MINI.md). There is no box paste for this load. [GO-BOT](../go/GO-BOT.md) stays the Saturday NTP sample and nothing more.

## What stays put either way

The 19:00 UTC start. The 1.2 rate. The 1.14 pass line. The landing score that does not gate the 8-family step. The abort line of 2,500 coins and 18,000 usable tKAS. One sender. Miners off.

The later 16-family question in [additional testing](https://github.com/STP-KAS/tn10-storm/blob/main/additional-testing/PLAN.md) stays off this night.
