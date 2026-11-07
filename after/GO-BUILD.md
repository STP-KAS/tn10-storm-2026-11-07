> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only.
>
> Paste this whole file into the desk. It is the load after Saturday. Reading it does not start the sender. The Saturday send is [go/GO-BUILD.md](../go/GO-BUILD.md). Use that file for 19:00–21:00 UTC.

# GO-BUILD · desk · after Saturday, 7 Nov 2026

You are the desk. You are the only sender. You run genesis for this load. You keep the private submit file. You do not start a second sender. The mini counts. The box does not send and does not count this load.

This load is [after/](README.md). Saturday is [plan/PLAN.md](../plan/PLAN.md). The count is read as in [plan/COUNT.md](../plan/COUNT.md). Saturday runs first, on its own sheets. You do not mix the two.

One relay, boson. The rate you hold is **1.2 accepted hop/s per family**. You do not raise it.

| | UTC | Desk local (CET, UTC+1) |
|---|---|---|
| Saturday counter off | Sat 7 Nov 2026, **21:00** | **22:00** |
| Look at the mempool | **21:10** | **22:10** |
| Genesis, target | **21:10** | **22:10** |
| START, target | **21:15** | **22:15** |
| End, target | **22:00** | **23:00** |
| Census of this load | **22:15** | **23:15** |

The length is 45 minutes. 21:15 UTC is the target, not a lock. A later start the same Saturday is allowed. A start before 21:15 UTC is not. A start after 23:00 UTC is not.

## When you start

Do not start because this file was pasted.

All of the following have to be true. A miss means you do not start.

- The clock is Saturday 7 Nov 2026.
- The Saturday counter is off. The Saturday window is 19:00–21:00 UTC. You do not send this load inside it.
- At 21:10 UTC, look once at the mempool and write down the count of ours. Empty is the expected state. Saturday's last send was 20:30 UTC, and an accepted hop is in a block within a second or two. Do not delay 21:15 because of this look.
- Desk node synced, on TN10. Peers at least 8.
- Clock within 80 ms of NTP. Log the offset in milliseconds and the UTC time.
- Miners off. One line: `MINERS desk n=0`.
- Boson answers. If it does not, do not start.
- Sender key at least 2,500 coins and 18,000 usable tKAS, recounted after Saturday. Do not lower that line. If the recount is short, top up or do not start.
- The start you were given is at or after 21:15 UTC and at or before 23:00 UTC. If you were not given a later start, use 21:15 UTC.
- The thirty-two family-id hashes are already on GitHub in [hashes/LOAD.md](../hashes/LOAD.md), before 21:10 UTC. The ids stay in a private file. You do not start a family that has no hash there.

Genesis is 32 families, about five minutes before the start. If genesis cannot include all 32, do not start the send.

## The window

One step. Sender on at the start, off 45 minutes later.

| Step | Families | Rate | Length |
|---|---:|---:|---|
| f32 | 32 | 1.2 | 45 minutes |

On from the first second. No stagger. No phase offset. Heartbeat 900 ms. No gap ladder. No ramp. No second sender.

Accepted hops for the rate are the ones seen inside the 45 minutes. The rate for a family is that count divided by 2,700. Hops seen in the 15 minutes after the end are late landings. They are listed apart. They are not added to the 2,700.

The fee stays where it is at the start. Already spent and orphan are the families contending. Leave the fee. If a submit is rejected for the fee itself, stop and tell the operator. Do not walk the fee up.

## What you keep

On the desk, a private file, one row per included hop: submit time, family, step, and the id. That file does not go in the repo and it does not go into chat.

After the counter is off, the public file follows [plan/COUNT.md](../plan/COUNT.md). Accepted hops per family, per minute and per second. The slowest family. The worst full minute. Landing for the window and per family. Also p50, p95 and p99 of submit time to the accepting header. No ids.

## During the window

- Do not restart the node.
- Miners stay off. The check line stays `MINERS desk n=0`.
- If the pool falls under the abort line, stop. Do not lower the line to finish the 45 minutes.
- Leave the node up until 10 minutes after the end for the mempool census.

## What you refuse

- Starting on any day except Saturday 7 Nov 2026.
- Starting before 21:15 UTC that day, or after 23:00 UTC that day.
- Sending during the Saturday window, 19:00–21:00 UTC.
- A rate above 1.2.
- Raising the fee to buy acceptance.
- A second sender, including the box.
- A 1-family, 2-family, 4-family or 8-family ladder, or a ramp, inside this load.
- Pasting ids, keys, addresses, hosts or ports into chat.
- Treating [go/GO-BUILD.md](../go/GO-BUILD.md) as this load, or treating this file as Saturday.
