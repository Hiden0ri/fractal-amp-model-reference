# T's DST-Pro22 Carved: Tornado of Souls Singing Lead

An FM9 lead preset inspired by the character of a supplied `Tornado of Souls`
solo stem: dense midrange, smooth upper treble, distinct pick articulation,
and enough delay to lengthen notes without obscuring fast phrases. This is a
starting-point recreation of the **heard result**, not a claim about Marty
Friedman's original studio equipment.

The source stem was band-separated, so its treble is likely softer than the
full mix. Do not compensate by adding excessive Presence or a very high Cab
high cut.

## Routing

`IN 1 -> T808 Mod -> Amp 1 -> Cab 1 -> PEQ -> Delay -> Reverb -> OUT 1`

Use direct to monitors, an FRFR speaker, headphones, or PA. Keep Cab enabled.

## Guitar and scenes

Use the DST-Pro22 bridge humbucker (`DH-611b`) first, guitar volume full and
tone at `8--10`.

| Scene | Role | Active blocks |
| --- | --- | --- |
| 1 -- Rhythm | Tight 80s metal rhythm | T808, Amp, Cab, PEQ, light Reverb |
| 2 -- Lead | Main solo sound | T808, Amp, Cab, PEQ, Delay, Reverb |
| 3 -- Solo lift | More forward, slightly louder lead | T808, Amp, Cab, PEQ, Delay, Reverb |

## Input Gate

| Parameter | Value |
| --- | --- |
| Threshold | -68 dB |
| Ratio | 2.5:1 |
| Attack | 2 ms |
| Release | 100 ms |

Lower Threshold to `-72 dB` if bends and vibrato tails are being shortened.

## Drive: T808 Mod

Enable in all scenes. This is a TS-style preamp tightener, not the main source
of gain.

| Parameter | Value |
| --- | --- |
| Type | T808 Mod |
| Drive | 0.30 |
| Tone | 4.60 |
| Level | +4.5 dB |

## Amp: Brit 800 Mod

`Brit 800 Mod` is the FM9's modified 50 W JCM800-style model. Its less-strident
top end is useful here: the solo must sing through the upper mids rather than
cut with abrasive treble.

| Parameter | Scene 1 | Scene 2 | Scene 3 |
| --- | ---: | ---: | ---: |
| Input Drive | 5.00 | 5.40 | 5.40 |
| Bass | 2.80 | 3.00 | 2.90 |
| Middle | 6.30 | 6.70 | 6.90 |
| Treble | 4.20 | 4.30 | 4.40 |
| Master Volume | 5.00 | 5.00 | 5.00 |
| Presence | 2.40 | 2.40 | 2.60 |
| Depth | 3.20 | 3.20 | 3.10 |
| Level | Match baseline | Reference | +1.5 dB over Scene 2 |

For more sustain, raise Input Drive to `5.8` before adding another boost. Do
not increase T808 Drive first; that blurs the note edges.

## Cab: Dyna-Cab

| Parameter | Value |
| --- | --- |
| Mode | Dyna-Cab |
| Cabinet | 4x12 1960TV |
| Microphone | R121 |
| Mic position | Cap edge |
| Mic distance | 1.5 in |
| Low Cut | 85 Hz |
| High Cut | 6.2 kHz |

The R121 retains body and keeps the upper treble rounded. Before raising the
high cut, move the mic slightly closer toward the cap if extra pick definition
is needed.

## PEQ

| Band | Frequency | Q | Gain |
| --- | ---: | ---: | ---: |
| 1 | 130 Hz | 1.00 | -1.5 dB |
| 2 | 350 Hz | 1.10 | -2.0 dB |
| 3 | 850 Hz | 0.80 | +1.8 dB |
| 4 | 1.65 kHz | 0.90 | +1.5 dB |
| 5 | 3.70 kHz | 1.00 | -1.5 dB |

The 850 Hz and 1.65 kHz boosts are the core of the vocal midrange. If the lead
does not cut, raise 1.65 kHz by only `+0.5 dB`; do not add Bass or Presence.

## Delay and Reverb

**Delay -- Mono Tape, Scenes 2 and 3 only**

| Parameter | Value |
| --- | --- |
| Time | 380 ms |
| Feedback | 19% |
| Mix | 14% |
| Low Cut | 180 Hz |
| High Cut | 4.8 kHz |

**Reverb -- Medium Plate**

| Scene | Time | Pre-delay | Mix | High Cut |
| --- | ---: | ---: | ---: | ---: |
| 1 | 1.0 s | 15 ms | 4% | 5.5 kHz |
| 2 | 1.4 s | 20 ms | 8% | 5.0 kHz |
| 3 | 1.6 s | 20 ms | 9% | 5.0 kHz |

## Quick adjustments

| Problem | First adjustment |
| --- | --- |
| Lead is too sharp | Lower Presence to `2.0`, then reduce 3.7 kHz by another 0.5 dB |
| Lead is too dark | Move R121 closer to the cap, then raise Treble to `4.6` |
| Legato lacks sustain | Lower gate Threshold, then raise Input Drive to `5.8` |
| Low strings cloud fast phrases | Raise Cab Low Cut to `95 Hz` |
| Lead is not loud enough | Raise Scene 3 Amp Level; do not raise Drive-block Level |

## Reference

- [Fractal Audio amp-model list](https://wiki.fractalaudio.com/wiki/index.php?title=Amp_models)
