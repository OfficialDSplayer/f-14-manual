## Communications Systems

### Antennas
Four VHF/UHF/L-band dual-blade antennas provide omnidirectional coverage for VHF/UHF voice, UHF data link, TACAN, and identification friend or foe/selective identification feature transponder (APX-72) operation. TACAN and VHF/UHF 2 voice communications use one set of antennas; UHF 1 voice communications, the data link, and IFF transponder use another set of antennas. Refer to the general arrangement illustration for antenna locations. The IFF interrogator (APX-76) antenna is an integral part of the AWG-9 WCS antenna.

Each individual system is connected to the appropriate portion of an upper or lower antenna through a coaxial switch and diplexer. The V/UHF 2 ANT switch on the RIO communication TACAN CMD panel must be used to select the upper or lower antenna manually; there is no automatic actuation function in these aircraft. The data link (DIL) antennas are similarly selected manually. Upper or lower antenna is selected by means of ANTENNA switches on the DATA LINK control panel. The UHF 1 voice communication ARC-159 antenna is shared with the DIL antenna system and is always on the opposite antenna from the one selected by the ANTENNA switch.

The upper V/UHF 2/TACAN antenna is the first one aft of the canopy on the turtleback, and the lower antenna is embedded in the bottom of the left ventral fin. Only one antenna is used at a time. Automatic switching between antennas prevents the loss of TACAN information. If a signal is lost or is too weak to hold receiver lockup, the TACAN automatically cycles between the two antennas every 6 seconds seeking a stronger signal.

During this cycling and search period, memory circuits retain range tracking for 8 to 12 seconds and bearing tracking for 8 seconds. The IFF antenna lobing switch is controlled by the IFF ANT switch on the RIO right outboard console. In AUTO, the lobing switch cycles the receiver-transmitter between the upper and lower antenna. In the LWR (lower) position, only the lower antenna is used to receive and transmit signals. The upper antenna pattern has a slight forward tilt; the lower pattern a slight aft tilt.

**Note:** In real life, it is often necessary to select LWR to improve ground station reception. However, due to the limitations of DCS, antenna switching is not modeled and thus not functional. The use of antennas is automated and/or neglected for the player. All radios and radio functions work through proper keying.

### Audio Warning Signals
Audio warning signals from the weapon system are available to either or both crewmen through the ICS. Each signal has a distinct tone. A visual display accompanies most audio signals so that the flight crew can expect the tone and interpret its meaning. Most audio signals may be attenuated or turned off if not required, allowing the flight crew to concentrate on more critical tones.

Critical warning tones cannot be attenuated by any mode of ICS operation. The table below provides a glossary of audio warning signals available within the aircraft weapon systems. Approximately 1 minute of warmup is required to achieve normal operating temperature.

| Tone                   | Position    | Controls                                      | Function            | Characteristics                          |
| ---------------------- | ----------- | --------------------------------------------- | ------------------- | ---------------------------------------- |
| **Sidewinder**         | Pilot       | Volume/TACAN Command Panel                    | Missile lock tone   | High frequency, increases with lockon indication. |
| **ALR-67**             | Pilot & RIO | Volume/TACAN Command Panel (pilot) & Radar Warning Receiver Panel (RIO) | Threat indication   | Low to high frequency, determined by threat level. |
| **AN/ALQ-126**         | RIO         | DECM Control Panel                            | Threat indication   | Raw PRF sound.                           |
| **Radar Altimeter**    | Pilot & RIO | Radar Altimeter Indicator (Pilot)             | Low altitude warning| 1 000 Hz tone, modulated at 2 pulses per second for 3 seconds. |
| **TACAN**              | Pilot & RIO | TACAN Control Panel                           | Station identification | TACAN station Morse code.              |
| **AN/ARC-159 (UHF 1)** | Pilot & RIO | UHF 1 Control Panel (Pilot) & RIO Communication/TACAN Command Panel | Own aircraft DF transmission | 1 020 Hz                                |
| **AN/ARC-182 (V/UHF 2)** | Pilot & RIO | V/UHF 2 Control Panel (RIO) & Volume/TACAN Command Panel (Pilot) | Other aircraft DF transmission | 1 020 Hz, Morse code or voice.          |
| **Engine Stall/Overtemperature** | Pilot       | None                                          | Engine stall detection & EGT overtemp warning | Modulated 320 Hz for 10 seconds or until fault is removed if before. |

### Pilot Volume/TACAN Command Panel
The Volume/TACAN command panel on the pilot left side console has three volume controls for regulating audio signals from the ALR-67, Sidewinder (SW), and V/UHF 2.

| Control/Indicator                  | Function                                |
| ---------------------------------- | --------------------------------------- |
| **ALR-67 Volume control**          | Controls volume for pilot ALR-67 indication. |
| **SW (Sidewinder) Volume control** | Controls volume of the pilot’s Sidewinder tone. |
| **V/UHF 2 Volume control**         | Controls volume of pilot audio from V/UHF 2 (AN/ARC-182). |
| **TACAN CMD control switch/indicator** | Controls and indicates crewmember in control of TACAN. |

### RIO Communication/TACAN Command Panel
Allows RIO to select either UHF 1 (AN/ARC-159), V/UHF 2 (AN/ARC-182), or both radios for transmitting.

**Note:** BOTH is not functional in DCS.

- The V/UHF 2 ANT switch allows the selection of upper or lower antenna to minimize interference between dual UHF or data link operation. Opposite antenna selection, frequency separation greater than 55 MHz, or turning one radio off is recommended. Additionally, the DATA LINK panel provides lower or upper antenna selection for UHF 1 and DIL operation.
- The TACAN CMD push buttons provide for the transfer of TACAN control functions between pilot and RIO. The crewmember (PLT or RIO) in control illuminates when selected.
- The UHF 1 VOL control allows the RIO to adjust the audio level of the ARC 159 UHF 1 radio. The KY MODE switch is operative only when the KY-58 is installed.

**Note:** The Heatblur F-14 version uses the KY-28 only.

| Control/Indicator                 | Function                           |
| --------------------------------- | ---------------------------------- |
| **XMTR SEL switch**               | Selects desired VHF/UHF radio for use.<br>UHF 1 - Selects ARC-159 UHF 1 radio.<br>V/UHF 2 - Selects ARC-182 VHF/UHF radio.<br>Both - Selects both radios. (Not functional in DCS) |
| **V/UHF 2 ANT switch**            | UPR - Selects upper antenna for V/UHF 2.<br>LWR - Selects lower antenna for V/UHF 2. |
| **TACAN CMD control switch/indicator** | Controls and indicates crewmember in control of TACAN. |
| **UHF 1 VOL control**             | Controls volume of RIO audio from UHF 1 (AN/ARC-159). |
| **KY MODE switch**                | Non-functional with KY-28.         |


#### Loading (saving) Preset Channel(s) on UHF 1 and V/UHF 2
1. MODE selection- T/R or T/R&G.
2. Frequency mode control - PRESET.
3. CHAN SEL switch- Select desired channel.
4. Frequency mode control- READ.
5. Frequency select switches - Slew to desired Frequency.
6. Frequency mode control - LOAD (frequency is stored in memory for the selected channel).
7. Frequency mode control- READ, Verify frequency display.
8. Repeat steps 2 through 7 for subsequent channels.

### AN/ARC-159 and AN/ARC-182 Remote Displays
Both the pilot and RIO have remote displays for the currently set channel or frequency of the radios. The pilot has remote displays for both UHF 1 and V/UHF 2 and the RIO only for UHF 1.

| Control/Indicator                  | Function                                   |
| ---------------------------------- | ------------------------------------------ |
| **UHF 1 Remote Channel/Frequency Indicator (Pilot)** | Displays a readout of the frequency or channel set for the UHF 1 radio.<br>TEST - Initiates test for the indicator, no fault resulting in 888.888 readout.<br>BRT - Controls display brightness. |
| **V/UHF 2 Remote Channel/Frequency Indicator (Pilot)** | Displays a readout of the frequency or channel set for the V/UHF 2 radio.<br>TEST - Initiates test for the indicator, no fault resulting in 888.888 readout.<br>BRT - Controls display brightness. |
| **UHF 1 Remote Channel/Frequency Indicator (RIO)** | Displays a readout of the frequency or channel set for the UHF 1 radio.<br>TEST - Initiates test for the indicator, no fault resulting in 888.888 readout.<br>BRT - Controls display brightness. |

### AN/ARA-50 UHF Automatic Direction Finder
The UHF automatic direction finder is used with the ARC-182 radio. ADF provides relative bearings to transmitting ground stations or other aircraft. It can receive signals on any 1 of 30 preset channels or on any manually set frequency in the 108 to 399.975 MHz range. The system has a line-of-sight range, varying with altitude.

The system requires a 5-minute warmup period. During the warmup time, failure indications should be disregarded. The system uses the AS-909/ARA-48 ADF antenna. Bearing to transmitting stations is displayed on the pilot/RIO BDHI (No. 1 needle), pilot HSD, and RIO multiple display indicator. The ADF signal is interrupted during voice UHF transmissions.
