# T's DST-Pro22 Carved: Cornfed Govan Fusion and Bright JM45 Fusion

Two separate FM9 presets for the T's DST-Pro22 Carved (H-S-H, large-pole
ceramic pickups). They share effects but do not try to make the same sound.

- **Preset A -- Cornfed Govan Fusion:** based on `CORNFED M50`, the FM9 model
  of the Cornford MK50 II. This is the more Guthrie Govan-oriented option.
- **Preset B -- Bright JM45 Fusion:** based on `Brit JM45`. It is a more open,
  vintage-Marshall fusion lead, not a Guthrie rig clone.

All parameter values below are starting points. Calibrate scene levels by ear
at the actual monitoring volume; do not use the Drive Block Level as a final
output-volume control.

## Routing

`IN 1 -> Drive -> Amp 1 -> Cab 1 -> PEQ -> Delay -> Reverb -> OUT 1`

Use the **Input Gate**, not a separate Gate block:

| Parameter | Value |
| --- | --- |
| Threshold | -73 dB |
| Ratio | 2.5:1 |
| Attack | 10 ms |
| Release | 85 ms |

If legato notes decay unnaturally, lower Threshold to `-76 dB`. If the idle
noise is objectionable, raise it no higher than `-70 dB`.

## Preset A: Cornfed Govan Fusion

### Guitar and scenes

| Scene | Pickup / use | Blocks enabled |
| --- | --- | --- |
| 1 -- Dynamic rhythm | Neck + middle or neck humbucker, guitar volume 7--8 | Amp, Cab, PEQ, light Reverb |
| 2 -- Fusion lead | Neck humbucker, tone full | FET Boost, Amp, Cab, PEQ, Delay, Reverb |
| 3 -- Cutting lead | Bridge humbucker | FET Boost, Amp, Cab, PEQ, Delay, Reverb |

The Cornford model is already saturated enough. Do not use a Tube Screamer
unless a dense modern mix specifically needs more low-end tightening.

### Drive: FET Boost

Enable in Scenes 2 and 3 only.

| Parameter | Value |
| --- | --- |
| Type | FET Boost |
| Drive | 0.00 |
| Tone | 5.00 |
| Level | +3.5 dB |

This substitutes the clean-push role of Guthrie's physical Koko Boost. It is
not a Koko model. If Scene 3 needs more cut, raise Tone only to `5.5`; do not
increase Drive first.

### Amp: CORNFED M50

| Parameter | Scene 1 | Scene 2 | Scene 3 |
| --- | ---: | ---: | ---: |
| Gain | 3.20 | 3.20 | 3.20 |
| Overdrive | 4.20 | 4.20 | 4.20 |
| Bass | 2.40 | 2.40 | 2.15 |
| Middle | 5.60 | 5.60 | 5.90 |
| Treble | 5.10 | 5.10 | 5.25 |
| Master Volume | 4.80 | 4.80 | 4.80 |
| Presence | 3.70 | 3.70 | 3.90 |
| Resonance / Depth | 2.80 | 2.80 | 2.60 |
| Level | Match Scene 2 | Reference | +1.5 dB over Scene 2 |

For more saturation, raise `Overdrive` to `4.8` before raising `Gain`. If the
lead is sharp with the DST's ceramic neck pickup, lower Presence to `3.2`.

### Cab: Dyna-Cab

| Parameter | Value |
| --- | --- |
| Mode | Dyna-Cab |
| Cabinet | 4x12 Friedman V30 |
| Microphone | R121 |
| Mic position | At the cap edge |
| Mic distance | 1.0 in |
| Low Cut | 90 Hz |
| High Cut | 8.0 kHz |

Start with one R121. A second Cab slot with an SM57 is optional only after the
single-mic sound is working: blend it quietly, about `20--30%`, to add pick
attack. It is not required for this preset.

### PEQ

| Band | Frequency | Q | Gain | Scene |
| --- | ---: | ---: | ---: | --- |
| 1 | 100 Hz | -- | High-pass | All |
| 2 | 220 Hz | 0.70 | -1.2 dB | All |
| 3 | 1.45 kHz | 0.70 | +0.8 dB | All |
| 4 | 3.10 kHz | 0.85 | -0.8 dB | All |
| 5 | 1.80 kHz | 0.70 | +0.8 dB | Scene 3 |

### Delay and Reverb

**Delay -- Digital Mono, Scenes 2 and 3 only**

| Parameter | Value |
| --- | --- |
| Time | 380 ms |
| Feedback | 18% |
| Mix | 11% |
| Low Cut | 180 Hz |
| High Cut | 6.2 kHz |

**Reverb -- Medium Plate**

| Scene | Time | Mix | Low Cut | High Cut |
| --- | ---: | ---: | ---: | ---: |
| 1 | 1.5 s | 6% | 180 Hz | 7.5 kHz |
| 2 | 1.8 s | 9% | 180 Hz | 7.0 kHz |
| 3 | 1.9 s | 10% | 180 Hz | 7.0 kHz |

## Preset B: Bright Singing JM45 Fusion

### Guitar and scenes

| Scene | Pickup / use | Blocks enabled |
| --- | --- | --- |
| 1 -- Edge rhythm | Neck + middle, volume 7--8 | Amp, Cab, PEQ, light Reverb |
| 2 -- Singing lead | Neck humbucker, tone full | FET Boost, Amp, Cab, PEQ, Delay, Reverb |
| 3 -- Bright lead | Bridge humbucker | FET Boost, Amp, Cab, PEQ, Delay, Reverb |

### Drive: FET Boost

Enable in Scenes 2 and 3 only.

| Parameter | Value |
| --- | --- |
| Type | FET Boost |
| Drive | 0.00 |
| Tone | 5.30 |
| Level | +4.0 dB |

### Amp: Brit JM45

| Parameter | Scene 1 | Scene 2 | Scene 3 |
| --- | ---: | ---: | ---: |
| Input Drive | 4.80 | 5.15 | 5.15 |
| Bass | 2.20 | 2.20 | 2.00 |
| Middle | 5.80 | 5.80 | 6.00 |
| Treble | 6.20 | 6.20 | 6.00 |
| Master Volume | 7.00 | 7.00 | 7.00 |
| Presence | 4.30 | 4.30 | 4.00 |
| Level | Match Scene 2 | Reference | +1.5 dB over Scene 2 |

If the neck humbucker is too dark, raise Treble to `6.5` before touching
Presence. If pick attack becomes piercing, lower Presence to `3.5`.

### Cab: Dyna-Cab

| Parameter | Value |
| --- | --- |
| Mode | Dyna-Cab |
| Cabinet | 4x12 Brit Green / Greenback-style 4x12 |
| Microphone | R121 |
| Mic position | At the cap edge |
| Mic distance | 1.0 in |
| Low Cut | 90 Hz |
| High Cut | 8.2 kHz |

### PEQ

| Band | Frequency | Q | Gain | Scene |
| --- | ---: | ---: | ---: | --- |
| 1 | 100 Hz | -- | High-pass | All |
| 2 | 220 Hz | 0.70 | -1.5 dB | All |
| 3 | 1.40 kHz | 0.70 | +0.8 dB | All |
| 4 | 3.20 kHz | 0.80 | +0.6 dB | All |
| 5 | 3.20 kHz | 0.80 | -1.0 dB | If bridge pickup is sharp |

### Delay and Reverb

Use the same Delay and Reverb values as Preset A.

## Monitoring and level calibration

- Use these presets direct to monitors, an FRFR speaker, or PA; keep Cab
  enabled in every scene.
- Calibrate Amp `Level` at performance volume. First make Scene 2 equal to a
  known good preset, then make Scene 1 about `1--1.5 dB` quieter and Scene 3
  about `1.5 dB` louder than Scene 2.
