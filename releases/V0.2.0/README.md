# Life Recorder V0.2.0

Firmware release for the Seeed Studio XIAO ESP32S3 Sense.

- Firmware image: `firmware.bin`
- PlatformIO environment: `seeed_xiao_esp32s3`
- Source revision: `e096a60`
- Serial version query: send `VERSION`
- Serial update utility: `python tools/upload_firmware.py COM5 firmware.bin`
- SHA-256: `E67570445D3BA8DA082A4BC51C5AC0E198211165CE2C16FADB45B1C45F129ACC`

This release adds serial firmware updates. The device stages the received
application image on the microSD card, verifies its SHA-256, writes the
inactive OTA slot, and restarts into the new firmware. SHA-256 detects
corruption but does not authenticate the firmware source.

The binary is the PlatformIO application image. Devices on older firmware
must first be updated through PlatformIO with
`pio run -e seeed_xiao_esp32s3 -t upload`.
