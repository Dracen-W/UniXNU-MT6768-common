# Agent instructions

This repository owns shared MT6768 resources and platform operations. Keep board
memory, peripherals, firmware selection, partition layout, display policy and
power policy in the device repository. Preserve source filenames, classes,
symbols, bundle IDs and protocol IDs.

Read these UniXNU pages before editing:

1. [Porting](https://unixnu.com/porting/)
2. [Device repositories](https://unixnu.com/porting/device-repository)
3. [Components](https://unixnu.com/reference/components)
4. [Device trees](https://unixnu.com/porting/device-tree)
5. [SoC support](https://unixnu.com/porting/soc-support)
6. [Driver matching](https://unixnu.com/drivers/device-tree-matching)

Hardware values must be traceable to the vendor MT6768 sources or measured on
the device. Run builds from the UniXNU checkout and record build commands,
hardware checkpoints and local inputs. Keep the documentation site in UniXNU.
