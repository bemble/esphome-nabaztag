# ESPHome - Nabaztag

> Replace the motherboard of your Nabaztag with an ESP and play with the hardware.

Just play with old Nabaztag. Ears, head button, speaker, wheel and probably the input power can be reused easily.
The microphone is an electret microphone, it's way easier to replace it by an i2s one.

## Components

- Nabaztag v1 or v2. Should be possible with a Karotz but the connectors are different (smaller on the Karotz)
- ESP32 ([ESP32 Dev Kit C](https://www.amazon.fr/gp/product/B074RG86SR?&_encoding=UTF8&tag=bemble-21&linkCode=ur2&linkId=e3e6b2688822db2bd779a096dffda58b&camp=1642&creative=6746))
- [INMP441 microphone](https://www.amazon.fr/dp/B07YXF6ZV2?&_encoding=UTF8&tag=bemble-21&linkCode=ur2&linkId=980b291099807d8eb12a9ffb818c0274&camp=1642&creative=6746)
- [MAX98357 DAC](https://www.amazon.fr/dp/B08BCHHZPN?&_encoding=UTF8&tag=bemble-21&linkCode=ur2&linkId=65fe38accd229f9937d377b7f792373c&camp=1642&creative=6746)

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