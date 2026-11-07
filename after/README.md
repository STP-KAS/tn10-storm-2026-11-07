> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only. No txid, key, seed, IP, host, port, covenant id or wallet address.

# After the Saturday count

This is the load added on top of Saturday, only if Pulse wants it added. It is not a different Saturday, and it does not replace the 19:00–21:00 window.

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

Saturday measures 1 family, then 2, then 4, then 8, at one held rate. The question there is whether 1.2 stays clean up to 8 families. The holds and the 6 Nov check say it does. At 8 families the slowest family was about 1.26/s.

32 families asks the next question. Does each added family still bring about 1.2 hops/s with it, or does the network settle on a total and give each family less?

Two nights of this shape say the second thing. At 8 families the total is about 10 hops/s. At 32 families the total was 33.86/s on 5 Nov and 34.55/s on 6 Nov. Four times the families, a bit more than three times the hops. The slowest family was 1.037/s, then 1.047/s. The offer was still 1.2. The network did not take the offer. Every full minute of both windows had a slowest family under the Saturday 1.14 line.

The rejects were already spent and orphan. Two families reach for the same coin. One lands. The other is dropped. That is not a fee miss. On the second night the builder was p50 13 ms and p95 69 ms. Submit time to the accepting header was p50 708 ms, p95 1,274 ms, p99 1,564 ms. Building the hop is not what sets the rate. How many of these hops a block will take, per family, does.

Our mini matched both loads, hop for hop. Pulse's nodes have not counted this shape yet. If his count lands on the same total and the same per-family floor, the limit is in the network, not in our join. If it does not, the difference is the result. Either reading is useful to someone working on the node. Saturday stays 8 families at 1.2 either way.

## How

Same shape as those two loads.

- One desk sender. 32 families from the first second. The 1-then-2-then-4 ladder and the ramp stay inside Saturday. They are not repeated here.
- Offered rate **1.2** accepted hop/s per family, held for the whole 45 minutes.
- One relay, boson. Stagger 0. No phase offset. Heartbeat 900 ms. Miners off. The desk node stays up. It is not restarted.
- The fee stays where it is at the start. Already spent and orphan mean the families are contending. They are not a reason to raise the fee. If a submit is rejected for the fee itself, the desk stops and tells the operator.
- The mini counts what lands on chain. The desk keeps a private submit file, one row per included hop. After the window the public numbers are the accepted hops, the slowest family, the worst full minute, and p50, p95 and p99 of submit time to the accepting header.
- The abort line stays 2,500 coins and 18,000 usable tKAS. Recount it after Saturday and before this genesis. Do not lower it. If the lane is short, top up or do not start.
- Genesis is 32 families, about five minutes before the send.

## Target

The length is 45 minutes because that is the length that already produced a full minute-by-minute floor. The start is 21:15 UTC because the Saturday counter turns off at 21:00 UTC. The load has its own file. It does not share a minute with the Saturday count.

Saturday's last send is 20:30 UTC. From 20:30 to 21:00 the counter stays on and the sender is quiet, so that half hour is in the Saturday file with none of our hops. An accepted hop on TN10 is in a block within a second or two. It does not wait in the mempool until 21:10. After the 5 Nov load, after both parts of the 6 Nov check, and after the second 32-family load, the mempool census was 0 of ours on the desk and 0 of ours on the mini. Empty is the expected state. We look once at 21:10 and write down what we see. We do not hold the 21:15 start for that look.

| | UTC | Desk local (CET, UTC+1) |
|---|---|---|
| Saturday counter off | 21:00 | 22:00 |
| Look at the mempool | 21:10 | 22:10 |
| Genesis | **21:10** | **22:10** |
| Mini counter on | **21:13** | **22:13** |
| Target start | **21:15** | **22:15** |
| Target end | **22:00** | **23:00** |
| Counter off | **22:15** | **23:15** |
| Look after this load | **22:15** | **23:15** |

The outside counter keeps counting through a 15-minute tail, to 22:15 UTC, for late landings. The desk's read of that node stays up for the same tail. The send still ends at 22:00 UTC.

The Saturday write-up stays on Sunday, as already agreed. The load write-up is a second file, on Monday 9 Nov 2026, by 18:00 UTC.

The start is not before 21:15 UTC. A later start the same Saturday is only if the Saturday window itself has not finished. The send is still 45 minutes. It does not start after 23:00 UTC.

## What this leaves alone

- Saturday's 19:00 UTC start, the 1.2 rate, the 1.14 pass line, and the rule that landing is written down and does not open or close the 8-family step.
- The box. It does not send and it does not count this load. Its Saturday sheet is still one NTP sample at 18:40 UTC.
- Ordinary payments. A full block of ordinary payments is a different measurement. These sends are covenant hops. The two loads accepted about 34 hops/s in total. This sender is not aimed at the payment ceiling.
- The 16-family question in [additional testing](https://github.com/STP-KAS/tn10-storm/blob/main/additional-testing/PLAN.md). That question stays off this night. It is the open point between 8 families and 32, and it already has its own file. It is not a second ask for Saturday.

## Sheets

[GO-BUILD.md](GO-BUILD.md) is the desk paste. [GO-MINI.md](GO-MINI.md) is the mini paste. Pasting either one does not start the sender and does not start the counter. If this load is declined, ignore both files and use the sheets in [go/](../go/README.md).
