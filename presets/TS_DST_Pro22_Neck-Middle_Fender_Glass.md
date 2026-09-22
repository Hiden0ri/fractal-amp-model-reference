# T's DST-Pro22 Carved: Neck + Middle Fender Glass

This is an FM9 starting preset for the fourth five-way-switch position: the neck-plus-middle sound. It is designed for direct use into full-range monitors, headphones, an audio interface, or PA.

## Guitar basis

Source guitar: T's Guitars DST-Pro22 Carved, serial 031575 (2018).

| Position | Pickup |
| --- | --- |
| Neck | DH-610n large-pole humbucker, ceramic, about 10 kOhm |
| Middle | DS-605 large-pole single-coil, ceramic, about 5 kOhm |
| Bridge | DH-611b large-pole humbucker, ceramic, about 11 kOhm |

The fourth switch position is the neck-plus-middle blend used here. Confirm whether the neck humbucker is automatically split in this position on the individual guitar; the tonal intent is the same either way.

This is not a low-output vintage Strat blend. The DS-605 was developed to match the DH-610n/611b high-gain humbuckers. It has tight low end and extended highs, while the large-pole humbuckers emphasize a long, articulate upper-mid response. Therefore the recipe controls boom and hard upper-mid edge first, rather than adding excessive treble.

## FM9 layout

```text
IN 1 -> Gate -> Compressor -> Drive -> Amp 1 -> Cab 1 -> PEQ -> Delay -> Reverb -> OUT 1
```

Use three scenes. Amp 1 and Cab 1 change channels with the scene. Match scene loudness with the amp's Level control, not by moving Input Drive or Master Volume after the sound is dialed in.

| Scene | Amp 1 channel | Cab 1 channel | Role |
| --- | --- | --- | --- |
| 1 | A: Double Verb Vibrato | A: Blackface Twin 2x12 | Main crystalline clean |
| 2 | B: Super Verb Vibrato | B: Blackface Super 4x10 | Funk, cutting and percussive clean |
| 3 | C: Deluxe Verb Vibrato | C: Blackface Deluxe 1x12 | Edge-of-breakup and lead clean |

The `Vibrato` names identify the original amplifier channel; they do not turn on a vibrato effect in FM9.

## Common blocks

### Gate

Set only high enough to mute idle noise. Do not clamp sustained notes or the soft tail of chord stabs.

### Compressor

Start with `Studio FF` or another transparent studio compressor. Set the threshold for about 2-3 dB of gain reduction on firm picking, a 2:1 ratio, and 50-55% mix. Scene 1 can run with the compressor bypassed for maximum pick dynamics; leave it on in Scene 2.

### Drive

Use a transparent boost such as `FET Boost`, with Drive at minimum and output roughly +2.5 to +3 dB. Leave it off in Scenes 1 and 2. Use it in Scene 3 only when a little more breakup is wanted. A Tube Screamer is optional, but keep its Drive near minimum and use it only after the clean sound works without it.

### PEQ

Use this only as a correction stage after selecting the cabinet IR.

| Adjustment | Starting value | Reason |
| --- | --- | --- |
| Low cut | 80 Hz | Removes unusable sub-low end without thinning the neck-plus-middle blend |
| 200-250 Hz | -1 to -2 dB, broad Q | Controls ash-body and neck pickup boom |
| 2.8-3.5 kHz | -0.5 to -1.5 dB only if needed | Smooths the ceramic large-pole attack when it becomes hard or scratchy |
| 4.5-5.5 kHz | +0.5 to +1 dB only if needed | Adds pick definition after the harsh band has been controlled |

Do not apply the last boost by default. A good Blackface IR should supply the air on its own.

### Time effects

Use a short plate or spring reverb: mix 8-12%, time about 1.5-2.0 s. For the ambient version, add a digital delay around 380-430 ms with 15-20% feedback and low mix. Keep delay bypassed for tight funk rhythm.

## Scene 1: Double Verb Vibrato - crystalline clean

```text
Input Drive  2.1
Bass         2.5
Mid          3.2
Treble       5.4
Presence     3.8
Master       4.5
```

Choose a Blackface Twin-style 2x12 IR. Start with an R121-style ribbon mic or a ribbon/dynamic blend. Set Cab low cut around 80 Hz and high cut around 8.5-9 kHz.

Use this for open chords, arpeggios, and the cleanest "glass" sound. Start with the compressor off. If it is too bright, reduce the cab's high cut to 8 kHz before reducing Treble; that keeps the amp's transient response intact.

## Scene 2: Super Verb Vibrato - funk and spank

```text
Input Drive  2.5
Bass         2.2
Mid          3.7
Treble       5.3
Presence     4.6
Master       4.7
```

Choose a Blackface Super Reverb-style 4x10 IR. Start with Cab low cut around 90 Hz and high cut around 8-8.5 kHz. Leave the compressor on.

This is the preferred scene for the DST neck-plus-middle position: tight low end from the DS-605 prevents the combination from becoming woolly, while the Super Reverb's attack makes the quack and muted sixteenth-note rhythm audible. Use very little reverb.

## Scene 3: Deluxe Verb Vibrato - edge of breakup

```text
Input Drive  3.3
Bass         2.2
Mid          4.1
Treble       5.1
Presence     3.8
Master       4.5
```

Choose a Blackface Deluxe-style 1x12 IR. Start with Cab low cut around 90 Hz and high cut around 7.5-8 kHz. The transparent boost is available for a louder, hairier sound.

This scene should not become a thick neck-humbucker lead tone. If it does, lower Input Drive before increasing high frequencies. The neck-plus-middle position should retain its hollow, separated chord quality even when it starts to break up.

## Hardware routing

- Direct to monitors, headphones, audio interface, or PA: keep Cab 1 on.
- FM9 OUT 1 into the Blackstar HT Stage 60 FX Return and its physical guitar speakers: bypass Cab 1. The real 2x12 replaces the virtual cabinet, so the three scenes will sound more mid-forward and less like their intended Fender cabinets.
- Do not send a full amp-and-cab signal into the Blackstar's normal guitar input; that stacks two preamps and makes the result difficult to tune.

## Quick troubleshooting

| Symptom | First correction |
| --- | --- |
| Clear but painfully sharp | Reduce 3 kHz in PEQ by 1 dB, then lower Cab high cut to 8 kHz |
| Clear alone but disappears in a band mix | Add 0.5-1 dB at 1.5-2 kHz; do not add bass |
| Too dark or too soft | Bypass the compressor first, then try a more direct/dynamic cab mic |
| Too much low-end thump | Increase Cab/PEQ low cut from 80 to 90-100 Hz |
| Not enough quack in position 4 | Verify the neck coil-split behavior and pickup height before changing the amp EQ |

## Sources

- T's Guitars original specification sheet for serial 031575.
- [T's Guitars Original Pickups](https://www.guitar-shop.co.jp/original-pickups/)
- [T's Guitars DST-24 Carved Top announcement](https://www.guitar-shop.co.jp/information/dst-24carvedtop/)
