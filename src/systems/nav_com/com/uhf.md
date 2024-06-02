# AN/ARC-159 (UHF 1) Radio

The UHF 1 (ARC-159) radio provides air-to-air and air-to-surface voice communications. Radio frequency range extends from 225.000 to 399.975 MHz. The equipment allows AM mode transmission and reception on any of the 20 preset channels and a guard channel (243.000 MHz). Guard frequency may be monitored simultaneously with any other frequency selected. The ARC-159 has a possible 7,000 frequencies available by manually tuning in 25-kHz steps. The ARC-159 radio is a solid-state, self-contained unit with a minimum RF output of 10 watts. All controls for operation of the radio are on the front panel of the radio. The radio is located on the pilot left console.

**Note:** The UHF 1 (ARC-159) ADF position is non-functional in the modeled version of the F-14; use the DF mode of V/UHF 2 ARC-182.

| Control/Indicator                  | Function                                                |
| ---------------------------------- | ------------------------------------------------------- |
| **VOL control**                    | Controls volume of pilot audio for UHF 1.               |
| **SQL (Squelch) switch**           | On/off control for radio squelch (noise-blanking when carrier is not present). |
| **Frequency Tuning switches**      | Four frequency tuning switches are used to tune the transceiver when the mode selector switch is set to MANUAL. The left switch controls the hundreds and tens digits, the second switch controls units, the third switch controls tenths, and the right switch controls hundredths and thousandths. Forward deflection of the switch increases the numeric reading, and aft deflection decreases the numeric reading. |
| **FREQ/(CHAN) display**            | Displays frequency when the mode selector switch is in MANUAL and displays UHF channel when the mode switch is in PRESET. |
| **READ switch**                    | Deflection of the switch causes the frequency display to show the preset channel frequency. |
| **BRT/TEST control**               | Controls brightness of radio FREQ/(CHAN) display. Turn past max to show 888.888 test display. |
| **LOAD button**                    | Depressing button saves displayed frequency to the selected preset channel. |
| **Function selector**              | ADF – The UHF 1 ARC-159 ADF function is not functional; use the DF mode of the V/UHF 2 ARC-182.<br>BOTH – Energizes both the main transceiver and the guard receiver.<br>MAIN – Main transceiver is energized permitting normal transmission and reception. Receive or transmit function is selected by the microphone push-to-talk switch.<br>OFF – Secures UHF 1 radio. |
| **CHAN SEL control**               | Selects one of 20 preset frequency channels to use when the tuning selector switch is set to PRESET. |
| **Frequency Chart**                | Used to record preset channel frequencies. Frequencies preset in the mission editor will be automatically displayed here in DCS. |
| **Mode Selector switch**           | GUARD – Main transceiver is energized and shifted to guard frequency of 243.0 MHz permitting transmission and reception. In this position, both preset and manual frequency selections are not available.<br>MANUAL – Frequency tuning controls are used to tune the main transceiver to any frequency (7,000 available) within the range of the set. The frequency selected is displayed in the readout window. In this position, PRESET selections are not available.<br>PRESET – Used to tune the transceiver to any of 20 preset channels using the PRESET channel selector. The selected channel is displayed in the readout window. |
| **TONE button**                    | Depressing button causes a steady tone (1 020 Hz) to be transmitted on the frequency or channel selected. |

**Note:** UHF communication interference with the D/L may cause the TILT light to illuminate and the autopilot ACL or VEC/PCD mode to disengage. Data link interference with the UHF radios may cause audible chirping at the D/L message reply rate. Although antenna switching is not implemented in DCS, it is still recommended to use a frequency separation greater than 55 MHz, and if necessary along with turning UHF 1 or V/UHF 2 radio OFF to avoid mutual interference between UHF communications.

**Note 2:** Transmissions on both UHF 1 and V/UHF 2 radios, while operating on the same frequency, may result in a squeal. This feedback is a normal condition caused by RF interaction between the two radios operating on the same frequency in close proximity to each other.

