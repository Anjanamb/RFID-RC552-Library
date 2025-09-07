# MFRC522 (RC522) — Altium Library

>Altium Designer library for the NXP MFRC522 13.56 MHz RFID reader IC (commonly called RC522). This repo includes schematic symbol(s), PCB footprint(s), an Altium Library Package, a compiled Integrated Library, and 3D models (STEP/SolidWorks).

---

## What’s in this repo
```
MFRC522-Altium-Library
├── Footprint/                          # (optional) extra or intermediate footprint sources
│   ├── History/                        # Altium auto-generated library history
│   └── Project Outputs for RFID/       # Altium compiler outputs (keep if you want local artifacts)
│       ├── RFID.IntLib                 # Compiled Integrated Library (ready to install)
│       ├── RFID.LibPkg                 # Altium Library Package (source project)
│       ├── RFID_RC552.PcbLib           # PCB footprint library  
│       └── RFID_RC552.SchLib           # Schematic symbol library 
├── My design/
│   ├── Part1.SLDPRT
│   ├── Part1.STEP
│   ├── Part2.SLDPRT
│   └── Part2.STEP                      # 3D sources/STEP exports used by the footprint
└── RC522_datasheet.pdf                 # NXP MFRC522 datasheet
```

---

## Quick start (Altium Designer)

Option A — Use the compiled Integrated Library (fastest)
1. In Altium: View > Panels > Components (or Libraries) > Installed > Install From File.
2. Select `RFID.IntLib`.
3. Place > Component and search for MFRC522/RC522.

Option B — Build from the Library Package (recommended for edits)
1. Open `RFID.LibPkg` in Altium.
2. Review symbol–footprint linking and parameters.
3. Right‑click the library project > Compile Integrated Library to generate a fresh `.IntLib`.

Option C — Use the raw libraries
1. Add `RFID_RC552.SchLib` and `RFID_RC552.PcbLib` to your project (or install via the Libraries/Components panel).
2. Place the component from the library.

---

## 3D model usage

- STEP files are under `My design/`. In PCB Library editor:
  1. Open `RFID_RC552.PcbLib` (or the renamed `MFRC522.PcbLib`).
  2. Select the footprint > Place > 3D Body > Generic 3D Model and choose the appropriate `.STEP`.
  3. Adjust rotation/offset to align with pads; verify in 3D (press 3 in PCB).

SolidWorks files (`.SLDPRT`/`.SLDASM`) are source models; export STEP if you modify them and re‑link in the footprint.

---

## Verification checklist (before manufacturing)

- Pin mapping: symbol pin numbers match footprint pad numbers.
- Package/mechanical: pad sizes, pitch, body outline match the selected package in the datasheet.
- Solder/paste/mask: clearances set per your fab’s rules.
- 3D alignment: STEP model aligns with footprint origin and pads.
- Electrical notes: power (3.3 V typical), reset/IRQ pins, and interface pins labeled and documented.

---

## Contributing

- Issues/PRs welcome for footprint/symbol fixes or improvements.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

## References

- Datasheet: see `RC522_datasheet.pdf` (MFRC522, NXP). Prefer the latest revision from NXP if updating.

---
