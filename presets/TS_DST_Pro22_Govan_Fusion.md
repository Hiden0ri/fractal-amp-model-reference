# T's DST-Pro22 Carved: Guthrie Govan-Style Fusion

This is an FM9 starting preset for the 2018 T's Guitars DST-Pro22 Carved (serial 031575). It aims for the expressive, medium-gain fusion language associated with Guthrie Govan's Suhr Badger 30 period: clear note separation, fast response to pick attack, and enough gain to sustain a line without hiding poor articulation.

It is not intended to clone one song, a particular live rig, or Guthrie's current FM9 preset.

## Guitar basis

| Position | Pickup | Recommended use |
| --- | --- | --- |
| Neck | DH-610n large-pole ceramic humbucker | Legato lead, round chord melody |
| Neck + middle | DH-610n + DS-605 | Clean chords and rhythmic fusion comping |
| Bridge | DH-611b large-pole ceramic humbucker | Driven rhythm, articulate rock-fusion lead |

The DST pickup set has more output and a firmer upper-mid attack than Guthrie's familiar Suhr HSH setup. Keep the low end and 2.5-3.5 kHz region under control before adding gain or treble.

## FM9 layout

```text
IN 1 -> Gate -> Compressor -> Drive -> Amp 1 -> Cab 1 -> PEQ -> Delay -> Reverb -> OUT 1
```

Use `Suhr Badger 30` in Amp 1 for every scene. The real Badger is a single-channel amp that interacts strongly with the guitar volume control; treat the FM9 scene changes as convenient gain staging, not as three unrelated amplifier sounds.

| Scene | Amp / drive state | Intended role |
| --- | --- | --- |
| 1 | Badger low gain, drive off | Neck + middle clean and fusion comping |
| 2 | Badger edge of breakup, drive off | Dynamic rhythm and touch-sensitive lead |
| 3 | Badger pushed by clean boost | Singing lead without a saturated metal character |

## Common blocks

## Exact starting parameters

The values below are the parameters to change from a freshly created FM9 preset. Leave every parameter not listed at its default value. Block parameter labels can vary slightly with firmware, but the function and values are the same.

### Input Gate

Use the gate on the `Input 1` block rather than adding a separate Gate block.

| Parameter | Value |
| --- | --- |
| Threshold | `-73.0 dB` |
| Ratio | `2.50 : 1` |
| Attack | `10 ms` |
| Release | `85 ms` |

If a lightly picked sustained note shuts off, lower Threshold to `-76 dB`. If high-gain Scene 3 hisses too much when idle, increase it only to about `-70 dB`.

### Gate

Use only the Input Gate values above. A hard gate removes the weakly picked notes, slides, and volume-knob clean-up that make this style work.

### Compressor

Use Compressor 1, channel A, in Scene 1 only.

| Parameter | Value |
| --- | --- |
| Type | `Studio FF` |
| Threshold | Adjust for `1.5-2 dB` gain reduction on a firm chord |
| Ratio | `2.00 : 1` |
| Attack | `25 ms` |
| Release | `110 ms` |
| Mix | `40%` |
| Level | Match bypassed level exactly |

Bypass Compressor 1 in Scenes 2 and 3. Do not use a high-ratio sustain compressor for lead tone.

### Drive

Use Drive 1, channel A, in Scene 3 only.

| Parameter | Value |
| --- | --- |
| Type | `FET Boost` |
| Drive | `0.00` |
| Level | `+4.00 dB` |

Bypass Drive 1 in Scenes 1 and 2. This is deliberately a clean boost rather than a Tube Screamer. It preserves the Badger's dynamic mids and avoids making the ceramic bridge humbucker nasal.

If Scene 3 needs more focus in a dense band mix, substitute a low-drive `T808 Mod`:

```text
Drive  0.15-0.30
Tone   4.5-5.0
Level  set for +3 to +4 dB
```

Use this only after the FET Boost version works. The Tube Screamer is a mix tool, not the core sound.

### Cab

Use Cab 1, channel A, in every scene. Start with a `2x12 Suhr` / `2x12 M65`-type cabinet if available in the installed firmware or IR library. Otherwise use a balanced 2x12 with Greenback/G12-65 character. Use an R121 ribbon or a ribbon plus SM57 blend; avoid a lone bright on-axis 57.

| Parameter | Value |
| --- | --- |
| IR | `2x12 Suhr / M65`, or closest balanced 2x12 |
| Mic | `R121` or `R121 + SM57` blend |
| Low Cut | `90 Hz` |
| High Cut | `8.2 kHz` |
| Level | Match the bypassed level exactly |

For direct monitoring, keep the Cab block on. When sending `OUT 1` to the Blackstar HT Stage 60 FX Return and its physical speakers, bypass Cab 1; the Blackstar cabinet then replaces the virtual 2x12, so re-check all EQ values.

### PEQ

Use correction after the cab, not as a fixed preset EQ.

| Band | Starting correction | Purpose |
| --- | --- | --- |
| Band | Frequency | Q | Gain | Purpose |
| --- | --- | --- | --- | --- |
| 1 | `90 Hz` | default | `HPF` | Stops the ash body / humbucker low end from masking fast lines |
| 2 | `220 Hz` | `0.70` | `-1.0 dB` | Removes bloom before increasing clarity |
| 3 | `3.10 kHz` | `0.80` | `-1.0 dB` | Smooths the ceramic large-pole attack |
| 4 | `1.60 kHz` | `0.70` | `+0.8 dB`, Scene 3 only | Adds vocal lead projection without fizz |

Do not boost 5-7 kHz to create clarity. Pick articulation should come from gain staging and the cabinet choice.

### Delay and reverb

Keep both effects low enough that fast phrases remain audible.

Use Delay 1, channel A, in Scene 3 only.

| Delay parameter | Value |
| --- | --- |
| Type | `Digital Mono` |
| Time | `380 ms` |
| Feedback | `18%` |
| Mix | `12%` |
| Low Cut | `180 Hz` |
| High Cut | `6.2 kHz` |
| Level | `0.0 dB` |

Use Reverb 1, channel A, in every scene.

| Reverb parameter | Scene 1 | Scene 2 | Scene 3 |
| --- | --- | --- | --- |
| Type | `Medium Plate` | `Medium Plate` | `Medium Plate` |
| Time | `1.6 s` | `1.6 s` | `1.9 s` |
| Mix | `7%` | `8%` | `10%` |
| Low Cut | `180 Hz` | `180 Hz` | `180 Hz` |
| High Cut | `7.5 kHz` | `7.5 kHz` | `7.0 kHz` |

Scene 1 can use a short room/plate and no delay. Scene 3 can use the 360-390 ms delay. Set delay and reverb spillover on if scene changes otherwise cut off a held phrase.

## Scene 1: Neck + middle fusion clean

Use the fourth switch position. Start with the guitar volume at 8-9.

```text
Input Drive  2.0
Bass         2.7
Middle       5.1
Treble       4.7
Presence     3.5
Master       5.0
Level        calibrate to Scene 2, as described below
```

This is for clean chord voicings, muted rhythmic figures, and lines that should open up when picked harder. If it is too dark, try a more open cab mic before raising Treble.

## Scene 2: Dynamic fusion crunch

Use bridge for rhythm, or neck for lower-gain lead. Start with guitar volume at 7-8 for rhythm and turn it fully up for a lead phrase.

```text
Input Drive  3.4
Bass         2.4
Middle       5.4
Treble       4.9
Presence     3.8
Master       5.0
Level        set as the reference loudness
```

Leave Drive and Compressor off initially. This is the main scene: it should clean up with a lighter right hand and bark only when you dig in. If it feels too compressed, lower Input Drive to 3.0 before reducing Master.

## Scene 3: Singing lead

Use neck humbucker for the roundest lead; use bridge for more cut. Turn on the FET Boost and delay.

```text
Input Drive  4.1
Bass         2.1
Middle       5.7
Treble       4.8
Presence     3.6
Master       5.0
Level        +1.5 to +2.0 dB above Scene 2
```

Set the Amp Level so this scene is only about 1.5-2 dB louder than Scene 2. Set Scene 1 to the same loudness as Scene 2 with guitar volume fully up. More level is useful; substantially more distortion usually is not. A fusion lead should retain the separation of two-note intervals and the attack of economy-picked runs.

## Playing and setup notes

- Begin with pickup heights that balance neck and bridge output. If the neck pickup is cloudy, lower its bass-side height slightly before adding treble in the FM9.
- Use the guitar volume knob: Scene 2 with volume 6-7 is part of the intended palette, not an emergency clean channel.
- Set each scene's final loudness with `Level`, not `Input Drive` or `Master`.
- If using the Blackstar return, use less Bass and less 180-250 Hz cut than through FRFR only after listening at actual playing volume. The physical 2x12 changes the response substantially.

## Sources

- [Guthrie Govan gear interview: Suhr Badger 30 and Suhr Koko Boost](https://www.premierguitar.com/artists/the-aristocrats-guthrie-govan-and-bryan-beller-rock-and-awe)
- [Suhr Badger product description](https://www.suhr.com/electronics/amplifiers/suhr-badger/)
- [Fractal Audio Amp Models: Suhr Badger and model controls](https://wiki.fractalaudio.com/wiki/index.php?title=Amp_models)
- T's Guitars original specification sheet for serial 031575.
