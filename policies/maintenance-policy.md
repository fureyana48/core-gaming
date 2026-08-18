# Core Gaming Maintenance Policy

## Normal maintenance

Allowed:
- Windows Update through normal Windows mechanisms.
- Normal filesystem operation.
- Game installation/removal.
- Game launcher updates.
- Game-specific configuration.
- Benchmarking.

## Restricted maintenance

Do not perform routinely:
- manual `Optimize-Volume -ReTrim`;
- repeated SSD retrim cycles;
- arbitrary registry optimization;
- arbitrary pagefile resizing;
- unnecessary GPU-driver replacement;
- speculative gaming-optimization scripts.

## SSD policy

TRIM enabled is sufficient for the Core Gaming baseline.

Manual retrim is an exceptional maintenance operation, not routine gaming maintenance.

## Change control

If a system-wide change is required:

1. Record the reason.
2. Record the configuration/command change.
3. Reboot if required.
4. Repeat validation.
5. Update documentation if the baseline changes.
6. Increment the release version if the baseline specification changes.
