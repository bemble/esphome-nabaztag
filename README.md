# ESPHome - Nabaztag

> Replace the motherboard of your Nabaztag with an ESP and play with the hardware.

Just play with old Nabaztag. Ears, head button, speaker, wheel and probably the input power can be reused easily.
The microphone is an electret microphone, it's way easier to replace it by an i2s one.

## Components

- Nabaztag v1 or v2. Should be possible with a Karotz but the connectors are different (smaller on the Karotz)
- ESP32
- I2S microphone
- DAC

## Configuration

```yaml
substitutions:
  name: "hackbaztag"
  friendly_name: "Hackbaztag"
  wifi_ap_password: ap_password

packages:
  violet.nabaztag-tag: github://bemble/esphome-nabaztag/violet-nabaztag-tag.yaml@main

esphome:
```

## TODO

- [ ] list used components
- [ ] add photos, schema etc
- [ ] use ears encoder instead of basic time based rotation
- [ ] use a led ring
- [ ] add an optional OLED screen
- [ ] use the wheel to manager leds max brightness (or something else, to be defined)
- [ ] make a PCB (⚠️ Nabaztag and Karotz have different connectors)

## Resources

- [Hack the Nabaztag](https://www.instructables.com/Hack-the-Nabaztag/)
- [Tagtagtag ears encoder](https://github.com/pguyot/tagtagtag-ears)
- [TEARDOWN: NABAZTAG](https://hackaday.com/2020/05/26/teardown-nabaztag/)