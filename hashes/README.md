> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only. No txid, key, seed, IP, host, port, covenant id or wallet address.

# Family-id hashes

This folder is the only place the hashes are published. They are not posted on X.

A family id is fixed by the genesis coin and the launch path. It is not a value that exists on its own this morning. Saturday genesis at 18:55 UTC spends one coin on each of the first eight keys. The 32-family load uses the coins that remain after that. A hash written before the coin is chosen would not match the send, so this page does not contain the hashes yet.

The desk adds them here, as a sha256 of the lowercase hex id. The id itself stays off the repo. The commit time is the proof that the hash was fixed before the send.

| Window | Families | File | On this repo by |
|---|---:|---|---|
| Saturday | 8 | [SATURDAY.md](SATURDAY.md) | Sat 7 Nov 2026, **18:40 UTC** (19:40 CET) |
| The load after it | 32 | [LOAD.md](LOAD.md) | Sat 7 Nov 2026, **21:10 UTC** (22:10 CET) |

If a genesis coin moves before the send, the desk replaces that file before the deadline above. The send uses the coin named by the hash that is in the file at the deadline.

## What these numbers are for

The Saturday count and the load are two files. The first write-up stays on Sunday, as already agreed. The load write-up is the second file, on Monday 9 Nov 2026, by 18:00 UTC.

Put the accepted hops first. The 1-to-8 window is the quiet case. The 32-family window is the busy case: what each family still got, and what was rejected. The question those numbers feed is whether a builder who needs transactions to keep landing while the network is busy should watch for that load. This load does not raise the fee. It is not a fee result.
