# Home Audio

Documentation for the two-zone home audio system.

## Layout

- **Main Room (Zone 1):** 7.1 home theater driven by Marantz SR5014 + Emotiva BasX A7+ amplification, KEF speaker stack, BIC F-12 sub
- **Living Room (Zone 2):** Stereo pair of KEF Q500 driven by Marantz Zone 2 outputs

## Index

| Doc | Purpose |
|---|---|
| [equipment.md](equipment.md) | Component inventory with model numbers and roles |
| [signal-chain.md](signal-chain.md) | Signal flow diagrams for both zones |
| [power.md](power.md) | Power conditioning and protection |
| [calibration.md](calibration.md) | Audyssey runs, settings, room notes |
| [troubleshooting.md](troubleshooting.md) | Known issues and recovery procedures |
| [maintenance-log.md](maintenance-log.md) | Dated log of changes, swaps, recalibrations |

## Quick reference

**Main room signal path:**

```
sources → Marantz SR5014 (HDMI / network in)
       → SR5014 pre-outs (7.1)
       → Emotiva BasX A7+ (7-channel power amp)
       → KEF R3 (FL/FR) + KEF Q250C (Center) + KEF Q150 (Surrounds)
SR5014 sub/LFE out → BIC America Formula F-12 (RCA in)
```

**Zone 2 signal path:**

```
sources → Marantz SR5014 Zone 2 outputs
       → KEF Q500 (Living Room front pair)
```

**Power chain:**

```
Wall → Furman P-1800 AR (front-end conditioner)
     → Furman M-8x2 (downstream distribution)
     → SR5014, Emotiva BasX A7+, sources
```
