# Life Recorder V0.2.2

Firmware release for the Seeed Studio XIAO ESP32S3 Sense.

- Firmware image: `firmware.bin`
- PlatformIO environment: `seeed_xiao_esp32s3`
- Source revision: `0d8de23`
- Device information: send `INFO` to receive `INFO <version> recorder <mac>`,
  for example `INFO 0.2.2 recorder 7c:df:a1:00:11:22`.
- Serial update: received images are staged on the microSD card, checked with
  SHA-256, installed to the inactive OTA slot, and booted after restart.
- Rebuild with: `pio run -e seeed_xiao_esp32s3`
- SHA-256: `D6913199BBC474D369F85961A02E1F315245B5FB781601DE3EC0BDD7E363B347`

The binary is the PlatformIO application image. To flash the device, use
`pio run -e seeed_xiao_esp32s3 -t upload` from the project root.
