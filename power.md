# Power Conditioning & Protection

## Topology

```
Wall → Furman Prestige Series P-1800 PF R → AV gear
```

Single point of power conditioning, transient current delivery, and surge protection for the rack.

## Furman Prestige Series P-1800 PF R (in service)

- Function: Power Factor Technology + EMI/RFI conditioning + non-sacrificial surge protection
- **Power Factor Technology** — 45A peak current reservoir feeds the Emotiva BasX A7+ instantaneously on dynamic transients (movie LFE peaks, orchestral crescendos) without sag
- **3 isolated outlet banks** (separate digital, analog, and high-current zones) — reduces inter-component noise crosstalk
- **SMP (Series Multi-Stage Protection)** — non-sacrificial surge defense, survives repeated hits without degradation
- **EVS (Extreme Voltage Shutdown)** — disconnects load below 90 V or above 140 V
- **LiFT (Linear Filtration Technology)** — 30 dB @ 2kHz / 40 dB @ 10kHz / 50 dB @ 20kHz / 70 dB @ 100kHz HF noise rejection
- **Surge clamp:** 188 VAC peak @ 3,000 A initial / 6,500 A max / 1 ns response
- **No voltage regulation** — relies on stable mains; if mains drift outside ~110-125 V chronically, consider AVR-equipped Furman (e.g., P-1800 AR)
- Front-panel: dimmable LED voltmeter (no ammeter)

## What's protected vs not

| Device | On Furman chain? |
|---|---|
| Marantz SR5014 | yes |
| Emotiva BasX A7+ | yes (high-current bank — benefits from PF reservoir) |
| Sources (streamers, disc, etc.) | yes |
| BIC F-12 subwoofer | (verify — high-draw subs sometimes on separate circuit) |
| Living Room KEF Q500 | n/a (passive speakers) |

## Things to log here

- Periodic line voltage readings from the PF R's front-panel display
- Any EVS shutdown events (under 90 V / over 140 V)
- Replacement of MOVs / surge cells (SMP is non-sacrificial — much longer lifetime than MOV-only units)

## Operational notes

- Inrush on power-up: the PF R's capacitor bank charges quickly but momentarily presents a high-current load; flipping its master switch may briefly dim other devices on the same circuit. Not damaging, just expected behavior.
- Voltage display drift: if you see chronic readings outside ~110-125 V, contact ComEd — chronic out-of-range voltage is utility-side, not gear-side. The PF R does not regulate, so the rack will see whatever the wall provides.

## Power conditioner history

- **Currently in service:** Furman Prestige Series P-1800 PF R (since 2026-04-25)
- **Previously briefly in service:** Furman P-1800 AR (replaced by PF R; AR is voltage-regulating but its series autoformer can theoretically restrict transient current to the A7+ — PF R chosen for transient delivery)
- **Earlier:** Furman M-8x2 (retired; passive surge + EMI/RFI filtering + 8-outlet distribution)
- See `maintenance-log.md` for swap dates.
