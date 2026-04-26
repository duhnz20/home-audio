# Troubleshooting

Quick reference for common failure modes. Add new entries when you encounter and resolve issues.

## No sound from any main-room channel

Likely culprits in order:
1. SR5014 in wrong input or zone-routed away
2. Emotiva BasX A7+ powered off or in standby — **front-panel LED check:**
   - Standby LED **amber** = standby (not the cause unless trigger missing)
   - Standby LED **off** AND Status LEDs **off** = AC power off (rear panel switch off)
   - Standby LEDs **flashing amber** AND Status LEDs **flashing red** = Protect mode / fault — see "A7+ in Protect mode" below
3. **A7+ Auto-On is NOT supported on the A7+** (only A2+/A3+/A2L+ have it). The A7+ wakes only via a 12 VDC trigger (5–12 V) or the front-panel Standby button. If the trigger cable from the SR5014 is loose or the SR5014 itself is in standby, the A7+ stays in standby. Verify SR5014 Trigger Out is configured (Settings → General → Trigger Out) and the cable is seated.
4. Pre-out RCA cable loose at SR5014 or XLR end at amp
5. SR5014 muted or volume at -∞

## Some channels missing (e.g., center silent, surrounds dropped)

1. Check Audyssey speaker config didn't disable the channel
2. Check SR5014 surround mode — stereo / direct / pure-direct will mute non-front channels
3. Verify the matching Emotiva amp channel input is connected (back of Emotiva — channels labeled 1-7)
4. Inspect speaker wire at amp binding posts (loose strand → intermittent)

## Subwoofer silent

1. Sub power LED on? (Green = on, red = standby)
2. RCA cable from SR5014 sub-out → BIC F-12 **SUB IN** RCA jack seated? (Not the high-level inputs)
3. SR5014 menu → Settings → Audio → Manual Setup → Speaker Config → Subwoofer = "Yes"
4. Source content actually has LFE? (Stereo music in "Stereo" mode won't send to sub unless front speakers are set to "Small" with bass redirect)
5. **BIC F-12 Receiver Type switch on "Digital Receiver" position** (rear panel, beside SUB IN RCA). In "Pro Logic Receiver" mode the F-12 applies its own crossover knob *on top of* the SR5014 crossover, double-filtering the signal. For Audyssey-driven systems, **always** keep the switch on Digital Receiver — this disables the F-12's internal crossover and lets the AVR handle bass management.
6. BIC F-12 volume knob too low (audible distortion if too high — start at 12 o'clock and let Audyssey trim).
7. F-12 has gone into auto-standby — 15-20 min after no signal. Sending any LFE-containing content wakes it. If it's not waking, set the rear-panel **Power/Auto switch to ON** (vs AUTO) to bypass auto-standby for the run.

## Hum or buzz in speakers

1. Ground loop — try lifting one ground (the Furman Prestige Series P-1800 PF R's 3 isolated banks often help; try moving the offending source to a different bank)
2. Check that all gear is on the same Furman / circuit
3. Disconnect inputs one by one to isolate which source introduces the hum
4. RCA cable shielding — try a different sub cable; sub interconnects are notorious for picking up noise

## Zone 2 silent

1. SR5014 menu → Zone 2 ON?
2. Source assigned to Zone 2 (separate from Zone 1 source)
3. Zone 2 volume not at -∞
4. SR5014 Zone 2 pre-out RCA cable seated at SR5014 (the small RCA pair labeled ZONE2) and at Emotiva ch 6/7 inputs. Q500s are driven by the Emotiva, NOT the SR5014's internal Zone 2 amps.
5. Emotiva BasX A7+ powered on (same amp that drives main room — if main is silent too, this is the cause).
6. **Amp Assign clarification (correcting earlier note):** the SR5014's **Zone 2 pre-out is independent of the Amp Assign setting** — it is always live regardless of what Amp Assign is set to (manual p 40 footnote: "5.1-channel + 2-channel (Pre-out) ZONE2 — can be set in all Amp Assign modes"). A factory reset reverts Amp Assign to **"ZONE2 (Speaker out)"** as the default, NOT 7.1 internal amps. Either way, Zone 2 pre-out → Emotiva ch 6/7 → Q500 keeps working. If you want the SR5014's surplus internal amps to do anything else (Bi-Amp, Front B, Atmos heights, Surround Back), check Settings → General → Manual Setup → Amp Assign — but it doesn't affect Zone 2 audio.

## Audyssey calibration won't complete

1. Mic must be at SETUP MIC port, not regular input
2. Check ambient noise — calibration tones won't run if room is too noisy
3. Sub volume set too low or too high — Audyssey wants ~75 dB at the mic position; adjust sub gain if it complains

## TV (LG 75UN7370PUE) audio not coming through SR5014

For TV-app audio (Netflix, YouTube, broadcast tuner, etc.) to flow back to the speaker chain:

1. SR5014 → Settings → Video → HDMI Setup → **HDMI Control = ON** AND **ARC = ON** (manual p 165). For an eARC-capable TV, eARC overrides these settings, but keep them on for compatibility.
2. LG TV → Settings → Sound → Sound Out → **HDMI ARC** (or "Audio Out (Optical/HDMI ARC)" depending on firmware).
3. Verify the HDMI cable is connected to the SR5014's **MONITOR 1** output (only Monitor 1 carries the return path).
4. The cable must be a "High Speed HDMI Cable with Ethernet" (HEC-rated, manual p 54). The Ultra Clarity flat cable on this run is HEC-rated (confirmed 2026-04-26).
5. **Audio format expectation:** the UN7370 is ARC-only (verified 2026-04-26 — UN73 is 2020 entry-level LG, eARC arrived on NanoCell-80 and OLED that year). Standard ARC carries compressed Dolby Digital / DTS, which is what every TV app and the built-in tuner deliver. Atmos / DTS:X / lossless from streaming apps will not pass through — by design, not a fault. If you ever want this, you'd need to either route the streamer directly to the SR5014 (Apple TV is already wired this way for Atmos) or upgrade the TV.

## SR5014 won't power on

1. Furman Prestige Series P-1800 PF R powered? (Front display should show line voltage)
2. SR5014 standby LED behavior — solid red = standby OK; flashing = fault
3. If recently moved/reseated cables, verify HDMI cable not shorting power circuit (rare but happens)

## P-1800 PF R shows abnormal voltage or shuts down

- **>140 V**: EVS has tripped (over-voltage only — see `power.md`). Front-panel "Extreme Voltage" indicator lights, the relay opens, and all connected gear loses AC. Wait for line voltage to normalize; the unit auto-resets per the datasheet. If recurring, the cause is utility-side — call ComEd before assuming gear failure.
- **<90 V (but no shutdown)**: PF R has no undervoltage cutoff — it just passes whatever voltage is at the wall to the load. Marantz SR5014 and Emotiva A7+ both have their own internal under-voltage protection circuits; one of them will go into protect mode before the other lets damage happen.
- **Display reads <108 V or >132 V (but inside 90-139)**: line is in spec but trending unstable. PF R is passing it through unmodified (no AVR / autoformer). If chronic, contact ComEd, or consider an AVR-equipped Furman (P-1800 AR).
- **Constantly clamping / unusual noise from PF R itself**: possible internal protection degradation. SMP is non-sacrificial so this is rare — service required.

## A7+ in Protect mode (Status LEDs flashing red, Standby LED flashing amber)

Per Emotiva manual p 21:

- Switch the rear-panel AC Power switch OFF then ON to clear the fault.
- If the fault returns: look for a shorted speaker cable, damaged speaker, or a bad source connection (DC on the input from a dying source can trigger protect — try disconnecting input cables one at a time to isolate).
- The A7+ also protects against excessive operating temperature — if the rack is enclosed and the A7+ is running hot for hours, it may shut down for thermal reasons. Verify ventilation above and behind the unit; the Class A/B output stage generates real heat at sustained high power.
