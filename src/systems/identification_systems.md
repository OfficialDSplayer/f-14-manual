# Identification Systems

## AN/APX-76 IFF Interrogator

The AN/APX-76 IFF (Identification Friend or Foe) interrogator is integrated into the AN/AWG-9 operation. Then interrogator antenna itself is located on the AN/AWG-9 antenna gimbal platform.

An IFF system works by sending out an interrogation pulse and then listening for returns from cooperating transponders. In addition to the unencrypted civilian mode the AN/APX-76 is capable of interrogating in the encrypted military mode 4. This ensures that targets replying to mode 4 interrogations are indeed friendly.

The AN/APX-76 can be used both in search radar modes and in STT radar modes. To enable interrogation the IFF switch is depressed on the Detail Data Display Panel which then activates the interrogator for as long as the button is held up to 10 seconds max.

When enabled IFF received IFF returns are then overlaid on the normal AN/AWG-9 radar returns on the DDD. A friendly target will be indicated with two bars, one above and one below the normal radar return. As the AN/APX-76 is a secondary mode radar (transponder radar) apart from the AWG-9 the IFF can sometimes also detect targets not detected by the AWG-9. In this case the IFF return will not have a radar echo inside it.

In the search mode this is overlaid over each target replying and in STT over the STT target. Additionally, if the STT target is hooked on the TID the DDD will switch from normal range display to a ±10 NM display to enable display of multiple returns in case of closely grouped targets.

### AA1 Control Panel

![aa1](../../img/aa1.png)
AN/APX-76 interrogator control panel.

| No. | Control/Indicator     | Function                                                                                   |
|-----|-----------------------|--------------------------------------------------------------------------------------------|
| 1   | M4 ALARM OVERRIDE switch | Switch disabling the mode 4 tone alarm in the RIO headset.                                 |
| 2   | TEST-CHAL CC switch   | Switch spring-loaded to center controlling IFF challenge and test. TEST - Momentary actuation, tests the AN/APX-76 by interrogating own transponder, if the same codes are set two solid lines appear on DDD at 3 and 4 miles. CHAL CC - Momentary actuation, starts a 10 second interrogation cycle only showing returns with correct mode and code on DDD. |
| 3   | CODE selector thumbwheels | Thumbwheels controlling mode and code used for interrogation. First wheel sets mode, last four set code. |
| 4   | CHAL light            | Light indicating active interrogation in progress.                                          |
| 5   | FAULT light           | Light indicating fault in AN/APX-76.                                                        |
