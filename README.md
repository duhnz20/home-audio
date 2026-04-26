# Home Audio

Documentation for the two-zone home audio system.

## Layout

- **Main Room (Zone 1):** 5.1 home theater. Marantz SR5014 as pre/pro, Emotiva BasX A7+ amp ch 1-5 driving KEF R3 / R2 Meta / Q150 stack, BIC F-12 sub on SR5014 LFE pre-out.
- **Living Room (Zone 2):** Stereo. SR5014 Zone 2 pre-outs → **same Emotiva BasX A7+** (ch 6-7) → KEF Q500 pair.

**Architectural rule:** No speaker in this house is driven by the Marantz SR5014's internal amps. All amplification flows through the single Emotiva BasX A7+.

## Index

| Doc | Purpose |
|---|---|
| [equipment.md](equipment.md) | Component inventory with model numbers and roles |
| [signal-chain.md](signal-chain.md) | Signal flow diagrams for both zones |
| [power.md](power.md) | Power conditioning and protection |
| [calibration.md](calibration.md) | Audyssey runs, settings, room notes |
| [troubleshooting.md](troubleshooting.md) | Known issues and recovery procedures |
| [maintenance-log.md](maintenance-log.md) | Dated log of changes, swaps, recalibrations |
| [manuals.md](manuals.md) | Index of all equipment manuals — links to manufacturer source PDFs; local PDFs in [`manuals/`](manuals/) (gitignored) |

## Quick reference

**Main room signal path (5.1):**

```
sources → Marantz SR5014 (HDMI / network in)
       → SR5014 5.1 pre-outs
       → Emotiva BasX A7+ ch 1-5
       → KEF R3 (FL/FR) + KEF R2 Meta (Center) + KEF Q150 (Surround L/R)
SR5014 sub/LFE out → BIC America Formula F-12 (RCA in)
```

**Zone 2 signal path (stereo):**

```
sources → Marantz SR5014 Zone 2 pre-outs
       → Emotiva BasX A7+ ch 6-7  (same physical amp as main room)
       → KEF Q500 (Living Room L/R)
```

**Power chain (current):**

```
Wall → Furman Prestige Series P-1800 PF R → SR5014, Emotiva BasX A7+, sources
```

<!-- Public mirror at https://github.com/duhnz20/home-audio -->
