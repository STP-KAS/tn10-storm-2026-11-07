> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only. No txid, key, seed, IP, host, port, covenant id or wallet address.

# How the count is read

This is the reading for tonight. The steps stay in [PLAN.md](PLAN.md). The load stays in [after/](../after/README.md).

## What is an accepted hop

An accepted hop is a hop that landed in a block. Genesis is not a hop. A conflicting spend, already spent or orphan, is not a hop. Those are listed apart.

The Saturday file counts the eight families whose hashes are in [hashes/SATURDAY.md](../hashes/SATURDAY.md) before 18:40 UTC. The load file counts the thirty-two whose hashes are in [hashes/LOAD.md](../hashes/LOAD.md) before 21:10 UTC. The thirty-two are not pulled forward to 18:40. Their coin is chosen after Saturday genesis at 18:55.

## A valid minute

For the outside count, a minute is valid when both of their nodes read it in full, agree on every family, and the miner lines show no change. The desk logs one miner line at the check, miners off, and does not start a miner during the window.

An attempt every second is read from the desk sender log. Attempts are not on chain. The Sunday file gives the attempt seconds as counts. It does not give the ids.

## The 1.14 line

1.14 is 0.95 times 1.2. Over a 900 second step that is **1,026** accepted hops per family. That product is exact.

It is not a 10 second tail. A hop counts in the step when its seen time is at or after the step opens and before the step closes. The count is divided by 900. A hop seen after the close is not in the rate. The gate waits 3 seconds after the close before it reads the file. That wait does not extend the 900 seconds.

A full minute at 1.14 is 68.4 hops. The gate does not round that to 69, and it does not require every minute to clear 69. The line is the whole step.

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
