# UniXNU-MT6768-common

Shared MediaTek MT6768 / MT6769Z (Helio G85) SoC configuration, device tree includes, and XNU kernel patches for UniXNU.

## Current Status

- **iPadOS 17.7.11 (`21H461`)**: Confirmed working on hardware (8-core SMP + Mali-G52 + NativeEmmc), **not yet fully stress-tested**.
- **iOS 16.7.16 (`20H392`)**: Confirmed working on hardware (8-core SMP `smp=1 cpus=8`, EL2-to-EL1 drop with `SPAN=1`, TTEP flush, workqueue parallelism, zero kernel panics).

## Configuration Layering (`CONFIG_XNU_DW_MT6768_*`)

- [`configs/mt6768.config`](configs/mt6768.config): SoC baseline fragment loaded first by board `board.toml`.
- [`configs/example.config`](configs/example.config): Blank reference template documenting all `CONFIG_XNU_DW_MT6768_*` parameters (`SMP`, `CPUS`, `EL2_DROP`, `FLUSH_TTEP`, `WORKQUEUE_PARALLEL`).
- Board general configs (`configs/merlinx_defconfig`) and OS override configs (`configs/merlinx-iOS16.7.config`) layer on top and take final precedence.

## SoC Patch Series (`patches/xnu/series`)

- `mt6768-emmc-personality.patch`
- `mt6768-mali-personality.patch`
- `mt6768-workqueue-parallelism.patch`
- `mt6768-smp-flush-ttep.patch`
- `mt6768-smp-el2-drop.patch`
