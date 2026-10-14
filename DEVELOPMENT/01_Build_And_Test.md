# Build and Test

**Project:** `SQLITE`
**Upstream:** https://github.com/capacitor-community/sqlite
**License:** MIT

## Quick Start

```bash
git clone https://github.com/capacitor-community/sqlite
cd sqlite
pip install -r requirements-anticloud.txt
python anticloud_main.py --offline --pax-local
```

## Anticloud Improvements Applied

1. PAX L5 Narrow L2 General 27B on-device inference — no API calls, no server
2. AIOSS tamper-evident app update and configuration chain
3. AES-256 device-level encryption for all user data
4. Single-binary APK/IPA with all ML models bundled
5. Zero-cloud: all AI features work in airplane mode
6. GPU/CPU equalizer: uses Android NNAPI/CoreML GPU delegation automatically
7. Zero-telemetry: no passive analytics or crash reporting to third parties
8. Open local API: other apps can call PAX inference via local socket

## Benchmark Targets

| Metric | Target |
| --- | --- |
| Latency | Primary inference task: <5s on CPU, <1s on GPU |
| Throughput | Batch processing: >100 items/hour on single CPU server |
| Memory | <8GB RAM for standard deployment |
| Accuracy | Task-specific accuracy within 5% of cloud-API baseline |

## Build Status

Not yet measured. Run verified build and record actual figures above.
