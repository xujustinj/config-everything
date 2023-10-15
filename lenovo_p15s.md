# Configure Lenovo ThinkPad P15s

## Hardware Sensors Indicator

Enable and relabel the following sensors:

- **`GPU`** (originally `NVIDIA T500`): `nvidia` > `ThermalSensor0`**
- **`CPU`** (originally `Package id 0`): `libsensors` > `coretemp-isa-0000` > `0`
- **`Fan`** (originally `fan1`): `libsensors` > `thinkpad-isa-0000` > `0`

Display `CPU` by default.
