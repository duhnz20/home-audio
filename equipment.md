# Equipment Inventory

## Main Room — Zone 1 (Home Theater, 5.1)

| Role | Make / Model | Notes |
|---|---|---|
| AVR / Processor | Marantz SR5014 | Pre-outs feeding external amp; **no internal amps used by any speaker** |
| External power amp | Emotiva BasX A7+ | 7-channel — drives ALL speakers in the house (5 main room + 2 Zone 2) |
| Front L/R | KEF R3 | Bookshelf, 3-way coaxial Uni-Q + bass driver |
| Center | KEF R2 Meta | R-series Meta center — 12th-gen Uni-Q + Metamaterial Absorption Technology (MAT). Voiced to match original R-series. |
| Surrounds (L/R) | KEF Q150 | Pair |
| Subwoofer | BIC America Formula F-12 | Powered, 12", connected via RCA from SR5014 sub out |
| Room correction | Audyssey (built into SR5014) | Run from MultEQ mic that ships with the AVR |

## Living Room — Zone 2

| Role | Make / Model | Notes |
|---|---|---|
| Source / control | Marantz SR5014 Zone 2 | Pre-out → Emotiva (NOT SR5014's internal amps) |
| Power amp channels | Emotiva BasX A7+ ch 6 & 7 | Same physical amp as main room; channel assignment via SR5014 Amp Assign menu |
| Speakers | KEF Q500 | Floorstanding stereo pair, front L/R only. Mounted on **IsoAcoustics Gaia III** isolation feet (decouples cabinet from floor; tightens bass and stereo image). |

## Channel allocation across the Emotiva BasX A7+

| Amp ch | Speaker | Zone |
|---|---|---|
| 1 | KEF R3 (Front L) | Main 1 |
| 2 | KEF R3 (Front R) | Main 1 |
| 3 | KEF R2 Meta (Center) | Main 1 |
| 4 | KEF Q150 (Surround L) | Main 1 |
| 5 | KEF Q150 (Surround R) | Main 1 |
| 6 | KEF Q500 (Living L) | Zone 2 |
| 7 | KEF Q500 (Living R) | Zone 2 |

All 7 amp channels in use. No surround-back / 7.1 capacity available without freeing one of these channels.

## Video — Sources & Displays

### Sources
| Role | Make / Model | Connection |
|---|---|---|
| Streamer | Apple TV 4K (2nd Gen) | HDMI → SR5014 **HDMI IN 5** ("Media Player"). Ultra Clarity CL3-rated flat HDMI 2.0 high-speed cable. |

### Displays
| Zone | Make / Model | Connection |
|---|---|---|
| Zone 1 (Main Room) | LG 75UN7370PUE (75" 4K UHD) | SR5014 **HDMI OUT Monitor 1 (eARC)** ↔ TV. Ultra Clarity CL3-rated flat HDMI 2.0 high-speed cable. eARC return brings TV-app and built-in-tuner audio back into the SR5014 → Emotiva → KEF chain. |
| Zone 2 (Living Room) | LG NanO75UQA (NanoCell 75 series) | SR5014 **HDMI OUT Monitor 2** → TV. Ultra Clarity CL3-rated flat HDMI 2.0 high-speed cable. Video-only (no return path). |

The SR5014's two HDMI outputs allow video to drive either or both TVs while audio stays on the receiver and feeds the speaker chain. Only Monitor 1 carries eARC; Monitor 2 is one-way video out.

## Power Protection / Conditioning

| Make / Model | Status | Role |
|---|---|---|
| Furman Prestige Series P-1800 PF R | **In service** | Power Factor Technology (45A peak current reservoir for transient delivery to A7+) + 3 isolated banks + SMP / EVS / LiFT + 6,500A surge max |

## Cabling

### Speaker wire (all speakers, both zones)
| Item | Spec |
|---|---|
| Wire | **GEARit 14 Gauge Speaker Wire (CCA, white)** — 14 AWG copper-clad aluminum |
| Termination | **WGGE WG-3333 24k Gold-Plated Speaker Banana Plugs (closed screw type)** on every speaker post end |

The same wire + plug combination is used for **all 7 amp-driven speakers** (KEF R3 L/R, R2 Meta center, Q150 surround L/R, Q500 Zone 2 L/R) at both the Emotiva BasX A7+ binding post end and the speaker binding post end.

**14 AWG sanity check:** 14 AWG handles ≤25-30 ft runs at 4-8 Ω without meaningful resistive loss; appropriate for the longest run in this house. CCA (vs pure copper) is ~70% the conductivity of OFC at the same gauge — gauge oversizing compensates. Banana plugs are closed-screw (mechanical, no solder) — strip wire, insert into screw barrel, tighten.

### Pre-out interconnects (SR5014 → Emotiva)
**Cable used for ALL 7 SR5014 → Emotiva runs (5.1 main + Zone 2 stereo):**
**Monoprice Premier Series XLR Male to RCA Male Cable** — 6 ft, black, E21 gold-plated connectors, 16 AWG shielded twisted pair, OFC braid conductors

| Pre-out | Count | SR5014 end | Emotiva end |
|---|---|---|---|
| 5.1 pre-outs (FL / FR / C / SL / SR) | 5 | RCA-male into SR5014 RCA pre-out jack | XLR-male into Emotiva balanced XLR input |
| Zone 2 pre-outs (L / R) | 2 | RCA-male into SR5014 Zone 2 RCA pre-out jack | XLR-male into Emotiva balanced XLR input |

**Topology note:** the SR5014 has unbalanced RCA pre-outs, the Emotiva BasX A7+ accepts both RCA and balanced XLR. These cables convert connector type (RCA → XLR) but the signal remains unbalanced — XLR is used purely for the locking connector and good contact at the amp end. True balanced operation would require an AVR with balanced XLR pre-outs (the SR5014 doesn't have them).

### Subwoofer interconnect (SR5014 sub/LFE pre-out → BIC F-12)
| Item | Spec |
|---|---|
| Cable | **Amazon Basics Subwoofer RCA Audio Cable** — gold-plated connectors (also marketed for S/PDIF / digital audio) |

### HDMI cabling
| Run | Cable |
|---|---|
| Apple TV → SR5014 HDMI IN 5 | Ultra Clarity CL3-rated flat HDMI 2.0 high-speed |
| SR5014 HDMI OUT Monitor 1 ↔ LG 75UN7370PUE (Zone 1, eARC) | Ultra Clarity CL3-rated flat HDMI 2.0 high-speed |
| SR5014 HDMI OUT Monitor 2 → LG NanO75UQA (Zone 2) | Ultra Clarity CL3-rated flat HDMI 2.0 high-speed |

## Speaker isolation / mounting

| Speaker | Mounting | Notes |
|---|---|---|
| KEF R3 (Front L/R) | **Rockville RHSB8 Adjustable Wall Mount Speaker Brackets** (pair) | Wall-mounted in main room; adjustable angle for toe-in |
| KEF R2 Meta (Center) | **3 × heavy-duty black metal floating shelf** under the Zone 1 LG 75UN7370PUE | Centered below the TV, three shelves distribute the speaker's weight |
| KEF Q150 (Surrounds) | **Vogel's VLB 200 Universal Speaker Wall Bracket** | Wall-mounted in main room |
| KEF Q500 (Zone 2 L/R) | **IsoAcoustics Gaia III** isolation feet | Decouples cabinet from floor — reduces structure-borne resonance, tightens bass definition and stereo image |
| BIC F-12 (Sub) | Sits on floor with **SVS SoundPath Subwoofer Isolation System** installed on the bottom | Decouples sub from floor — important in a high-rise / shared-wall context to reduce structure-borne bass transmission |

### Anti-slip / vibration damping
**Non-Slip Self-Adhesive Silicone Cuttable Furniture Pads** (5 × 40 in sheet, cuttable to size) installed on **all wall-bracketed speaker mounts** (R3 brackets, Q150 brackets, R2 Meta floating-shelf bracket contact points). Function: prevents speaker creep on bracket surfaces and adds a thin damping layer between speaker cabinet and metal mount.
