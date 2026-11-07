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

**What.** One desk sender. Steps of 15 minutes at 1 family, then 2, then 4, then 8 if 4 held the line, with 5-minute gaps. Then a 10-minute ramp. The offer is 1.2 accepted hops/s per family. The line is 1.14. The desk sends. The mini counts. The box is not part of this window. Miners stay off.

**Why.** 29 Oct ran 1, then 2, then 4 families and asked for the next shape: one sender, on from the first second, and eight families. The holds and the Friday passes of that shape already cleared 1.14 at eight families, with the slowest family near 1.26 hops/s. Tonight is the counted window of that shape, not a search for a new eight-family number. The ramp has gone flat near 1.3 every time it has been run. The useful part is that flat stretch. The listed top of 2.1 is not a rate the network has taken.

The 32-family load after 21:00 UTC is the busy case in the same evening. Two loads of that shape are already published, both near 34 hops/s total and both under 1.14 for the slowest family. A third run confirms that band, or shows a difference. It is not a new question. The full why, including what this does not test, is [WHY.md](WHY.md).

**Already run, and not this window.** The [5 Nov load](one-time/REPORT.md), the [dress rehearsal](rehearsal/REPORT.md), the [Friday check](precheck/README.md), and the [second 32-family load](load-32/REPORT.md). [Additional testing](https://github.com/STP-KAS/tn10-storm/blob/main/additional-testing/PLAN.md) is a later 16-family question. None of these moves the clock above.

## Map

| Folder or file | What is in it |
|---|---|
| [DISCLAIMER.md](DISCLAIMER.md) | Experimental; certainty labels A / B / C |
| [plan/PLAN.md](plan/PLAN.md) | Saturday steps, both clocks |
| [plan/COUNT.md](plan/COUNT.md) | Count plan in force for the desk and the mini |
| [WHY.md](WHY.md) | Why this shape, what is already known, what tonight does not test |
| [plan/ROADMAP.md](plan/ROADMAP.md) | Saturday, then one 32-family load after 21:00 UTC |
| [go/README.md](go/README.md) | The single clock and the roles. These sheets are plan 1 |
| [go/GO-MAP.md](go/GO-MAP.md) | Who does what |
| [go/GO-BUILD.md](go/GO-BUILD.md) | Desk paste. The only sender. The whole sheet is in this file |
| [go/GO-MINI.md](go/GO-MINI.md) | Mini paste. Count only. The whole sheet is in this file |
| [go/GO-BOT.md](go/GO-BOT.md) | The box is not part of this window. No sample. No task |
| [go/GO-KNS.md](go/GO-KNS.md) | KNS is not part of this storm |
| [go/LOGGING.md](go/LOGGING.md) | What may be published after 21:00 UTC |
| [plan/METRICS.md](plan/METRICS.md) | Hop/s per family, and what the outside count sees |
| [tools/README.md](tools/README.md) | No sender in this repo. Counter lives in the rehearsal |
| [logs/](logs/README.md) | Results after 21:00 UTC. Empty until then |
| [one-time/](one-time/REPORT.md) | Not Saturday. One 32-family load on 5 Nov |
| [rehearsal/](rehearsal/REPORT.md) | Not Saturday. Dress rehearsal of this plan, evening of 5 Nov |
| [precheck/](precheck/README.md) | Fri 6 Nov check for Saturday. Two rounds |
| [load-32/](load-32/REPORT.md) | Not Saturday. Another 32-family load, night of 6 Nov |
| [after/](after/README.md) | The same Saturday window, then one 32-family load. Desk and mini pastes. No box paste |
| [hashes/](hashes/README.md) | Family-id hashes. GitHub only, not X. 8 before 18:40 UTC, 32 before 21:10 UTC |
| [docs/README.md](docs/README.md) | Where the 29 Oct definitions still apply |

## Results

Placeholder. After 21:00 UTC the minute sheet and the write-up land under [logs/](logs/README.md).

Counts only: no txid, key, seed, IP, host, port, covenant id or wallet address in this repo.

---

Si vis pacem, para bellum.
