# Students — SQLITE

**Project:** SQLITE  
**Category:** MOBILE  
**Upstream:** see BENCH.json  
**Pinned commit:** `dbbe931904f2ee06546448fbe7cf7780f61bc110`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `0b912f7bac7e80660d3c69eb577213313853fcf8458905c7b0be15e9bb4ead4c`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `dbbe931904f2ee06546448fbe7cf7780f61bc110`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `0b912f7bac7e80660d3c69eb577213313853fcf8458905c7b0be15e9bb4ead4c`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
