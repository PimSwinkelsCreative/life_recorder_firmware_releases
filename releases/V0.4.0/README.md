# Life Recorder V0.4.0

Firmware for the Seeed Studio XIAO ESP32S3 Sense.

- Firmware image: `firmware.bin`
- PlatformIO environment: `seeed_xiao_esp32s3`
- Source base: `ed7f8d7`, plus the V0.4.0 version change.
- Device information: `INFO` returns `INFO 0.4.0 recorder <mac>`.
- Recording numbers are reserved in flash and are not reused after deletion or
  `WIPE`.
- Exports include SHA-256 checksums and mark acknowledged recordings as
  uploaded in place. Legacy `/BACKUP` recordings remain available via `BACKUP`.
  The new export protocol requires an updated host client.
- `LIST`, `DELETE`, and `WIPE` manage recordings. `WIPE` permanently removes
  root recordings and markers and all contents of `/BACKUP`.
- LED animations are white except for red recording feedback; the startup
  battery animation is five times faster.
- Audio output uses 70% digital sample amplitude. The hardware test command is
  `TEST` followed by a newline.
- Rebuild with: `pio run -e seeed_xiao_esp32s3`
- SHA-256: `1C4E51D12232F54F4E884AE9FC5A125FAB4AC51D29B36DD505F638F1D8FEBB06`

The binary is the PlatformIO application image. Hardware and web-interface
testing are still required before release.
