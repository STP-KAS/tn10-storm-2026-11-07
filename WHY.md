> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only. No txid, key, seed, IP, host, port, covenant id or wallet address.

# Why

The steps are in [plan/PLAN.md](plan/PLAN.md). The count is in [plan/COUNT.md](plan/COUNT.md). This page is why those steps exist, and which parts are not a new question.

We do not claim this is the truth about mainnet. tKAS has no value. The numbers are what TN10 did in the windows already run.

## Where this sits

The storms before 29 Oct pushed ordinary transactions and asked how many the network accepted per second. That record is [tn-master](https://github.com/STP-KAS/tn-master/blob/main/WHAT-WHY-HOW.md). This repo is not that test.

A covenant hop is a different transaction. On 29 Oct, one family, then two, then four, the totals were 0.81, 1.96 and 3.24 hops/s. A single family stayed under 1 hop/s. The review of that night asked for the next shape: one sender, on from the first second, a higher offered rate, and eight families. That review is [REVIEW.md](https://github.com/STP-KAS/tn10-storm-2026-10-29/blob/main/logs/storm-2026-10-29/REVIEW.md).

## What is worth measuring tonight

The Saturday window is that next shape, on one clock, with the mini counting. The offer is 1.2 accepted hops/s per family. The steps are 15 minutes at 1 family, then 2, then 4, then 8 if 4 held the line.

The 5 Nov holds and the two Friday passes of this same shape already cleared the 1.14 line at eight families. The slowest family in those eight-family steps was about 1.26 hops/s. So tonight is not a search for a new eight-family number. It is the counted window: longer steps than the holds, the families in one sequence, and the quiet half hour after the sends stop. If it lands in the same band, that is the result.

Another pass of the same eight-family shape, after the ones already published, would not teach a new number. We are not adding one.

The ramp offers 1.2 and steps up by 0.1 toward 2.1. Every ramp so far has gone flat near 1.3 and stopped. The useful part is that flat stretch, with the hop counts written behind each gain. The 2.1 figure is the top of the list. It is not a rate this network has taken.

## The 32-family load

Two loads of 32 families are already published.

| When | Total | Slowest family | Worst full minute |
|---|---:|---:|---:|
| [5 Nov](one-time/REPORT.md) | 33.86/s | 1.037/s | 0.833/s |
| [Night of 6 Nov](load-32/REPORT.md) | 34.55/s | 1.047/s | 0.933/s |

The offer was 1.2 on both nights. Every full minute of both windows had a slowest family under 1.14. The rejects were already spent and orphan: two families reaching for the same coin. The fee was not raised. Building the hop was not what set the rate.

A third run of that same shape will not discover a new ceiling if the network is the same. We run it once more, after the Saturday count closes, so the quiet 1-to-8 case and the busy 32-family case are in one evening and can be read together. If it matches the two reports, the confirmation is the result. If it leaves that band, the difference is the result.

## What this does not test

- Ordinary-payment throughput. The September and October storms did that. Covenant hops at 32 families have sat near 34 per second. Reading that number as a payment-storm result would be the wrong comparison.
- Whether a higher fee buys inclusion. These loads did not raise the fee. A submit rejected for the fee itself stops the run.
- A 16-family ladder. That question is written down as [additional testing](https://github.com/STP-KAS/tn10-storm/blob/main/additional-testing/PLAN.md). It is not tonight.
- Anything the box sends. The box takes one time sample. It does not send and it does not count.
