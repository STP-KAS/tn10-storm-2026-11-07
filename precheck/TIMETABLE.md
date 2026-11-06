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

Leave the counter on through both rounds. Round 2 starts only if round 1 is clean. If a round is not clean, it is fixed and run again. Round 3 does not start until round 2 has succeeded. This page is updated before the new clock, and the mini does not need a new paste while its counter is still on.

The mini counter stays up until **Sat 7 Nov 2026, 08:00 UTC (09:00 CET)**. That covers a rerun and, if both rounds succeed, the load test. It is not the Saturday count. Saturday still starts its own counter at 18:58 UTC.

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

## Round 3, only if both rounds are clean

Another test, initiated by STP. Not Saturday. Not a change to the 1.2 plan.

It starts with the same covenant shape as rounds 1 and 2, at 1.2, so the standard is back on the tape. Then the family count steps up. The offered rate stays 1.2. The climb stops when acceptance per family stops growing. The clock for that round is written here only after rounds 1 and 2 are clean, and the mini gets a second paste before it starts.

What this round is watching: accepted hops per family, whether the node stays synced, peer count, and how many of our transactions are still in each mempool after the sends. Desk and mini each write their own note.

## What this will not aim at

The [kaspa master file](https://github.com/STP-KAS/kaspa-master-file) reread on 6 Nov, and [tn-master FINDINGS](https://github.com/STP-KAS/tn-master/blob/main/FINDINGS.md), put a full block at about 304 to 308 ordinary payments. At 10 blocks per second that is about **3,000 payments per second**. Submitting faster only fills mempools.

That figure is ordinary payments. A covenant hop is not that payment. The 32-family covenant load on 5 Nov accepted about 34 hops per second in total, near 1.04 to 1.10 per family. Offering more did not raise acceptance. It added rejects.

This check will not point the covenant sender at 3,000 transactions per second. That would fill mempools and would not become 3,000 accepted covenant hops. Round 3 climbs until acceptance stops growing, and stops there.

The same 6 Nov reread still shows rusty-kaspa [#1147](https://github.com/kaspanet/rusty-kaspa/pull/1147) open: a node can keep already-accepted transactions in its mempool after IBD. The nodes are not restarted for this check. Mempool counts are logged. A stuck transaction with no live funding input is recorded and is not chased with a new tool.

vProgs issue [#177](https://github.com/kaspanet/vprogs/issues/177), opened 5 Nov, is a crash between a batch's state-diff flush and its commit. Pruning can then delete a live row. That is not a covenant hop, and it is not tested by this sender. After round 2 succeeds, the load round logs mempool retention on the TN10 nodes, which is the open rusty-kaspa [#1147](https://github.com/kaspanet/rusty-kaspa/pull/1147) question. The #177 sequence is run separately, on a scratch store, not on the TN10 node and not while a round is sending.
