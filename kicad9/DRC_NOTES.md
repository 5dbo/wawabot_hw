DRC and Layout Notes (kicad9/DRC_NOTES.md)

General
- KiCad constraints used: minimum trace width 0.25 mm for signals, 1.0 mm for power/5V traces, 1.5 mm for battery/motor high-current traces.
- Via: 0.6 mm diameter with 0.4 mm drill.
- Use 2 oz copper if motor currents approach >= 2 A sustained.

BQ25895 Thermal & Layout
- Place BQ25895 over a dedicated copper pour on the top layer with thermal vias (6-12 vias 0.3 - 0.4 mm drill) stitching to a bottom thermal plane.
- Provide 10 mm^2 of exposed copper pad area for thermal dissipation; add multiple vias under the IC's thermal pad.
- Place input bulk capacitor (100 uF low ESR) close to VIN pin. Place 1 uF ceramic decoupling directly at the IC.
- Respect datasheet layout for CC resistors and USB-C CC configuration.

ML307C Daughterboard & Antenna
- Daughterboard holds ML307C module and U.FL connector for external antenna. Place U.FL on the board edge and keep 8-12 mm circular keepout area on both sides for antenna clearance.
- Place a 220 uF low-ESR capacitor close to module VCC to support burst currents.

ESP32-S3 & RF
- Keep the ESP32 module's antenna area clear of copper and large ground pours for a 6-8 mm radius.
- Stitch ground plane at least 10 mm away from the antenna area with a clear keepout zone around the antenna trace.

Motor Driver (TB6612FNG)
- Place a 47 uF electrolytic capacitor near VM input for motor supply decoupling.
- Motor output traces: recommended minimum width 1.2 mm.
- Include STBY pull-ups and thermal relief for the chip.

Mic PCB (LMA3729T)
- Microphone acoustic port must be unobstructed; add a mechanical hole in the enclosure aligned with the mic port.
- Place decoupling 0.1 uF as close as possible to the mic VDD pin.

General EMI/ESD
- Add series resistors (22-47 ohm) on external IO lines (camera, UART, SPI) near the connector.
- Use ESD diodes on external connectors (U.FL, camera FFC, USB) to protect against transients.

Review & Test
- Run electrical DRC (connectivity and net class checks) before generating gerbers.
- Validate footprint library paths and update any custom footprints in the kicad9/footprints/ directory.
