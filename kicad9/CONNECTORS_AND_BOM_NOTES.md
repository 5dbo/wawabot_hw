Component and connector pinout notes (initial)

Connectors and harness pinouts (proposed):
- POWER BUS (6-pin JST SH): BAT+, GND, 5V_BCK, 3V3, CHG_STAT, BAT_SENSE
- MAIN <-> MOTOR DRIVER (6-pin JST): M1_PWM, M1_DIR, M1_EN, M2_PWM, M2_DIR, FAULT
- MAIN <-> IR BOARD (6-pin JST): 3V3, GND, SCL, SDA, IRQ, ADC_IN
- MIC boards: 4-pin JST SH: 3.3V, GND, PDM_CLK, PDM_DATA
- CAMERA: 24-pin connector (DVP)
- DISPLAYS: SPI bus signals + CS1, CS2, DC, RST

BOM placeholders will be completed in the next commit with manufacturer part numbers and footprints.
