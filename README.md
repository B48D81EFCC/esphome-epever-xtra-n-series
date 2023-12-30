# EPEVER XTRA N Series MPPT Solar Charger ESPHome project
Read measurement values from the MPPT Solar Charger and write configuration values to the Solar Charger via RS485 (Modbus) using ESPHome.

# Limitations
At the moment only read operations are supported. No write operations are supported yet.

# Supported modbus register
| Number    | Name | Description |
| --------- | ---- | ----------- |
| A1        | Over Temperature Device | True or False. According to the manual, the controller will stop operation if 85°C is exceeded |
| A3        | PV Input Voltage | PV array voltage |
| A4        | PV Input Current | PV array current |
| A5 / A6   | PV Input Power | PV array power |
| A11       | Battery Temperature | Measurement of the battery sensor (if connected). Otherwise 25°C |
| A12       | Device Temperature | Temperature insinde of controller |
| A13       | Battery Remaining Capacity | Remaining capacity in % |
| A14       | Battery Rated System Voltage | Battery system rated voltage |
| A28 / A29 | PV Generated Energy Day | Generated PV energy, reset at 00:00, using internal clock |
| A30 / A31 | PV Generated Energy Month | Generated PV energy, reset first day of the month at 00:00, using internal clock |
| A32 / A33 | PV Generated Energy Year | Generated PV energy, reset first of January at 00:00, using internal clock |
| A34 / A34 | PV Generated Energy Total | Total generated PV energy |
| A36       | Battery Voltage | Current measured battery voltage |
| A37 / A38 | Battery Current | Current measured battery current |
| B6        | Temperature Compensation Coefficient | Configured compensation factor |
| B7        | Over Voltage Disconnect Voltage |  |
| B8        | Charging Limit Voltage |  |
| B9        | Over Voltage Reconnect Voltage |  |
| B11       | Boost Charging Voltage |  |
| B12       | Float Charging Voltage |  |
| B13       | Boost Reconnect Charging Voltage |  |
| B14       | Low voltage Reconnect Voltage |  |
| B15       | Under Voltage Warning Recover Voltage |  |
| B16       | Under Voltage Warning Voltage |  |
| B17       | Low Voltage Disconnect Voltage |  |
| B18       | Discharging Limit Voltage |  |

# Supported devices
This project is based on version 2.6 of the "XTRA, TRIRON, TracerAN Series Controller Communication Instruction" document.
You can request the Modbus communication documentation via the official Support (support@epever.com).

Tested with a XTRA 4415N device.
