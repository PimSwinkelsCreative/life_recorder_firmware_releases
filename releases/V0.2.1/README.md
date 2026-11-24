# Life Recorder V0.2.1

Firmware release for the Seeed Studio XIAO ESP32S3 Sense.

- Firmware image: `firmware.bin`
- PlatformIO environment: `seeed_xiao_esp32s3`
- Source revision: `1417096`
- Device information: send `INFO` to receive `INFO <version> recorder <mac>`.
- Serial update: received images are staged on the microSD card, checked with
  SHA-256, installed to the inactive OTA slot, and booted after restart.
- Rebuild with: `pio run -e seeed_xiao_esp32s3`
- SHA-256: `1CFBB2D6C9C1F91A5CD84189CE8B35AD2DFF78F2C0F2658CE80977B84D547CB2`

The binary is the PlatformIO application image. To flash the device, use
`pio run -e seeed_xiao_esp32s3 -t upload` from the project root.
