> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value. Mainnet: **not tested (label B)**.
>
> **Part of [tn-master](https://github.com/STP-KAS/tn-master)**, the map of every TN10 storm. Named by the [11 Oct naming rule](https://github.com/STP-KAS/tn-master/blob/main/repos/INDEX.md): `tn10-storm-YYYY-MM-DD`.

# tn10-storm-2026-11-07 · Sat 7 Nov, 19:00–21:00 UTC (20:00–22:00 CET): covenant families, 1 → 2 → 4 → 8

**History of every storm: [MASTER.md](https://github.com/STP-KAS/tn-master/blob/main/history/MASTER.md)** (in tn-master).

**Previous storm of this shape:** [tn10-storm-2026-10-29](https://github.com/STP-KAS/tn10-storm-2026-10-29) · Thu 29 Oct, 19:00–20:00 UTC (20:00–21:00 CET).

The rehearsal that set the rate lives in [tn10-storm](https://github.com/STP-KAS/tn10-storm), folder [desk-saturday](https://github.com/STP-KAS/tn10-storm/tree/main/desk-saturday). This repo is the Saturday record. The sender starts at 19:00 UTC and not before.

## Start, end, gate

Times are UTC first. Desk local is CET (UTC+1). Brussels moved from CEST to CET on Sun 25 Oct 2026, so 7 Nov is CET.

| | UTC | Desk local (CET) |
|---|---|---|
| **Checks** | Sat 7 Nov 2026, 18:40 | 19:40 |
| **Genesis** | 18:55 | 19:55 |
| **Mini counter on** | 18:58 | 19:58 |
| **START (T0)** | **19:00** | **20:00** |
| **Sends finished** | 20:30 | 21:30 |
| **Counter off / END of the window** | **21:00** | **22:00** |

The sends are the steps in [plan/PLAN.md](plan/PLAN.md). They finish at 20:30 UTC. The count stays up until 21:00 UTC so the quiet half hour is on the mini.

## What and why

**What.** One desk sender, eight covenant families available, one rate. Steps are 15 minutes at 1 family, then 2, then 4, then 8 if 4 was clean, with 5-minute gaps. A 10-minute ramp follows, four families, offered rate up by 0.1/s from 1.2, and it stops when acceptance per family stops growing.

**Rate.** 1.2 accepted hop/s per family. The pass line is 1.14. Two 10-minute holds on 5 Nov held that rate. On 8 families the worst full minute was 1.167. Detail: [HOLD.md](https://github.com/STP-KAS/tn10-storm/blob/main/desk-saturday/HOLD.md) (label A for those windows). Saturday's steps are 15 minutes. That length is what this storm measures.

**Roles.** The desk sends. The mini counts and does not send. The box does not send. Miners stay off.

**Not this storm.** [Additional testing](https://github.com/STP-KAS/tn10-storm/blob/main/additional-testing/PLAN.md) is a later 16-family question. It is not in this window.

## Map

| Folder or file | What is in it |
|---|---|
| [DISCLAIMER.md](DISCLAIMER.md) | Experimental; certainty labels A / B / C |
| [plan/PLAN.md](plan/PLAN.md) | Saturday steps, both clocks |
| [go/README.md](go/README.md) | The single clock and the roles |
| [go/GO-MAP.md](go/GO-MAP.md) | Who does what |
| [go/GO-BUILD.md](go/GO-BUILD.md) | Desk: the only sender. [Paste sheet](https://github.com/STP-KAS/tn10-storm/blob/main/build-count/PROMPT.md) |
| [go/GO-MINI.md](go/GO-MINI.md) | Mini: count only. [Paste sheet](https://github.com/STP-KAS/tn10-storm/blob/main/mini-count/PROMPT.md) |
| [go/GO-BOT.md](go/GO-BOT.md) | Box: NTP sample only. [Paste sheet](https://github.com/STP-KAS/tn10-storm/blob/main/bot-count/PROMPT.md) |
| [go/GO-KNS.md](go/GO-KNS.md) | KNS is not part of this storm |
| [go/LOGGING.md](go/LOGGING.md) | What may be published after 21:00 UTC |
| [plan/METRICS.md](plan/METRICS.md) | Hop/s per family, and what the outside count sees |
| [tools/README.md](tools/README.md) | No sender in this repo. Counter lives in the rehearsal |
| [logs/](logs/README.md) | Results after 21:00 UTC. Empty until then |
| [docs/README.md](docs/README.md) | Where the 29 Oct definitions still apply |

## Results

Placeholder. After 21:00 UTC the minute sheet and the write-up land under [logs/](logs/README.md).

Counts only: no txid, key, seed, IP, host, port, covenant id or wallet address in this repo.

---

Si vis pacem, para bellum.
