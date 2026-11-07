> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only. No txid, key, seed, IP, host, port, covenant id or wallet address.

# After the Saturday count

This is a proposal. It runs only if Pulse wants the count. It is not the Saturday storm.

Saturday stays **7 Nov 2026, 19:00–21:00 UTC (20:00–22:00 CET)**. The Saturday sender starts at 19:00 UTC and not before. Those steps, that rate, and the sheets in [go/](../go/README.md) stay as they are. This folder starts after that counter is off.

Initiated by this desk (STP), for review by Pulse, the same way as the [5 Nov load](../one-time/REPORT.md). The choice between the two plans is in [plan/ROADMAP.md](../plan/ROADMAP.md).

## Why

Two 32-family loads already settled in the same place. Label **A** for both.

| | [5 Nov](../one-time/REPORT.md) | [Night of 6 Nov](../load-32/REPORT.md) |
|---|---|---|
| Hops | 91,424 | 93,289 |
| All families | 33.86/s | 34.55/s |
| Slowest family | 1.037/s | 1.047/s |
| Worst full minute | 0.833/s | 0.933/s |
| Outside count | matched every hop | matched every hop |

Offered rate both nights was 1.2 per family. Acceptance stayed near 1.05–1.15 per family. The attempts above that came back already spent or orphan. The fee was left where it was. On the second night the builder sat at p50 13 ms and p95 69 ms. Submit time to the accepting header sat at p50 708 ms, p95 1,274 ms, p99 1,564 ms. The builder was not the ceiling. The ceiling was how many hops the network accepted per family.

Saturday, at 8 families and 1.2, is a different question and it already has its own sheet. This load asks whether a third 45-minute window, with Pulse's counter on it, lands on the same ceiling. People working on the node can read the reject classes, the header percentiles, and the per-family floor next to the two nights already published. That is the use of running it once more.

## How

Same shape as those two loads.

- One desk sender. 32 families from the first second. The 1-then-2-then-4 ladder and the ramp stay inside Saturday. They are not repeated here.
- Offered rate **1.2** accepted hop/s per family, held for the whole 45 minutes.
- One relay, boson. Stagger 0. No phase offset. Heartbeat 900 ms. Miners off. The desk node stays up. It is not restarted.
- The fee stays where it is at the start. Already spent and orphan mean the families are contending. They are not a reason to raise the fee. If a submit is rejected for the fee itself, the desk stops and tells the operator.
- The mini counts what lands on chain. The desk keeps a private submit file, one row per included hop. After the window the public numbers are the accepted hops, the slowest family, the worst full minute, and p50, p95 and p99 of submit time to the accepting header.
- The abort line stays 2,500 coins and 18,000 usable tKAS. Recount it after Saturday and before this genesis. Do not lower it. If the lane is short, top up or do not start.
- Genesis is 32 families, about five minutes before the send, and only after the Saturday census is clear. That census is none of the Saturday hops left on the desk node and none left on the mini node.

## Target

A target, not a locked clock. The length is 45 minutes because that is the length that already produced a full minute-by-minute floor. The start moves later on Saturday if the census is not clear. It does not move earlier, and it does not take a minute out of the 19:00–21:00 count.

| | UTC | Desk local (CET, UTC+1) |
|---|---|---|
| Saturday counter off | 21:00 | 22:00 |
| Saturday census | 21:10 | 22:10 |
| Genesis, if that census is clear | **21:10** | **22:10** |
| Mini counter on | **21:13** | **22:13** |
| Target start | **21:15** | **22:15** |
| Target end | **22:00** | **23:00** |
| Counter off | **22:05** | **23:05** |
| Census of this load | **22:10** | **23:10** |

If 21:15 UTC is not clear, name a later start the same Saturday. The send is still 45 minutes. Shift genesis, the counter, and the census by the same amount. The start is at or after 21:15 UTC and at or before 23:00 UTC. A start at 23:00 UTC ends at 23:45 UTC. After 23:00 UTC this sheet does not start.

## What this leaves alone

- Saturday's 19:00 UTC start, the 1.2 rate, the 1.14 pass line, and the rule that landing is written down and does not open or close the 8-family step.
- The box. It does not send and it does not count this load. Its Saturday sheet is still one NTP sample at 18:40 UTC.
- Ordinary payments. A full block of ordinary payments is a different measurement. These sends are covenant hops. The two loads accepted about 34 hops/s in total. This sender is not aimed at the payment ceiling.
- The 16-family question in [additional testing](https://github.com/STP-KAS/tn10-storm/blob/main/additional-testing/PLAN.md). That question stays off this night. It is the open point between 8 families and 32, and it already has its own file. It is not a second ask for Saturday.

## Sheets

[GO-BUILD.md](GO-BUILD.md) is the desk paste. [GO-MINI.md](GO-MINI.md) is the mini paste. Pasting either one does not start the sender and does not start the counter. If this load is declined, ignore both files and use the sheets in [go/](../go/README.md).
