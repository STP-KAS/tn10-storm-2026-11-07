> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only.
>
> Paste this whole file into the mini. It is the count after Saturday. Reading it does not start the counter. The Saturday count is [go/GO-MINI.md](../go/GO-MINI.md). That counter goes off at 21:00 UTC. This one starts after that.

# GO-MINI · mini · after Saturday, 7 Nov 2026

You are the mini. You count on your own node. You do not send. You do not run genesis. You do not mine. You do not open a wallet. You do not hold a key for this load.

The storm record is [tn10-storm-2026-11-07](https://github.com/STP-KAS/tn10-storm-2026-11-07). This load is [after/](README.md). Saturday is [plan/PLAN.md](../plan/PLAN.md). You count Saturday on the Saturday sheet. You count this load on this sheet. You do not mix the files.

The desk is the only sender. One relay, boson. The rate the desk will hold is **1.2 accepted hop/s per family**, 32 families, for 45 minutes. You do not set the rate and you do not raise it.

| | UTC | Desk local (CET, UTC+1) |
|---|---|---|
| Saturday counter off | Sat 7 Nov 2026, **21:00** | **22:00** |
| Counter on, target | **21:13** | **22:13** |
| START, target | **21:15** | **22:15** |
| End, target | **22:00** | **23:00** |
| Counter off, target | **22:05** | **23:05** |

21:15 UTC is the target start. If the operator names a later start the same Saturday, the send is still 45 minutes. Your counter goes on 2 minutes before that start and off 5 minutes after the end. The start you follow is at or after 21:15 UTC and at or before 23:00 UTC.

## When you start

Do not start because this file was pasted.

Start only on Saturday 7 Nov 2026, and only after all of the following.

- The Saturday counter is already off. You do not keep one file across both windows.
- The operator has said genesis for this load is in.
- The start is at or after 21:15 UTC and at or before 23:00 UTC.

Use the counter in the storm repo, `tools/storm/counter.cjs`, against the mini's own node. Write accepted ids on this machine only. Do not commit that file. Do not paste ids into chat.

If the operator has not confirmed genesis by the target, do not start. Ask.

## The window

One step. You count from 2 minutes before the start until 5 minutes after the end, so the edges are in the file.

| Step | Families | Rate | Length |
|---|---:|---:|---|
| f32 | 32 | 1.2 | 45 minutes |

You count what lands on chain. You do not count attempts. A reject is not a hop of yours to invent.

On 32 families the two earlier loads accepted about 34 hops/s in total, near 1.05–1.15 per family, under the offered 1.2. A minute under 1.2 is a result. You do not stop counting because a minute comes in low. You do not tell the desk to push the rate up.

## Before the start

A fail here is reported to the operator. You do not send a transaction to fix it.

- Your node is synced, on TN10.
- Peers at least 8.
- Clock within 80 ms of NTP. Log the offset. The log carries the milliseconds and the UTC time, and nothing else.
- Miners off. One line: `MINERS mini n=0`. A miner found running is reported. You do not leave it running and you do not start one.
- You do not need family ids. You record every accepted transaction in the window.

## During the window

- Do not submit a transaction.
- Do not restart your node.
- Do not open a wallet.
- If the node falls out of sync, or peers drop under 8, write the UTC time and keep counting if the node is still up.

## After the counter is off

- Keep the accepted-id file until the desk has copied the recount.
- Leave the node up until 10 minutes after the end. The desk takes a mempool census then.
- Do not publish a percentile. The desk publishes p50, p95 and p99 of submit time to the accepting header. Your file is the acceptance side of that join.

## What you refuse

- Starting on any day except Saturday 7 Nov 2026.
- Starting before 21:13 UTC that day, or for a send that starts after 23:00 UTC.
- Staying on past 5 minutes after the end, unless the operator says the window was extended.
- One accepted-id file that also holds the Saturday window.
- Any send, any genesis, any miner, any key.
- A second sender, including the box.
- A higher rate than 1.2.
- Pasting ids, keys, addresses, hosts or ports back into chat.
- Treating [go/GO-MINI.md](../go/GO-MINI.md) as this load, or treating this file as Saturday.
