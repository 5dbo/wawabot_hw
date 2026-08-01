Verification & Test Checklist (kicad9/TEST_CHECKLIST.md)

1) Pre-assembly checks
- Ensure footprints and polarity for BAT connector, ML307C daughterboard JST, and motor connectors are correct.
- Verify LMA3729T microphone orientation and acoustic port clearance.

2) First power (no battery)
- Apply 5V to charger input (USB or bench supply) through a current-limited supply (set to 1 A).
- Verify that CHG_STAT changes state, and that 3.3V regulator outputs 3.3V.
- Measure thermal behavior of BQ25895 (should remain cool with 1A input). Increase input current gradually if you have thermal monitoring.

3) Battery installation
- Install battery (2500 mAh) and verify BAT voltage and 3.3V rail under no-load conditions.
- Start charging and verify charging current; ensure cell temperature rises no more than a few degrees.

4) ML307C power test (daughterboard)
- Connect ML307C daughterboard via JST to main board. Apply power and verify 5V_BCK stays within 4.8-5.2V during brief transmit bursts.
- Verify external antenna via U.FL connection.

5) Motor test
- Connect one motor and run short PWM bursts at low duty cycle to confirm direction and current sense.
- Monitor TB6612FNG temperature; ensure it doesn't overheat.

6) Sensor & peripheral tests
- Power up ESP32-S3 and verify I2C scan for VL53L1X sensors through TCA9548A.
- Check OV2640 camera power & DVP signals, and initialize the camera from firmware.
- Verify SPI displays are reachable and can draw test patterns.
- Verify PDM microphones show expected audio frames on ESP32-S3 PDM input.
- Verify NFC read/write basic operation with PN532.

7) Final acceptance
- After bench tests, run endurance motor test and full functional test with camera, audio, 4G comms.
