# Specifications Quick Reference

Consolidated specs for every active component, pulled from the manufacturer manuals/spec sheets in [`manuals/`](manuals/). Use this for sanity checks (impedance / power / crossover compatibility) without opening individual PDFs. For full design rationale, see the manuals; for component roles, see [equipment.md](equipment.md).

## Speakers

| | KEF R3 (non-Meta, FL/FR) | KEF R2 Meta (Center) | KEF Q150 (Surround L/R) | KEF Q500 (Zone 2 L/R) |
|---|---|---|---|---|
| **Series / generation** | R Series, 03.2021 sheet | R Series Meta, 02.2023 sheet | Q Series 8th gen, 08.2019 | Q Series 7th gen (~2014) |
| **Design** | 3-way bass reflex | 3-way closed box | 2-way bass reflex | 2½-way bass reflex floorstander |
| **Drivers** | 25 mm Uni-Q HF + 125 mm MF + 165 mm LF | 25 mm Uni-Q HF (with MAT) + 125 mm MF + 2× 130 mm LF | 25 mm HF + 130 mm Uni-Q | 25 mm HF + 165 mm Uni-Q + 165 mm LF + 165 mm ABR |
| **Crossover** | 400 Hz, 2.9 kHz | 560 Hz, **2.5 kHz** | 2.5 kHz | 2.5 kHz |
| **Frequency range (-6 dB)** | 38 Hz – 50 kHz | 58 Hz – 50 kHz | 47 Hz – 50 kHz | ~42 Hz – 50 kHz |
| **Frequency response (±3 dB)** | 58 Hz – 28 kHz | 67 Hz – 28 kHz | 51 Hz – 28 kHz | ~48 Hz – 28 kHz |
| **Sensitivity (2.83 V / 1 m)** | 87 dB | 87 dB | 86 dB | 88 dB |
| **Nominal impedance** | **8 Ω** (min 3.2 Ω) | **4 Ω** (min 3.2 Ω) | **8 Ω** (min 3.7 Ω) | **8 Ω** |
| **Recommended amp power** | 15 – 180 W | 15 – 200 W | 10 – 100 W | 15 – 150 W |
| **Max output** | 110 dB | 110 dB | 108 dB | 108 dB |
| **Weight (each)** | 13.5 kg / 29.8 lbs | 15.4 kg / 34.0 lbs | 5.6 kg / 12.3 lbs | ~16.5 kg / ~36 lbs |

> **Front-stage impedance asymmetry:** R3 mains are nominal **8 Ω**, R2 Meta center is nominal **4 Ω**. The Emotiva BasX A7+ is rated to 4 Ω so this drives fine, but the center channel pulls roughly 2× the current of each main at the same voltage swing. Audyssey trims SPL automatically; the asymmetry only matters at extreme volume where the A7+'s shared linear supply would prefer a uniform load. No action needed in normal use — recorded for awareness when comparing future amp options.

## Subwoofer

**BIC America Formula F-12** (powered, vented, 12") — `bic-formula-f12-manual.pdf`

| Spec | Value |
|---|---|
| Driver | 12" injection-molded long-throw |
| Power | 475 W dynamic peak / 150 W RMS continuous |
| Max acoustic output | 115 dB SPL |
| Frequency response | 25 Hz – 200 Hz (±3 dB) |
| Crossover knob range | 40 – 180 Hz (bypassed in "Digital Receiver" mode — see below) |
| Phase | 0° / 180° switch |
| Auto-on idle | Standby after 15–20 min of no signal |
| AC | 120 V, 60 Hz, 100 W, fuse 5×20 mm 1.6 A 250 V |
| Weight | 19 kg / 42 lbs |

**Receiver Type switch (rear, key setting for this system):** must be on **"Digital Receiver"** position. This bypasses the F-12's internal crossover and lets the SR5014's Audyssey-derived crossover do all bass management. If the switch is on "Pro Logic Receiver", the F-12 applies its own knob crossover *on top of* the SR5014 crossover and the result is a low-passed double-filter that dulls the sub.

## Pre/Pro and Power Amplification

### Marantz SR5014 — AV pre/pro (used as pre/pro only, internal amps unused)
Source: `marantz-sr5014-owners-manual.pdf` (pp 275-279)

| Spec | Value |
|---|---|
| Internal amp (NOT used in this system) | 100 W × 7 ch @ 8 Ω, 20 Hz – 20 kHz, 0.08% THD |
| Speaker terminals | 4 – 16 Ω rated (n/a — not connected) |
| Pre-out connectors | 7.1 RCA (FL/FR/C/SL/SR/SBL/SBR) + 2× sub + Zone 2 L/R |
| Room correction | **Audyssey MultEQ XT** (not XT32; XT32 is on the SR6014/higher) |
| HDMI | 7 in, 2 out (Monitor 1 = ARC/eARC capable, Monitor 2 = video only) |
| Analog input sensitivity | 200 mV |
| Analog freq response | 10 Hz – 100 kHz (+1 / -3 dB, Direct mode) |
| Analog S/N | 100 dB IHF-A weighted |
| Power | AC 120 V, 60 Hz, 650 W draw, 0.2 W standby |
| Operating temp | 5 – 35 °C / 41 – 95 °F |
| Dimensions | 17 3/8" × 6 3/8" × 13 3/4" (440 × 161 × 348 mm) with feet |
| Weight | 10.1 kg / 22.25 lbs |

### Emotiva BasX A7+ — 7-channel power amp (drives ALL speakers)
Source: `emotiva-basx-a7plus-manual.pdf` (pp 17-19)

| Spec | Value |
|---|---|
| Topology | Class A/B, fully discrete short signal path, heavy-duty linear supply with toroidal transformer |
| Power, all 7 channels driven | **90 W RMS / channel @ 8 Ω**, 20 Hz – 20 kHz, THD <0.02% |
| Power, all 7 channels driven (4 Ω, 1 kHz) | 125 W RMS / channel, THD <1% |
| Input sensitivity (8 Ω rated) | 1.2 V |
| Voltage gain | 29 dB |
| Power bandwidth | 20 Hz – 20 kHz (±0.07 dB) |
| Broadband freq response | 5 Hz – 80 kHz (+0 / -1.8 dB) |
| THD+N | <0.02% A-wt @ rated, 1 kHz, 8 Ω |
| S/N | >112 dB ref rated power; >95 dB ref 1 W (A-wt) |
| Min load | 4 Ω (one 4-Ω load OR two paralleled 8-Ω loads per channel) |
| Damping factor | >500 @ 8 Ω |
| Inputs | RCA + XLR per channel — **summed at the input** (do not connect both) |
| Input impedance | 27 kΩ |
| Trigger | In: 5–12 V (AC or DC); Out: 12 VDC up to 120 mA |
| Auto-On | **NOT available on the A7+** (Auto-On is A2+/A3+/A2L+ only) — runs from 12 V trigger or front-panel standby button |
| AC | 115 V or 230 V auto-detect, 50/60 Hz, IEC C13 inlet |
| Dimensions | 17"W × 4¼"H × 15½"D (incl. feet) |
| Weight | 28 lbs / 12.7 kg |
| Heat | Class A/B output stages generate substantial heat at sustained high power — leave open clearance above and behind |

> **Why "all channels driven" matters for sizing:** the 90 W/ch all-driven figure is the conservative number relevant to this system. KEF speaker recommended power ranges (R3 15–180 W, R2 Meta 15–200 W, Q150 10–100 W, Q500 15–150 W) all comfortably bracket 90 W — the A7+ has plenty of headroom across the entire stage with no channel starved.

## Power Conditioning

**Furman Prestige Series P-1800 PF R** — `furman-p1800-pfr-datasheet.pdf` + `furman-p1800-pfr-owners-manual.pdf`

| Spec | Value |
|---|---|
| Maximum current | 15 A (high-inrush magnetic circuit breaker) |
| Operating voltage range | **90 – 139 VAC** (passes through unmodified — no AVR) |
| Extreme Voltage Shutdown (EVS) | **Trips at >140 VAC nominal — overvoltage only**, not undervoltage |
| Spike protection mode | Line-to-Neutral (zero ground leakage) |
| Spike clamp | 188 VAC peak @ 3,000 A (initial), 6,500 A max, 1 ns response |
| Surge technology | SMP (Series Multi-Stage) — non-sacrificial, survives multiple 6 kV / 3 kA pulses |
| Noise attenuation (LiFT) | 30 dB @ 2 kHz · 40 dB @ 10 kHz · 50 dB @ 20 kHz · 70 dB @ 100 kHz |
| Power Factor Technology | 45 A peak instantaneous-current reservoir for high-current amplification |
| Outlets | 9 total (8 rear: 3 transformer-spaced "Secure Strap" + 5 standard high-current; 1 front USB convenience) |
| Outlet banks | Isolated (digital / analog / high-current) |
| Reactive power | 460 VA |
| Power consumption (no load) | 8 W |
| Line cord | Captive 10 ft, 14 AWG/3, NEMA 5-15 plug |
| BNC rear-rack lamp | 12 VAC 500 mA max (lamp not included) |
| Dimensions | 19" W × 12" D × 1.75" H (1U rack) |
| Weight | 13 lbs |

> **Correction vs prior docs:** EVS is **overvoltage-only** (trips above 140 VAC). The datasheet does not specify an undervoltage cutoff — earlier notes implying "EVS disconnects below 90 V" were incorrect. The 90 V figure is the lower bound of the **operating** voltage range; below it, performance is undefined (the unit may chatter or the front-panel voltmeter may report low) but EVS itself watches only for over-voltage.

## Mounting / Isolation Load Capacities

| Hardware | Load rating | Speaker(s) | Speaker weight (each) | Margin |
|---|---|---|---|---|
| Rockville RHSB8 (pair, swivel wall bracket) | ~30 lbs / bracket per published spec | KEF R3 | 29.8 lbs | **At upper limit — verify lag-bolt is into stud, not just drywall anchor** |
| 3× heavy-duty floating shelf brackets (R2 Meta) | Manufacturer-rated per single bracket; 3× shelves distribute the load | KEF R2 Meta | 34 lbs total | Comfortable with 3 brackets |
| Vogel's VLB 200 (each) | 20 kg / 44 lbs per bracket | KEF Q150 | 12.3 lbs | ~3.5× margin |
| IsoAcoustics Gaia III (set of 4) | 70 lbs / 32 kg per speaker (set) | KEF Q500 | ~36 lbs | ~2× margin (within spec) |
| SVS SoundPath sub isolation (4-foot kit) | Universal screw-in (¼-20/M6/M8); no published max — designed for cabinet subs in the 50–150 lb class | BIC F-12 | 42 lbs | Comfortable |

> **R3 / RHSB8 watchpoint:** the R3 at 29.8 lbs each is right at the published limit of an RHSB8-class swivel bracket. The bracket must be lag-bolted into a wood stud, not just drywall anchors, for the static load AND for the dynamic load at high SPL (cabinet vibration adds a transient component the static rating doesn't cover). If the brackets ever feel any droop or wall-plate movement, that's the failure mode to act on first.

## Cables (electrical only — see equipment.md for full inventory)

| Run | Cable | Notes |
|---|---|---|
| Speaker (all 7 amp-driven) | GEARit 14 AWG CCA + WGGE WG-3333 closed-screw banana plugs | 14 AWG handles 25–30 ft @ 4–8 Ω with negligible resistive loss; CCA is ~70% conductivity of pure copper — gauge oversizing compensates |
| SR5014 → Emotiva (5.1 + Z2 = 7 runs) | Monoprice Premier 6 ft RCA-M to XLR-M, 16 AWG OFC twisted pair | RCA pre-out at SR5014 → XLR at A7+; signal stays unbalanced (true balanced needs balanced AVR pre-outs) |
| SR5014 sub/LFE → BIC F-12 | Amazon Basics subwoofer RCA | Single mono RCA |
| HDMI runs (×3) | Ultra Clarity CL3-rated flat HDMI 2.0 high-speed | CL3 = in-wall safety rated. For ARC/eARC, **must be a "High Speed HDMI Cable with Ethernet"** (HEC) per Marantz manual p 54 |

## Source PDFs

All specs pulled from manuals in [`manuals/`](manuals/). For the source URLs and download instructions, see [manuals.md](manuals.md).
