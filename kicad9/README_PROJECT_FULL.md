README: How to open and use this KiCad project

1. Clone repository and checkout branch kicad9-initial
   git clone https://github.com/5dbo/wawabot_hw.git
   cd wawabot_hw
   git checkout kicad9-initial

2. Open KiCad 9 and open the project file: kicad9/wawabot.kicad_pro

3. The current commit contains detailed textual schematic and PCB descriptions for each board. These are intended to be converted into KiCad schematic sheets and PCB layouts by copying the described components and nets into KiCad schematic editor (they are human-readable canonical designs). In follow-up commits I will provide native .kicad_sch XML-format files and .kicad_pcb files if you want fully-importable files.

Notes & Warnings:
- The TP4056-based charger is limited to ~1A in practice; the user's 2.5A desired charging requires a different charger IC. Please follow the BOM notes and consider using a BQ25895 or similar if fast charging at 2.5A is required.
- Ensure ML307C power rail and decoupling are sized for cellular bursts (2-3A). Use the 5V boost with large electrolytic capacitor near the module.
- Verify antenna keepouts and RF layout guidelines for Wi-Fi/BT and 4G.

If you want, I can now proceed to convert these textual designs into native KiCad 9 .kicad_sch and .kicad_pcb XML files and push them as a follow-up commit. Reply "Generate native KiCad files" to continue.