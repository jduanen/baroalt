# baroalt
Barometric Altimeter that Logs Altitude and Displays Sample Statistics

**WIP**

# Notes

* High Accuracy Ambient Pressure Sensors
  - Omron 2SMBP-02B
    * discontinued
    * pre-2022 3M air filter sensors
    * 24b barometric pressure and ?b temperature
    * Interface: I2C or SPI
    * Supply Voltage: 1.8V (typ), 3.6V (max)
      - has separate "interface voltage"?
    * Range: 30-110KPa
    * Precision: ±4Pa (±?mm)
    * Resolution: 0.06Pa
    * Sample Time: 5.5-33.7ms
      - sample longer for greater accuracy, selectable filtering
  - Infineon DPS310
    * available from Adafruit (as QWIC module) and SeeedStudio (as a Grove module)
      - Adafruit has CircuitPython and Arduino drivers
      - ESPHome driver exists
    * Supply Voltage: 3.3V or 5V @ 1.7uA (1KHz high-precision sampling), 0.5uA (standby)
      - Vdd: 1.7-3.6V
      - Vddio: 1.2-3.6V
    * Interface: I2C or SPI
    * Range: 300-1200hPa
    * Precision: delta (high precision) = ±0.002hPa (±2cm), absolute = ±1hPa (±1m)
    * Temperature Accuracy: ±0.5°C
    * Sample Time: 27.6ms (std mode 16x), 3.6ms (low precision)
    * 32x sample FIFO for pressure or temperature samples
