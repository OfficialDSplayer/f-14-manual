# Electronic Countermeasures - AN/ALQ-100 & 126 DECM (Defensive Electronic CounterMeasures)

The AN/ALQ-100 and 126 jammers are designed to detect radar threats, analyze them, select the optimum countermeasure technique available and apply it. Available techniques for jamming are, among others, mainlobe blanking, inverse con-scan, range-gate pull-off, and swept square modes.

In real life, these two systems differ greatly, with the AN/ALR-126 being by far the most effective system. In DCS, both are modeled as simple noise jammers due to engine limitations but controlled by the DECM logic as to when it’s on or off and thus work the same.

## DECM Controls and Indicators

![Control Panel](../../img/control2.png)

The controls for the DECM are all located on the right horizontal panel in the RIO pit, as shown in the image above. In addition, there are two indication lights co-located with the RWR threat indicators on the right side of the TID.

The two indication lights on the threat advisory are **RCV (receive)** and **XMIT (transmit)**. **RCV** illuminates when the system detects and analyzes a threat, while the **XMIT** illuminates when it’s actively jamming a threat.

The control panel itself contains a **STANDBY** indicator light, a mode selector knob, and an **AUDIO** volume knob.

- The **STANDBY** light indicates that system warmup is not yet completed and turns off when completed. At other times, illumination of this indicator indicates the presence of a fault in the system.
- The **AUDIO (volume)** knob controls the audio volume of the RIO sound from the system. The pilot has no access to this audio. The audio itself is generated from the PRF of received threats with PRF frequency being converted to audio frequency.
- The mode selector knob controls power and operational mode of the system:
  - **OFF** turns off power to the system.
  - **STBY** begins pre-warming of the system, taking around 5 minutes.
  - **TEST - HOLD 3 SEC** is used to prepare the system for BIT. After 3 seconds in this mode, turn the knob to TEST - ACT.
  - **TEST - ACT** starts the BIT in the system. The BIT takes approximately 30 seconds, and the **RCV** light will be illuminated the whole time while the **XMIT** light will flash twice. If the **STANDBY** light illuminates, it indicates that a no-go condition exists in the system.
  - **REC** enables the system in receive-only mode, enabling analysis of threats and also the threat audio.
  - **RPT** enables full system functionality; in addition to **REC**, it also tries to jam threats according to the selected method.

> **Note:** In DCS, jamming is always done with noise jamming, turning on as a threat is detected.
