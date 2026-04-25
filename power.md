# Power Conditioning & Protection

## Current topology

```
Wall → Furman M-8x2 → AV gear
```

Single point of distribution, surge protection, and EMI/RFI filtering.

## Planned topology (after upgrade)

The **Furman P-1800 AR is on hand to replace the M-8x2** (not stack with it). After the swap:

```
Wall → Furman P-1800 AR → AV gear
```

The upgrade trades the M-8x2 for active voltage regulation (AVR — keeps line voltage near 120 V) on top of the surge + conditioning the M-8x2 already provides.

## Furman M-8x2 (in service)

- Function: distribution + surge + filtering (passive)
- Form factor: 1U rack, 8 rear outlets
- Use: feeds AVR + power amp + sources

## Furman P-1800 AR (pending swap)

- Function: voltage regulation + power conditioning + series-mode surge
- Adds: AVR vs M-8x2's passive-only design
- Watch after install: front-panel voltage display — if line voltage drifts more than ±10 V from 120 V the AR is doing real work; record readings if it ever clips or trips
- Pre-swap checklist:
  - Confirm P-1800 AR outlet count covers all rack gear currently on M-8x2
  - Confirm rack space / form factor (P-1800 is also rack-mount but verify depth)
  - Plan a downtime window (rack power-cycle)
  - Note current channel trims / settings before swap so any new ground/voltage condition can be compared

## What's protected vs not

| Device | On Furman chain? |
|---|---|
| Marantz SR5014 | yes |
| Emotiva BasX A7+ | yes |
| Sources (streamers, disc, etc.) | yes |
| BIC F-12 subwoofer | (verify — high-draw subs sometimes on separate circuit) |
| Living Room KEF Q500 | n/a (passive speakers) |

## Things to log here

- Date M-8x2 → P-1800 AR swap completed
- Any voltage anomalies displayed by the P-1800 AR after install
- Any clamp/event indicators triggered
- Replacement of MOVs / surge cells (manufacturer-specific lifetime)
