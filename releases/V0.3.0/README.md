# Life Recorder V0.3.0

Firmware release for the Seeed Studio XIAO ESP32S3 Sense.

- Firmware image: `firmware.bin`
- PlatformIO environment: `seeed_xiao_esp32s3`
- Source revision: `c2b34da`
- Device information: send `INFO` to receive `INFO <version> recorder <mac>`,
  for example `INFO 0.3.0 recorder 7c:df:a1:00:11:22`.
- Battery level is estimated from powered run time and shown in startup and
  charging LED animations.
- Start and end WAV jingles are updated separately and stored in the SPIFFS
  flash partition; recordings remain on the microSD card.
- Recording begins before the start jingle plays. Playback runs in a dedicated
  task to keep audio streaming continuous while recording.
- Firmware updates are installed to the inactive OTA slot. The image is staged
  on the microSD card and checked with SHA-256 before installation.
- Rebuild with: `pio run -e seeed_xiao_esp32s3`
- SHA-256: `D4C03646B4C5E1EF116D7CFD5387ABE3AD72799D50E5D9D77000A6B2E639A722`

The binary is the PlatformIO application image. To flash the device, use
`pio run -e seeed_xiao_esp32s3 -t upload` from the project root.
