# Audyssey Calibration

## Runs

| Date | Trigger | Mic positions | Notes / channel trims | Crossover settings |
|---|---|---|---|---|
| | | | | |

## Procedure (Marantz SR5014 / Audyssey MultEQ XT32)

1. Place primary listening position mic stand (tripod) at ear height of main seat.
2. Connect MultEQ mic to SR5014 SETUP MIC input.
3. SR5014 menu → Audio → Audyssey → Setup.
4. Run 6-8 mic positions across the seating area.
5. After completion, verify in Audyssey menu:
   - All speakers detected and assigned correctly (FL/FR/C/SL/SR/SBL/SBR/SW)
   - Speaker distances reasonable (compare to tape measure)
   - Subwoofer crossover set (default 80 Hz — KEF R3s can go lower if desired)
   - Channel level trims within ±6 dB of 0
6. Save.

## Reference settings to record after each run

- LFE crossover (typically 80 Hz)
- Front L/R crossover (small vs large; R3s are usually set to "small" with 60-80 Hz crossover for best blend with sub)
- Center crossover (Q250C → 80 Hz)
- Surround crossover (Q150 → 100-120 Hz typical)
- Subwoofer level trim
- Audyssey Dynamic EQ on/off
- Audyssey Dynamic Volume setting

## Things to log

Each run should append a row above with:
- Why you re-ran (new speaker, room change, gear swap)
- The mic positions used
- The post-cal channel trims (so you can spot drift over time)
- Any "speaker too loud / too quiet" warnings Audyssey reported

## Known issues

- Audyssey calibration is tied to the Marantz SR5014. **If the AVR is replaced, recalibration is mandatory** — settings do not export to other brands.
- The Audyssey app (paid) allows tweaking the curve and exporting/importing — worth considering if dialing in detailed EQ.
