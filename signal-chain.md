# Signal Chain

## Zone 1 — Main Room

```
                 ┌─────────────────────────────────────────────┐
 HDMI sources ──►│                                             │
 Streamers   ──►│         Marantz SR5014 AV Receiver          │
 Disc player ──►│  (decoding, room correction, switching)     │
                 │                                             │
                 └────┬─────────────────────────┬─────────────┘
                      │ 7.1 pre-outs (RCA)      │ Sub/LFE pre-out
                      ▼                          ▼
            ┌──────────────────────┐   ┌────────────────────┐
            │ Emotiva BasX A7+     │   │ BIC America F-12   │
            │ 7-channel power amp  │   │ Powered subwoofer  │
            └────────┬─────────────┘   └────────────────────┘
                     │
        ┌────────────┼────────────┬─────────────┐
        ▼            ▼            ▼             ▼
   KEF R3 (FL)  KEF R3 (FR)  KEF Q250C    4× KEF Q150
                              (Center)    (Side + Rear surrounds)
```

**Notes**
- SR5014 internal amps **do not** drive any main-room speaker — all amplification goes through the Emotiva BasX A7+.
- Sub is connected to the SR5014's dedicated LFE/sub pre-out, NOT to the Emotiva (which has no sub output).
- Audyssey runs at the SR5014; corrections apply to the pre-out signal *before* it hits the Emotiva.

## Zone 2 — Living Room

```
 sources ──► Marantz SR5014 ─── Zone 2 amp section ───► KEF Q500 (L/R)
                                  (internal amp,
                                   not the Emotiva)
```

**Notes**
- Zone 2 is stereo only.
- Driven by the SR5014's internal Zone 2 amplifier — Emotiva is not in this path.
- Source can be any input the SR5014 can switch into Zone 2 (analog inputs, network audio).

## Power Chain

```
 Wall outlet
    │
    ▼
 Furman P-1800 AR  (voltage regulation + conditioning + surge)
    │
    ▼
 Furman M-8x2      (rack distribution + surge)
    │
    ├─► Marantz SR5014
    ├─► Emotiva BasX A7+
    └─► Source components
```

The BIC F-12 sub typically plugs into wall (or its own surge strip) due to current draw — confirm whether it's on the Furman chain or separate.
