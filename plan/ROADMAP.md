> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only.

# Two ways to spend Saturday

The outside counter took the second way. Saturday runs as already planned. The 32-family load is added after that count closes. The load is not a different Saturday, and it does not replace the window.

Pasting a sheet before its own clock does not start a sender and does not start a counter.

## Plan 1

The count plan is [COUNT.md](COUNT.md). It is in force for the desk and the mini.

| | UTC | Desk local (CET, UTC+1) |
|---|---|---|
| Checks | Sat 7 Nov 2026, **18:40** | **19:40** |
| Genesis | **18:55** | **19:55** |
| Counter on | **18:58** | **19:58** |
| START | **19:00** | **20:00** |
| Sends finished | **20:30** | **21:30** |
| Counter off | **21:00** | **22:00** |

One sender, the desk, on from the first second of each step. 1 family, then 2, then 4, then 8 if 4 is clean. One rate, **1.2** accepted hop/s per family. Pass line **1.14**, read as in [COUNT.md](COUNT.md). Landing is written down. It does not open or close the 8-family step. The ramp is 10 minutes, steps of 0.1 from 1.2 to 2.1, 50 seconds on and 10 seconds off, and it stops when two gains in a row are under 3%.

The steps are in [PLAN.md](PLAN.md). The pastes are [GO-BUILD](../go/GO-BUILD.md), [GO-MINI](../go/GO-MINI.md) and [GO-BOT](../go/GO-BOT.md). The box takes one NTP sample. It does not send and it does not count.

If the load is declined, use these sheets and ignore [after/](../after/README.md). Saturday is unchanged either way.

## Plan 2

Plan 1, unchanged, through 21:00 UTC. Then one 32-family load. The write-up, the reason, and the target are in [after/](../after/README.md).

| | UTC | Desk local (CET, UTC+1) |
|---|---|---|
| Target start | **21:15** | **22:15** |
| Target end | **22:00** | **23:00** |

45 minutes. 32 families from the first second. The same 1.2 offer. One sender. The mini counts what lands. 21:15 UTC is after the Saturday counter turns off at 21:00. The two counts are two files. Accepted hops are already in blocks by then. The mempool of ours has been empty at the end of every recent window. We look once. We do not hold the start for that look. The start is not before 21:15 UTC and not after 23:00 UTC.

The pastes are [after/GO-BUILD.md](../after/GO-BUILD.md) and [after/GO-MINI.md](../after/GO-MINI.md). There is no box paste for this load. [GO-BOT](../go/GO-BOT.md) stays the Saturday NTP sample and nothing more.

## What stays put either way

The 19:00 UTC start. The 1.2 rate. The 1.14 pass line. The landing score that does not gate the 8-family step. The abort line of 2,500 coins and 18,000 usable tKAS. One sender. Miners off.

The later 16-family question in [additional testing](https://github.com/STP-KAS/tn10-storm/blob/main/additional-testing/PLAN.md) stays off this night.
