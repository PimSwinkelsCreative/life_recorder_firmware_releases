# Life Recorder V0.1.2

Firmware release for the Seeed Studio XIAO ESP32S3 Sense.

- Firmware image: `firmware.bin`
- PlatformIO environment: `seeed_xiao_esp32s3`
- Source revision: `22ee4dd`
- Charging behavior: LED ring stays off until USB power is removed; the
  hardware-test LED pattern remains enabled.
- Rebuild with: `pio run -e seeed_xiao_esp32s3`
- SHA-256: `7D7B865F9DE1290379561B907E09E2476D23941A77C00AB1FBF2A9A3DDA89BE9`

The binary is the PlatformIO application image. To flash the device, use
`pio run -e seeed_xiao_esp32s3 -t upload` from the project root.
