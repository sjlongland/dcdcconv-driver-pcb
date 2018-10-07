# PWM MOSFET driver board

This is a LVDS-compatible MOSFET driver board for use with the [DC-DC converter
board](https://github.com/sjlongland/dcdcconv-controller-pcb).  It can drive
two N-Channel MOSFETs, either mounting the leads through the supplied
connection points `J3` and `J4` (suitable for TO-220 size MOSFETs) or via short
connection cables.  Due to parasitic inductance, it is best these be kept as
short as practical.

## Parts list

* U1: TI DS90C402 dual-channel LVDS receiver
* U2: TI UCC27212A-Q1 high/low side N-MOSFET driver
* U3: 74AHC04 (SOIC-14) hex inverting buffer (U1 when not connected to a LVDS
  source will drive both its outputs high, this inverts this to ensure both MOSFETs
  remain off in this condition.)
* C2: ≥100µF ≥10V electrolytic capacitor 6.3mm SMD (Bulk 5V rail decoupling)
* C1, C10: 100nF ≥10V ceramic capacitor 0805 SMD (local decoupling for U1, U3)
* C3: ≥100µF ≥20V electrolytic capacitor 6.3mm SMD (Bulk 12V rail decoupling)
* C4: 100nF ≥20V ceramic capacitor 0805 SMD (local decoupling for U2)
* C5: Bootstrap electrolyic capacitor for U2, refer to data sheet.  6.3mm SMD.
* J1: 6-pin 2.54mm "KK" connector (LVDS input and 5V rail)
* J2: 2-pin 2.54mm "KK" connector (12V rail)
* J3, J4: 3-pin 2.54mm "KK" connector or TO-220 size MOSFETs with heatsinks.
* (**FIT ONE ONLY**) C6, C7, C8, C9: ~100pF ≥20V ceramic capacitor 0805 (0V AC
  de-coupling to chassis.  Choose the one that best suits your mounting
  requirements.)
