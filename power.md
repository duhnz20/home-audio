# Power Conditioning & Protection

## Topology

```
Wall → Furman P-1800 AR → Furman M-8x2 → AV gear
```

The P-1800 AR was recently added in front of the M-8x2 to provide active voltage regulation (AVR — keeps line voltage near 120 V) on top of the M-8x2's surge protection and EMI/RFI filtering.

## Furman P-1800 AR

- Function: voltage regulation + power conditioning + series-mode surge
- Use: front-end protection for the rack
- Watch: front-panel voltage display — if line voltage drifts more than ±10 V from 120 V the AR is doing real work; record the readings if it ever clips or trips

## Furman M-8x2

- Function: distribution + surge + filtering
- Outlets: 8 rear (1U rackmount form factor)
- Use: downstream of P-1800 AR, feeds the AVR + power amp + sources

## What's protected vs not

| Device | On Furman chain? |
|---|---|
| Marantz SR5014 | yes |
| Emotiva BasX A7+ | yes |
| Sources (streamers, disc, etc.) | yes |
| BIC F-12 subwoofer | (verify — high-draw subs sometimes on separate circuit) |
| Living Room KEF Q500 | n/a (passive speakers) |

## Things to log here

- Date P-1800 AR added
- Any voltage anomalies displayed
- Any clamp/event indicators triggered
- Replacement of MOVs / surge cells (manufacturer-specific lifetime)
