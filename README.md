# Core Gaming

**Version:** v1.0  
**Status:** RELEASED / BASELINE FROZEN  
**Scope:** Windows gaming environment across the retained ThinkPad fleet

## Purpose

Core Gaming defines the standardized Windows gaming baseline for the retained ThinkPad fleet. It establishes a reproducible operating-system configuration layer before game installation, benchmarking, and gameplay.

Core Gaming is a configuration baseline, not a game catalog.

## Fleet

| Host | Windows Gaming Target | GPU | Status |
|---|---|---|---|
| Lenovo ThinkPad T540p | Windows 10 Gaming | NVIDIA GeForce GT 730M + Intel HD Graphics 4600 | COMPLETE |
| Lenovo ThinkPad T540p | Windows 11 Gaming | NVIDIA GeForce GT 730M + Intel HD Graphics 4600 | COMPLETE |
| Lenovo ThinkPad W530 | Windows 10 Gaming | NVIDIA Quadro K1000M + Intel HD Graphics 4000 | COMPLETE |
| Lenovo ThinkPad W530 | Windows 11 Gaming | NVIDIA Quadro K1000M + Intel HD Graphics 4000 | COMPLETE |
| Lenovo ThinkPad A475 | Windows 10 Gaming | AMD Radeon R7 Graphics | COMPLETE |
| Lenovo ThinkPad A475 | Windows 11 Gaming | AMD Radeon R7 Graphics | COMPLETE |

## Baseline policy

- Game Mode: enabled.
- Game DVR/background capture: disabled.
- Ultimate Performance power plan: active.
- GPU devices: PnP status OK.
- Pagefile: retained according to the existing per-system configuration.
- NTFS TRIM: enabled at the Windows storage stack.
- Manual SSD TRIM/retrim is intentionally excluded from normal maintenance.
- Temporary files and Windows Update download cache are cleaned during baseline preparation.
- DISM component cleanup is performed during baseline preparation.
- No unnecessary registry, pagefile, storage, or driver tuning is performed after validation.

## Lifecycle

`BASELINE -> CLEANUP -> POLICY CONFIGURATION -> REBOOT -> VALIDATION -> FREEZE -> GAME INSTALLATION`

Once validation passes, Core Gaming is frozen. Future work normally occurs above this layer: game installation, configuration, benchmarking, and gameplay.

## Non-goals

- Game installation.
- Game-specific graphics tuning.
- Benchmark result collection.
- Hardware modification.
- SSD health remediation.
- Server configuration.
- Daily-use application configuration.

## Repository structure

```text
.
├── README.md
├── docs/
│   ├── architecture.md
│   ├── baseline.md
│   ├── lifecycle.md
│   └── validation.md
├── inventory/
│   └── windows-gaming-matrix.md
├── policies/
│   └── maintenance-policy.md
└── validation/
    └── validation-record.md
```
