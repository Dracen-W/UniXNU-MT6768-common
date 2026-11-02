# UniXNU MT6768 support

Shared MediaTek MT6768/MT6769Z support for UniXNU: CPU topology, GICv3, the
architectural timer, the Mali-G52 node and the MTK power, clock and pwrap
resources used during GPU bring-up.

`soc.toml` selects `ArmCpu`, `ArmDTPlatform` and `MaliG52`. Device repositories
supply RAM, board peripherals, firmware, packaging and the final power policy.
The board DTS includes `dts/mt6768.dtsi` and keeps board-only nodes.

Hardware descriptions come from the vendor MT6768 device tree and the MT6768
Mali bring-up work. The shared tree contains only confirmed SoC resources.

Build through the [UniXNU CLI](https://unixnu.com/building). Read the
[device repository specification](https://unixnu.com/porting/device-repository),
[device-tree specification](https://unixnu.com/porting/device-tree),
[SoC support guide](https://unixnu.com/porting/soc-support) and
[component catalog](https://unixnu.com/reference/components).

## Contents

| Path | Contents |
| --- | --- |
| `soc.toml` | SoC profile and component selection |
| `configs/mt6768.config` | Shared kernel configuration fragment |
| `dts/mt6768.dtsi` | Shared CPU, GIC, timer, Mali, SPM, topckgen, mfgcfg and pwrap nodes |
| `patches/xnu/series` | Ordered SoC patches; currently empty |
| `kits/` | Shared platform helpers, when required |

The initial device is merlinx (Xiaomi Redmi Note 9).
