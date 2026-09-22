# 7-String Soldano High Gain: Ave Mujica Style

An FM9 style-oriented high-gain preset for a seven-string guitar in Drop A
(`A-E-A-D-G-B-E`). It uses the Soldano SLO-100 model, `SOLO 100 LEAD`.

This is **not** a claim that it reproduces the band's actual live rig. It aims
at the useful musical traits: firm low-A palm mutes, clear chord extensions,
present upper mids, and a lead sound that stays articulate without becoming a
scooped djent preset.

## Routing

`IN 1 -> T808 Mod -> FET Boost -> Amp 1 -> Cab 1 -> PEQ -> Delay -> Reverb -> OUT 1`

Use it direct to monitors, an FRFR speaker, or PA. Keep Cab enabled.

## Guitar and scenes

| Scene | Intended use | Pickup / controls | Active blocks |
| --- | --- | --- | --- |
| 1 -- Tight rhythm | Palm-muted riffs and dense chords | Bridge humbucker, tone full | T808, Amp, Cab, PEQ, short Reverb |
| 2 -- Lead | Single-note melody and harmonized lead | Neck humbucker or bridge humbucker | T808, FET Boost, Amp, Cab, PEQ, Delay, Reverb |
| 3 -- Wide rhythm | Open chords and less-muted riffs | Bridge humbucker | T808, Amp, Cab, PEQ, Reverb |

Scene 3 is intentionally only a little wider than Scene 1. It is not a second
high-gain tone with more bass; that would make a Drop-A seven-string cloudy.

## Input Gate

| Parameter | Value |
| --- | --- |
| Threshold | -68 dB |
| Ratio | 3.0:1 |
| Attack | 2 ms |
| Release | 100 ms |

If sustained notes stop abruptly, lower Threshold to `-72 dB`. Do not simply
raise it for a tighter rhythm tone; use the T808 and the low cut first.

## Drive 1: T808 Mod

Enable in all three scenes.

| Parameter | Value |
| --- | --- |
| Type | T808 Mod |
| Drive | 0.20 |
| Tone | 5.20 |
| Level | +5.0 dB |

This is a tightening device, not the main source of distortion. It removes
some loose low end before the SLO input and gives the pick a more immediate
attack. If the sound is thin, reduce Level to `+4.0 dB` before increasing Bass
in the Amp block.

## Drive 2: FET Boost

Enable in Scene 2 only.

| Parameter | Value |
| --- | --- |
| Type | FET Boost |
| Drive | 0.00 |
| Tone | 5.00 |
| Level | +2.0 dB |

It provides extra sustain and harmonic density for lead notes without changing
the rhythm EQ. If lead volume is still insufficient after level matching,
increase Scene 2 Amp Level before raising this control.

## Amp: SOLO 100 LEAD

| Parameter | Scene 1 | Scene 2 | Scene 3 |
| --- | ---: | ---: | ---: |
| Input Drive | 5.20 | 5.20 | 5.00 |
| Bass | 2.20 | 2.20 | 2.60 |
| Middle | 5.40 | 5.60 | 5.20 |
| Treble | 5.20 | 5.10 | 5.30 |
| Master Volume | 4.20 | 4.20 | 4.20 |
| Presence | 3.40 | 3.20 | 3.60 |
| Depth | 2.50 | 2.50 | 2.80 |
| Level | Match Scene 1 | +1.5 dB over Scene 1 | Match Scene 1 |

`Input Drive` is the amp's Gain. Do not exceed `6.0` before testing in a mix:
more gain makes seven-string chord voicings smaller rather than heavier.

If your bridge pickup is active or unusually high output, start with Input
Drive at `4.6` and use the same rest of the settings. If it is a lower-output
passive pickup, the listed `5.2` is the appropriate starting point.

## Cab: Dyna-Cab

| Parameter | Value |
| --- | --- |
| Mode | Dyna-Cab |
| Cabinet | 4x12 Solo 100 |
| Microphone | R121 |
| Mic position | Cap edge |
| Mic distance | 1.0 in |
| Low Cut | 80 Hz |
| High Cut | 8.4 kHz |

The R121 keeps the V30-style cabinet substantial without the sharp top end of
an on-axis 57. For more pick definition, add a second Cab slot with `SM57`,
also at the cap edge, but blend it at only `20--25%`.

## PEQ

| Band | Frequency | Q | Gain | Scene |
| --- | ---: | ---: | ---: | --- |
| 1 | 80 Hz | -- | High-pass | All |
| 2 | 180 Hz | 0.80 | -1.8 dB | All |
| 3 | 750 Hz | 0.70 | +0.8 dB | All |
| 4 | 1.55 kHz | 0.75 | +1.0 dB | All |
| 5 | 3.60 kHz | 1.00 | -1.0 dB | All |
| 6 | 1.80 kHz | 0.70 | +0.8 dB | Scene 2 only |

For a more modern, compressed rhythm, lower Band 3 to `0 dB`; do not scoop it
below `-1 dB`, or the guitar will disappear when bass and drums enter.

## Delay and Reverb

**Delay -- Digital Mono, Scene 2 only**

| Parameter | Value |
| --- | --- |
| Time | 360 ms |
| Feedback | 16% |
| Mix | 10% |
| Low Cut | 200 Hz |
| High Cut | 6.0 kHz |

**Reverb -- Medium Plate**

| Scene | Time | Mix | Low Cut | High Cut |
| --- | ---: | ---: | ---: | ---: |
| 1 | 1.2 s | 4% | 200 Hz | 7.0 kHz |
| 2 | 1.7 s | 8% | 200 Hz | 6.8 kHz |
| 3 | 1.4 s | 5% | 200 Hz | 7.0 kHz |

## Quick adjustments

| Problem | Change first |
| --- | --- |
| Low A booms or flubs | Raise Cab Low Cut to 90 Hz, then lower Amp Bass to 1.8 |
| Palm mutes lack impact | Lower Cab Low Cut to 75 Hz; do not add Amp Bass first |
| Rhythm is fizzy | Lower Cab High Cut to 7.8 kHz or lower Presence to 2.8 |
| Rhythm is dull | Raise Mic position slightly toward the cap, then raise Treble by 0.3 |
| Lead is not loud enough | Raise Scene 2 Amp Level by 1 dB |
| Lead lacks sustain | Raise FET Boost Level to +3 dB, then Input Drive to 5.5 |
