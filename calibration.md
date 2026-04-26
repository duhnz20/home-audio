# Audyssey Calibration

The SR5014 ships with **Audyssey MultEQ XT** (not XT32 — XT32 is on the SR6014/higher). All references in this doc are to MultEQ XT specifically. Source: `manuals/marantz-sr5014-owners-manual.pdf` pp 157-160 (Audyssey settings) + pp 179-188 (Setup procedure).

## Runs

| Date | Trigger | Mic positions | Channel trims (FL / FR / C / SL / SR / Sub) | Crossovers (C / FL/FR / Surr / Sub) | Dynamic EQ | Dynamic Volume | Notes |
|---|---|---|---|---|---|---|---|
| | | | | | | | |

## Procedure (SR5014 / Audyssey MultEQ XT)

### Pre-cal: subwoofer prep (BIC F-12)

The SR5014 manual (p 181) describes two paths depending on whether the sub has a "direct mode":

| Sub feature | Setting |
|---|---|
| If sub has a **direct mode** | Set direct mode ON; disables internal volume + crossover so AVR drives entirely. |
| If sub has **no direct mode** (BIC F-12) | Volume knob to 12 o'clock position; Crossover knob to maximum; **Receiver Type switch to "Digital Receiver"** (this is the F-12's equivalent of direct mode — bypasses internal crossover and lets SR5014 do bass management); Phase 0°; Auto-On to ON. |

### Mic placement

- Connect the supplied Audyssey calibration mic to the **SETUP MIC** jack on the SR5014 front panel (under the flap).
- Mount the mic on a tripod (or its supplied stand) at the **ear height of the primary listening seat**. Tip pointing at the ceiling.
- Keep the mic at least 50 cm (20 in) clear of any wall during measurement.
- 6–8 measurement positions across the seating area; subsequent positions within 60 cm (2 ft) of the first.
- Don't operate volume during measurement — it cancels the run.

### Run

1. SR5014 menu → **Settings → Audio → Audyssey Setup**.
2. Optional pre-run choices (manual p 182):
   - **Amp Assign** — only relevant if SR5014 internal amp is repurposed for surround back / heights / Bi-Amp. Not in use in this system; leave alone.
   - **Channel Select** — skip channels not in use (e.g., surround back) to shorten measurement time.
   - **Dolby Speaker Setup** — only if Amp Assign is set to "Front Dolby" or "Surround Dolby" (Atmos-enabled speakers). N/A here.
3. Select **Start** → **Begin Test**.
4. Move mic to position 2-8 between tone bursts when prompted.
5. After all positions, choose **Continue** to analyze.
6. Audyssey then asks about **Dynamic EQ** (recommended ON) and **Dynamic Volume** (Off / Light / Medium / Heavy).
7. Unplug the mic when prompted.
8. Verify via **Details** screen (manual p 186): all expected speakers detected, distances reasonable, sub level within ±3 dB of 0.

### Things to record after each run (this is what you fill into the table above)

| Setting | Where to find it |
|---|---|
| Per-channel level trims (FL/FR/C/SL/SR/SBL/SBR/Sub) | Settings → Audio → Manual Setup → **Levels** |
| Per-channel distances | Settings → Audio → Manual Setup → **Distances** |
| Per-channel crossovers | Settings → Audio → Manual Setup → **Crossovers** |
| Dynamic EQ on/off | Settings → Audio → Audyssey → **Dynamic EQ** |
| Dynamic Volume | Settings → Audio → Audyssey → **Dynamic Volume** |
| Reference Level Offset | Settings → Audio → Audyssey → **Reference Level Offset** (0 dB film / 5 dB classical / 10 dB jazz, TV / 15 dB pop, rock) |

## Audyssey post-run settings menu — what each does

Source: SR5014 manual pp 157-160.

### MultEQ XT mode (Settings → Audio → Audyssey → MultEQ XT)

| Mode | Behavior | When to use |
|---|---|---|
| **Reference** (default) | Calibrated curve with slight HF roll-off | Film / general use |
| L/R Bypass | Reference curve everywhere except FL/FR | If front L/R already sound good without EQ but center + surrounds need help |
| Flat | Calibrated, no HF roll-off | Small rooms / nearfield |
| Off | No correction | A/B comparison, or if Audyssey is making things worse |

### Dynamic EQ (Settings → Audio → Audyssey → Dynamic EQ)

Compensates for human hearing's reduced bass + treble sensitivity at low volumes. **Recommended ON** for late-night low-volume listening — without it, dialogue gets thin and bass disappears as you turn down. Turning Dynamic EQ on disables manual Tone control (manual p 158).

### Reference Level Offset (Settings → Audio → Audyssey → Reference Level Offset)

Audyssey calibrates to the standard film mix reference (0 dB = "reference level" film, MV -10). Music is mixed hotter; this offset compensates so Dynamic EQ behaves correctly at quieter listening levels.

| Offset | Use case |
|---|---|
| 0 dB (default) | Film / movies |
| 5 dB | Wide-dynamic-range music (classical) |
| 10 dB | Jazz, TV content (typically mixed 10 dB below film reference) |
| 15 dB | Pop / rock at high listening levels (compressed dynamic range) |

Only takes effect when Dynamic EQ is ON.

### Dynamic Volume (Settings → Audio → Audyssey → Dynamic Volume)

Auto-leveler that smooths out commercials, channel changes, etc. Heavy / Medium / Light / Off (default = Off; Audyssey sets it to Medium if you said yes during the run, manual p 159).

Don't run Dynamic Volume Heavy for music — it kills micro-dynamics. Light or Medium for TV viewing where ad-break loudness is annoying; Off for critical listening.

### Graphic EQ (Settings → Audio → Graphic EQ)

Independent of MultEQ XT — must turn MultEQ XT **Off** to access Graphic EQ. 9 bands (63/125/250/500/1k/2k/4k/8k/16k Hz), -20 to +6 dB, settable per speaker / per L+R / globally. Also has a "Curve Copy" option that imports the Flat-mode Audyssey curve as a starting point for manual tweaking.

## Recovering / restoring a previous run

The **Restore...** option in the Audyssey Setup menu (manual p 188) reverts to the last successful measurement run, undoing any subsequent manual changes you made in Levels / Distances / Crossovers. Useful if a manual tweak made things worse.

## Known issues

- Audyssey calibration is tied to the Marantz SR5014. **If the AVR is replaced, recalibration is mandatory** — Audyssey settings do not export to other brands or to non-Audyssey rooms-correction (Dirac, etc.).
- The paid **Audyssey MultEQ Editor app** (iOS / Android) lets you tweak the target curve, set per-speaker trim points, and import/export — well worth the $20 if you're dialing in a stubborn room. Works with the SR5014's MultEQ XT.
- **Do not change speaker connections or sub volume after a run** (manual p 186 explicit warning). If you swap a speaker (e.g., the Q250C → R2 Meta upgrade on 2026-04-24), recalibration is mandatory — the old curve is wrong for the new speaker's sensitivity / impedance / distortion profile.
- Subwoofer measured-distance often reads farther than tape-measured distance because powered subs add electrical delay. Don't manually "correct" this — Audyssey accounts for it (manual p 186 note).
- Sub level too low / too high during the run: Audyssey wants ~75 dB at the mic position. If it complains, adjust the BIC F-12 volume knob and re-run.

## Common error messages (manual p 187)

| Error | Cause | Fix |
|---|---|---|
| "No speakers found" | Mic not connected to SETUP MIC jack, or speakers disconnected | Verify mic in correct jack; check speaker wires at amp end |
| "Ambient noise too high or level too low" | Room noise or speaker too quiet | Quiet the room (HVAC off, phones away, no kitchen activity); raise sub volume if it complains specifically about LF |
| "Front R: None" / similar | Audyssey can't detect that speaker | Speaker wire loose or amp channel off |
| "Front R: Phase" | Speaker wired with reversed polarity | Check +/- on speaker wire. If you're sure it's correct (e.g., a known-good speaker), Audyssey lets you press ▷ to "Ignore" |
