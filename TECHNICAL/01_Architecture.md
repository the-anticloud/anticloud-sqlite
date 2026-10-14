# Technical Architecture — SQLITE

**Upstream:** [https://github.com/capacitor-community/sqlite](https://github.com/capacitor-community/sqlite)
**License:** MIT
**Category:** MOBILE
**Anticloud Integration:** PAX L5 Narrow L2 General 27B + AIOSS + Offline-First

## Upstream Description

SQLite plugin for mobile apps

## Anticloud Architectural Changes

1. PAX L5 Narrow L2 General 27B on-device inference — no API calls, no server
2. AIOSS tamper-evident app update and configuration chain
3. AES-256 device-level encryption for all user data
4. Single-binary APK/IPA with all ML models bundled
5. Zero-cloud: all AI features work in airplane mode
6. GPU/CPU equalizer: uses Android NNAPI/CoreML GPU delegation automatically
7. Zero-telemetry: no passive analytics or crash reporting to third parties
8. Open local API: other apps can call PAX inference via local socket

## Integration Points

- **PAX Inference Socket:** Local HTTP endpoint at `127.0.0.1:11434/v1/chat` — same OpenAI-compatible API, zero cloud
- **AIOSS Hook:** Every write operation calls `aioss_append(event, payload)` before commit
- **Encryption Layer:** All file I/O routed through `anticloud_crypto.encrypt_at_rest()`
- **Single Binary Build:** `pyinstaller anticloud_sqlite.spec` or `go build -o sqlite`

## Deployment Modes

| Mode | Hardware | Notes |
| --- | --- | --- |
| Edge CPU | Raspberry Pi 4 / Intel NUC | Full feature set, PAX on CPU |
| Desktop GPU | RTX 3060 / A10 | PAX GPU inference, <1s latency |
| Server | 2× A100 | Full batch throughput |
| Air-gapped | Any x86/ARM | Zero network dependency |