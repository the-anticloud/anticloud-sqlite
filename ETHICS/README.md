# Ethics — SQLITE

**Project:** SQLITE  
**Category:** MOBILE  
**Upstream:** see BENCH.json  
**Pinned commit:** `dbbe931904f2ee06546448fbe7cf7780f61bc110`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `0b912f7bac7e80660d3c69eb577213313853fcf8458905c7b0be15e9bb4ead4c`  
**Date:** October 2026

## Position

SQLITE is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
