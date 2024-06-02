# ICS - Intercommunications System
The ICS provides normal, backup, or emergency communications between crewmembers. It also combines and amplifies audio signals received from other electronic receiving equipment (ECM, Sidewinder tone, IFF/SIF, radar altimeter, and voice radios, etc.). Identical ICS control panels are on the pilot and RIO left side consoles. The ICS consists of four amplifiers, two at each cockpit station, which permit duplex operation during normal operation. If one amplifier fails, it may be bypassed by selecting either the B/U (backup) or EMER (emergency) position on the ICS control panel. This permits continued ICS operation.

**Note:** If two amplifiers fail at the same station, intercommunication is impossible.

**Note 2:** By selecting EMER on the respective ICS control panel and using the other crewmember’s amplifier, you can listen in on audio normally only available at that station (like SW-tone or ALQ-126 PRF) but you lose the ability to control the volume of the audio you listen to.

The external interphone connection is in the nose-wheel well. When the pilot ICS switch is set to HOT MIC, ground personnel can communicate with the cockpit stations. In DCS, this works through selecting the ground crew communication menu in the DCS radio communication menu when activating ICS PTT.

| Control/Indicator                 | Function                                                                                                                                                                 |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Pilot Radio ICS button**        | ICS – Permits intercommunication when COLD MIC is selected on the function selector. Overrides UHF/VHF communications.<br>BOTH – Keys both radios for operation. Not functional in DCS.<br>UHF 1 – Keys ARC-159 radio for operation.<br>UHF 2 – Keys ARC-182 radio for operation. |
| **VOL control**                   | Controls intercommunication audio level at that cockpit station. Audio level at other stations is not affected.                                                           |
| **Amplifier selector**            | B/U – (Backup) used to bypass a fault amplifier and uses a backup output amplifier at own station.<br>NORM – (Normal) used when all amplifiers are functioning properly.<br>EMER – (Emergency) used to bypass faulty amplifier and makes use of input amplifier of the other station. No HOT MIC. |
| **CAUTION**                       | With the front cockpit amplifier selector switch in the EMER position, engine stall/overtemperature and Sidewinder tones will not be available to the pilot.              |
| **Function selector**             | RADIO OVERRIDE – Attenuates noncritical radio audio to emphasize intercommunication when urgent.<br>HOT MIC – Intercommunication without keying.<br>COLD MIC – Intercommunication only when the pilot actuates ICS keying switch on the inboard throttle or RIO actuates the keying switch on the left footrest. |
| **RIO’s ICS button (Left Foot Rest)** | Permits intercommunication if COLD MIC is selected on the function selector control. Overrides UHF communication.                                                         |
| **RIO’s MIC button (Right Foot Rest)** | Permits transmission of UHF 1 or UHF 2 radios as selected on the communications/TACAN command panel. Note that BOTH is not functional in DCS.                               |

> **Note**: The two RIO footpedals have axis bindings in DCS to allow sim rudder pedals to trigger these functions.
