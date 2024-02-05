# Configure Lenovo ThinkPad P15s

## UEFI

- **Config**
  - **Power**
    - **Sleep State** = `Linux S3`
  - **USB**
    - **Always On USB** = `Off`

## Hardware Sensors Indicator

Enable and relabel the following sensors:

- **`GPU`** (originally `NVIDIA T500`): `nvidia` > `ThermalSensor0`**
- **`CPU`** (originally `Package id 0`): `libsensors` > `coretemp-isa-0000` > `0`
- **`Fan`** (originally `fan1`): `libsensors` > `thinkpad-isa-0000` > `0`

Display `CPU` by default.

## Setting the Right Amount of Swap Space

Following the [Ubuntu recommendations](https://help.ubuntu.com/community/SwapFaq#How_much_swap_do_I_need.3F), this system should have 20GB of swap.
It only has 2GB by default.

Due to a [deadlock bug](https://github.com/openzfs/zfs/issues/7734) in ZFS (which this machine uses) we should not use swap files.
Unfortunately, the also has no unallocated space, so changing the swap partition space is going to be hard... I'll figure this out later.
