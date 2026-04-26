# Power Conditioning & Protection

## Topology

```
Wall → Furman Prestige Series P-1800 PF R → AV gear
```

Single point of power conditioning, transient current delivery, and surge protection for the rack.

## Furman Prestige Series P-1800 PF R (in service)

Specs verified from `manuals/furman-p1800-pfr-datasheet.pdf` and `furman-p1800-pfr-owners-manual.pdf`.

- Function: Power Factor Technology + EMI/RFI conditioning + non-sacrificial surge protection
- **Power Factor Technology** — 45 A peak current reservoir feeds the Emotiva BasX A7+ instantaneously on dynamic transients (movie LFE peaks, orchestral crescendos) without sag
- **9 outlets total** — 8 rear panel (3 widely-spaced "Secure Strap" plug-locking transformer outlets + 5 standard high-current) + 1 front-panel USB convenience outlet for media-device charging
- **3 isolated outlet banks** (separate digital, analog, and high-current zones) — reduces inter-component noise crosstalk
- **SMP (Series Multi-Stage Protection)** — non-sacrificial surge defense, survives repeated 6 kV / 3 kA pulses without degradation
- **EVS (Extreme Voltage Shutdown)** — **trips at >140 VAC nominal — overvoltage only.** Per the datasheet, EVS "constantly monitors incoming voltage, and once any overvoltage condition over 140 volts AC is detected, a relay opens which immediately shuts down the unit and all connected equipment." There is **no datasheet-published undervoltage cutoff**; the 90 V figure is the lower bound of the **operating** voltage range, not an EVS trip threshold.
- **Operating voltage range:** 90 – 139 VAC (no AVR / autoformer — passes input voltage through unmodified)
- **LiFT (Linear Filtration Technology)** — 30 dB @ 2 kHz / 40 dB @ 10 kHz / 50 dB @ 20 kHz / 70 dB @ 100 kHz HF noise rejection
- **Surge clamp:** 188 VAC peak @ 3,000 A initial / 6,500 A max / 1 ns response, line-to-neutral mode (zero ground leakage)
- **15 A maximum current** with high-inrush magnetic circuit breaker
- **Reactive power:** 460 VA · **No-load consumption:** 8 W
- Front-panel: dimmable digital LED voltmeter, color-coded voltage range indicators, "Protection OK" + "Extreme Voltage" LEDs (no ammeter)
- Rear: BNC connector for 12 VAC 0.5 A gooseneck rack lamp
- Captive 10 ft, 14 AWG/3 line cord with NEMA 5-15 plug
- 1U rack form factor (19" W × 12" D × 1¾" H, 13 lbs)
- **No voltage regulation** — relies on stable mains; if mains drift outside ~110-125 V chronically, consider AVR-equipped Furman (e.g., P-1800 AR)

## What an EVS trip looks like

If line voltage rises above ~140 VAC, the EVS relay opens and **all connected equipment goes dark** simultaneously. Front-panel "Extreme Voltage" indicator lights. When the line voltage returns to the safe range, the unit auto-resets per the datasheet ("the unit may be reset and will operate normally"). If the trip is recurring, the cause is utility-side — call ComEd before assuming gear failure.

Conversely, if line voltage drifts **below** 90 VAC, the PF R does not actively shut down — it just passes whatever voltage it's getting through to the load. The Marantz SR5014 and Emotiva A7+ both have their own internal under-voltage protection circuits (the SR5014 uses a microprocessor-controlled status LED for fault, the A7+ flashes its status LEDs red while the standby LED flashes amber — see `troubleshooting.md`).

## What's protected vs not

| Device | On Furman chain? |
|---|---|
| Marantz SR5014 | yes |
| Emotiva BasX A7+ | yes (high-current bank — benefits from PF reservoir) |
| Sources (streamers, disc, etc.) | yes |
| BIC F-12 subwoofer | yes (verified 2026-04-26) — draws ~100 W AC nameplate, well within PF R 15 A capacity |
| Living Room KEF Q500 | n/a (passive speakers) |

## Things to log here

- Periodic line voltage readings from the PF R's front-panel display
- Any EVS shutdown events (over 140 V — overvoltage only; the unit auto-resets when line returns to safe range)
- Replacement of MOVs / surge cells (SMP is non-sacrificial — much longer lifetime than MOV-only units, but worth logging if it ever happens)

## Operational notes

- Inrush on power-up: the PF R's capacitor bank charges quickly but momentarily presents a high-current load; flipping its master switch may briefly dim other devices on the same circuit. Not damaging, just expected behavior.
- Voltage display drift: if you see chronic readings outside ~110-125 V, contact ComEd — chronic out-of-range voltage is utility-side, not gear-side. The PF R does not regulate, so the rack will see whatever the wall provides.

## Power conditioner history

- **Currently in service:** Furman Prestige Series P-1800 PF R (since 2026-04-25)
- **Previously briefly in service:** Furman P-1800 AR (replaced by PF R; AR is voltage-regulating but its series autoformer can theoretically restrict transient current to the A7+ — PF R chosen for transient delivery)
- **Earlier:** Furman M-8x2 (retired; passive surge + EMI/RFI filtering + 8-outlet distribution)
- See `maintenance-log.md` for swap dates.
