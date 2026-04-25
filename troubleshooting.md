# Troubleshooting

Quick reference for common failure modes. Add new entries when you encounter and resolve issues.

## No sound from any main-room channel

Likely culprits in order:
1. SR5014 in wrong input or zone-routed away
2. Emotiva BasX A7+ powered off or in standby (front panel LED check)
3. Pre-out RCA cable loose at SR5014 or amp end
4. SR5014 muted or volume at -∞

## Some channels missing (e.g., center silent, surrounds dropped)

1. Check Audyssey speaker config didn't disable the channel
2. Check SR5014 surround mode — stereo / direct / pure-direct will mute non-front channels
3. Verify the matching Emotiva amp channel input is connected (back of Emotiva — channels labeled 1-7)
4. Inspect speaker wire at amp binding posts (loose strand → intermittent)

## Subwoofer silent

1. Sub power LED on?
2. RCA cable from SR5014 sub-out → BIC F-12 RCA in seated?
3. SR5014 menu → Audyssey → speaker config → Subwoofer = "Yes"
4. Source content actually has LFE? (Stereo music routed to "Stereo" mode won't send to sub unless small-speaker bass redirect is on)
5. BIC F-12 crossover knob position (if set too low, may be crossing under what SR5014 sends)

## Hum or buzz in speakers

1. Ground loop — try lifting one ground (Furman P-1800 AR has filtered outlets that often help)
2. Check that all gear is on the same Furman / circuit
3. Disconnect inputs one by one to isolate which source introduces the hum
4. RCA cable shielding — try a different sub cable; sub interconnects are notorious for picking up noise

## Zone 2 silent

1. SR5014 menu → Zone 2 ON?
2. Source assigned to Zone 2 (separate from Zone 1 source)
3. Zone 2 volume not at -∞
4. SR5014 Zone 2 pre-out RCA cable seated at SR5014 and at Emotiva ch 6/7 inputs (Q500s are driven by the Emotiva, NOT the SR5014's internal Zone 2 amps)
5. Emotiva BasX A7+ powered on (the same amp that drives main room — if main is silent too, this is the cause)
6. SR5014 Amp Assign menu still set for "5ch + Zone 2 pre-out" topology (a factory reset would revert to 7.1 internal amps and break this path)

## Audyssey calibration won't complete

1. Mic must be at SETUP MIC port, not regular input
2. Check ambient noise — calibration tones won't run if room is too noisy
3. Sub volume set too low or too high — Audyssey wants ~75 dB at the mic position; adjust sub gain if it complains

## SR5014 won't power on

1. Furman P-1800 AR powered? (Front display should show line voltage)
2. Furman M-8x2 outlet for SR5014 not tripped?
3. SR5014 standby LED behavior — solid red = standby OK; flashing = fault
4. If recently moved/reseated cables, verify HDMI cable not shorting power circuit (rare but happens)

## P-1800 AR shows abnormal voltage

- **<108 V or >132 V**: line is genuinely unstable; AR is doing what it's supposed to. If it's chronic, contact ComEd.
- **Constantly clamping / making noise**: possible internal MOV degradation; consider service.
