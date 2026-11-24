# Life Recorder V0.1.3

Firmware release for the Seeed Studio XIAO ESP32S3 Sense.

- Firmware image: `firmware.bin`
- PlatformIO environment: `seeed_xiao_esp32s3`
- Source revision: `c440cd2`
- Charging behavior: steady, very dim blue; LED data is sent once on
  connection and not updated again until disconnection. The hardware-test
  pattern remains active while the test runs; blue resumes afterward if USB
  remains connected.
- USB detection uses separate connect/disconnect thresholds and a 40 ms
  disconnect debounce.
- Rebuild with: `pio run -e seeed_xiao_esp32s3`
- SHA-256: `450C07633327B958C795E83EB7091810FF655F3E9421C03845E7E21D48543F96`

The binary is the PlatformIO application image. To flash the device, use
`pio run -e seeed_xiao_esp32s3 -t upload` from the project root.
