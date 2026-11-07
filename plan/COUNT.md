> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only. No txid, key, seed, IP, host, port, covenant id or wallet address.

# Count plan

This is the plan for the desk and the mini.

| Who | Saturday | Load, after 21:00 UTC |
|---|---|---|
| Desk | [go/GO-BUILD.md](../go/GO-BUILD.md) | [after/GO-BUILD.md](../after/GO-BUILD.md) |
| Mini | [go/GO-MINI.md](../go/GO-MINI.md) | [after/GO-MINI.md](../after/GO-MINI.md) |

The steps stay in [PLAN.md](PLAN.md). The load clock stays in [after/](../after/README.md).

We do not claim this is the truth. It is our opinion from the testing already run: the holds, the two Friday checks, and the 32-family load. In those runs a hop counted when its seen time was inside the step, and a low minute did not by itself fail a step that held across the whole step.

This page is in force. A later note in this repo can replace it. Until that note, the desk and the mini follow this page and those four sheets.

## Three lines in this plan

### 1. Which families count

The Saturday file counts the eight families whose hashes are in [hashes/SATURDAY.md](../hashes/SATURDAY.md) before 18:40 UTC. The load file counts the thirty-two whose hashes are in [hashes/LOAD.md](../hashes/LOAD.md) before 21:10 UTC. The thirty-two stay on 21:10. Their coin is chosen after Saturday genesis at 18:55.

### 2. The rate is the step itself

A hop counts in the step when its seen time is at or after the step opens and before the step closes. The count is divided by the length of the step.

For a 900 second step that length is 900. 1.14 is 0.95 times 1.2, and over 900 seconds that is **1,026** accepted hops per family. That product is exact. The gate waits 3 seconds after the close before it reads the file. That wait does not extend the 900 seconds.

For the 32-family load the length is 2,700 seconds. The rate is hops seen inside those 2,700 seconds, divided by 2,700. The counter then stays up 15 minutes. Hops in that tail are late landings. They are listed apart from the rate.

### 3. The line is the whole step

A full minute at 1.14 is 68.4 hops. The line is the whole step, 1,026 hops per family. The gate does not use a 69-hop minute line. A minute can come in low and the step can still pass.

## What is an accepted hop

An accepted hop is a hop that landed in a block. Genesis is not a hop. A conflicting spend, already spent or orphan, is not a hop. Those are listed apart.

## A valid minute

For the outside count, a minute is valid when both of their nodes read it in full, agree on every family, and the miner lines show no change. The desk logs one miner line at the check, miners off, and does not start a miner during the window.

An attempt every second is read from the desk sender log. Attempts are not on chain. The Sunday file gives the attempt seconds as counts. It does not give the ids.

The mini counts accepted hops. A minute the mini did not read in full is marked. The mini does not fill that gap.

## Landing

Landing is the share of seconds in the window that contain a hop, the same way as [HOLD.md](https://github.com/STP-KAS/tn10-storm/blob/main/desk-saturday/HOLD.md). The Sunday file also gives that share per family. Landing is written down. It does not open or close the 8-family step.

## Ramp

Each ramp slot is 50 seconds on and 10 seconds off. The rate for a slot is the hops seen inside those 50 seconds, divided by 4 families and by 50. The stop is still two gains in a row under 3%. One hop at about 1.3 per family is a small part of that 3%, so the Sunday file shows the hop counts behind every gain.

## When the files come out

| File | What | By |
|---|---|---|
| 1 | Saturday, 19:00–21:00 UTC | Sunday 8 Nov 2026, **12:00 CET** (11:00 UTC) |
| 2 | The 32-family load | Monday 9 Nov 2026, **18:00 UTC** (19:00 CET) |

Hashes and counts only. No ids.
