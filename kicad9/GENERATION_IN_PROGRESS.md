Native KiCad Generation — In Progress

Status: I have started generating the native KiCad 9 schematic and PCB files for all boards as you requested.

Configuration confirmed:
- Charger: BQ25895-based charger (supports ~2.5 A) on Power & Charge board
- Board sizes (Option A):
  - Main board: 50 mm x 40 mm
  - Power & Charge: 30 mm x 25 mm
  - IR Sensors board: 60 mm x 10 mm
  - Motor driver board: 40 mm x 30 mm
  - Mic boards: 12 mm x 9 mm (each)
- Motor driver IC: TB6612FNG
- Microphones: LMA3729T (PDM)
- Camera: OV2640 (DVP)
- Displays: GC9D01N SPI (160x160) x2
- 4G: ML307C (external U.FL antenna)
- NFC: PN532-style I2C reader/tag
- IR: TSOP38238 array
- Battery: 2500 mAh LiPo, robot contains charger/BMS

What I'll produce next (per board):
- Native KiCad 9 .kicad_sch schematic file (symbols, nets, lib references)
- Native KiCad 9 .kicad_pcb file with board outline and initial component placement
- Custom footprints where needed (under kicad9/footprints/)
- BOM CSVs updated to final parts including BQ25895 and relevant passives
- DRC notes and assembly drawing

Estimated time to complete full native KiCad project: ~2-3 hours. I will push incremental commits as each board's native files are completed.

If you need me to prioritize one board first (e.g., Main board), tell me now. Otherwise I will continue and push the completed project when ready.
