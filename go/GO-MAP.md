> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only.

# Who does what

| Machine | Saturday |
|---|---|
| Desk | Sends. Genesis. The private submit file. The score afterwards |
| Mini | Counts from 18:58 to 21:00 UTC. Does not send |
| Box | NTP sample only. A bad sample is logged and does not abort |

| UTC | CET | What |
|---|---|---|
| 18:40 | 19:40 | Checks. A fail aborts |
| 18:55 | 19:55 | Genesis, 8 families |
| 18:58 | 19:58 | Mini counter on |
| 19:00 | 20:00 | f1 |
| 20:30 | 21:30 | Sends done, ramp included |
| 21:00 | 22:00 | Counter off |
| 21:10 | 22:10 | Node still up for the mempool census |

Full steps: [../plan/PLAN.md](../plan/PLAN.md).
