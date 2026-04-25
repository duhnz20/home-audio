# Power Conditioning & Protection

## Topology

```
Wall → Furman P-1800 AR → AV gear
```

Single point of voltage regulation, conditioning, and series-mode surge protection for the rack.

## Furman P-1800 AR (in service)

- Function: voltage regulation + power conditioning + series-mode surge
- Adds vs the M-8x2 it replaced: active voltage regulation (AVR — keeps line voltage near 120 V across input range ~97-141 V)
- Front-panel display: input voltage, output voltage, current draw — useful for passively monitoring line quality
- Extreme-voltage shutdown: cuts power to the rack if input voltage goes outside the safe operating range

## Furman M-8x2 (retired)

- Previously in service, replaced by the P-1800 AR
- Function had been: passive surge + EMI/RFI filtering + 8-outlet rack distribution
- No longer in the signal/power path

## What's protected vs not

| Device | On Furman chain? |
|---|---|
| Marantz SR5014 | yes |
| Emotiva BasX A7+ | yes |
| Sources (streamers, disc, etc.) | yes |
| BIC F-12 subwoofer | (verify — high-draw subs sometimes on separate circuit) |
| Living Room KEF Q500 | n/a (passive speakers) |

## Things to log here

- Date of M-8x2 → P-1800 AR swap (recorded in maintenance-log.md)
- Periodic line voltage readings from the AR's front-panel display
- Any clamp/event indicators triggered
- Any extreme-voltage shutdown events
- Replacement of MOVs / surge cells (manufacturer-specific lifetime — series-mode parts have less degradation than MOV)

## Operational notes

- Inrush on power-up: the P-1800 AR has a non-trivial transformer; flipping its master switch can momentarily dim other devices on the same circuit. Not damaging, just expected behavior.
- If line voltage display drifts more than ±10 V from 120 V chronically, contact ComEd — chronic out-of-range voltage is utility-side, not gear-side.
