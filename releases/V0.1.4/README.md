# Life Recorder V0.1.4

Firmware release for the Seeed Studio XIAO ESP32S3 Sense.

- Firmware image: `firmware.bin`
- PlatformIO environment: `seeed_xiao_esp32s3`
- Source revision: `38c08c2`
- Charging animation: dim blue LEDs fill clockwise, one per second. After the
  ring is full, it clears and repeats. The fill starts one LED counterclockwise
  from the previous zero position. LED data is sent only when the pattern
  changes; the hardware-test pattern remains active while the test runs.
- USB detection uses separate connect/disconnect thresholds and a 40 ms
  disconnect debounce.
- Rebuild with: `pio run -e seeed_xiao_esp32s3`
- SHA-256: `D7AF3AC544291F10E241DADFAEE8B75C2B6561CDFF5A7C79721F1DA937F93270`

The binary is the PlatformIO application image. To flash the device, use
`pio run -e seeed_xiao_esp32s3 -t upload` from the project root.
