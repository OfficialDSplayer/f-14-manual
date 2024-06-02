# Flight Control System

The flight control system on the F-14 Tomcat is driven by the two main hydraulic circuits, powered by pumps connected to each engine.

For longitudinal (pitch) control both tail stabilizers are deflected in unison, acting in the same way as traditional elevators.

Lateral (roll) control is produced by both the tail stabilizers and the spoilers working in unison. To produce roll the stabilizers are deflected opposite each other to act as ailerons in combination with the spoilers on the side to which roll is commanded.

The rudders on the F-14 is a standard rudder configuration albeit in a two tail, two rudder configuration.

Control surface position is indicated on the Control Surface Position Indicator and can also be used to check trim position with controls at neutral.

> **Note:** Above 15 units AOA, the rudders should be used for lateral (roll) control due to the different airflow along the aircraft control surfaces.

## Trim

Longitudinal and lateral trim is accomplished via the trim hat on the Control Stick. This changes the stick neutral position, thus trimming the aircraft. Rudder trim is accomplished via the RUDDER TRIM switch on the Inlet Ramps/Throttle Control Panel, changing the neutral rudder position.

The Mach Trim and ITS (Integrated Trim System) automatically trims to compensate for changes in longitudinal trim. The Mach Trim system compensates for transonic and supersonic trim changes and the ITS for trim changes due to flap and speedbrake position changes.

## AFCS Automatic Flight Control System

The AFCS or Automatic Flight Control System provides additional aircraft stability (SAS or Stability Augmentation System) via automatic control surface commands generated from AFCS sensors. The AFCS is controlled by switches on the AFCS Control Panel, and pitch, roll, and yaw can each be set individually.

- **Pitch and roll switches:** Spring-loaded to off but normally held to on by solenoids, meaning that if the system is turned off or inoperable, the switches return to off. The yaw switch is purely mechanical.
- **Roll SAS:** Should not be used for situations involving flight at AOA above 15 units and should therefore be set to off for combat maneuvers.
- **Autopilot emergency disengage paddle:** On the control stick, if held down, sets the pitch and roll channels to off.

## Autopilot

Apart from stability augmentation, the AFCS is also used to provide autopilot functionality. To use the autopilot, all three stabilization channels must be enabled.

### Autopilot Modes

The controls for the autopilot system are situated on the AFCS Control Panel. Available modes include:

- **Attitude hold:** Set the autopilot ENGAGE switch to on to maintain current aircraft attitude. Limited to within 30° pitch and 60° roll angles. The current attitude can be changed with the control stick and will be held when the stick is released.
- **Heading hold:** Set the HDG switch to HDG. Maneuver the aircraft to the desired heading with a bank angle of less than 5° to set the heading.
- **Ground track mode:** Set the HDG switch to GT, wait for the A/P REF warning light on the left side of the Vertical Display Indicator (VDI) to illuminate, and then press the nosewheel steering button on the control stick. The A/P REF warning light will turn off, and the ground track mode will be enabled.
- **Altitude hold mode:** Set via the ALT switch. The A/P REF warning light will illuminate until the nosewheel steering button is depressed, enabling the mode.
- **Data Link Vector - Precision Course Direction mode:** Allows a Link 4 controller to remotely control the aircraft. (Not modeled in DCS)
- **ACL or Automatic Carrier Landing mode:** Used for automatic carrier landings in conjunction with the Link 4 data link and the onboard radar beacon. Set the VEC/PCD switch to ACL, and the A/P REF warning light will illuminate. When intercepting the ACL glideslope and with the ACL READY and A/P CPLR warning lights illuminated on the VDI, depress the nosewheel steering button on the control stick to engage the ACL.

The ACL can be used in conjunction with the APC (see Throttle Controls) for a fully automatic landing. The ACL can be disengaged via the PLM button on the right throttle and the APC via the CAGE/SEAM button on the left throttle.

All autopilot modes can be overridden by enough force on the control stick or by depression of the autopilot emergency disengagement paddle, automatically resetting all autopilot switches to off.

## Spoilers

The spoilers located on the upper surfaces of the wings are used to control roll as detailed above under Flight Control System, for braking on the ground as part of the Antiskid system and as a part of the DLC system (see next header).

The spoilers are only used forwards of 62° wing-sweep as further aft these conflict with the fuselage.

In case of a spoiler malfunction the spoiler symmetry protection logic disables all of the spoilers in the same section as the failed spoiler, either inboard or outboard spoilers. If this occurs the SPOILERS caution light on the Caution - Advisory Indicator illuminates.

To override this the switch corresponding to the relevant section on the Spoiler Failure Override can be set to override by lifting the guard and setting the switch to ORIDE and then depressing the MASTER RESET button on the Fuel Management Panel.

Spoiler position can be seen on the Control Surface Position Indicator.

## DLC Direct Lift Control

The DLC or Direct Lift Control is used to control vertical glideslope position without pitch control inputs or engine throttle commands.

- **Engagement:** Engage the DLC by depressing the DLC switch on the control stick with flaps down and throttles less than MIL. This causes the inboard spoilers to extend to half and enables the DLC & maneuver flap command thumbwheel on the control stick to control them.
- **Control:** Rotation of the thumbwheel forwards extends the spoilers, decreasing lift and adjusting glideslope position downward. Rotation of the thumbwheel aft retracts the spoilers, increasing lift and adjusting glideslope position upward.
- **Disengagement:** Another depression of the DLC switch disengages the system.

## Flaps and Slats

The flaps and slats on the F-14 Tomcat can be used in two modes.

- **Normal flap and slat extension:** Controlled using the FLAP handle on the Throttle Quadrant. The flaps can be set to anywhere between retracted and fully extended where the flaps will extend to 35° and the slats to 17°. The auxiliary flaps, the innermost section, only have two positions, retracted and extended. They will extend fully when the FLAP handle is at more than 5° extension.
  - **Faulty retraction:** If a fault prevents retraction, move the FLAP handle to the UP position and then outboard and up to the EMER UP position to override faulty interlocks.
- **Maneuver flap system:** The CADC uses the flaps and slats automatically to improve aircraft performance. In this mode, the flaps extend to 10° maximum and the slats to 7° maximum, and the innermost flap section is disabled.
  - **Manual control:** The maneuver flap system can be manually controlled using the DLC & maneuver flap command thumbwheel on the control stick. Forward thumbwheel rotation retracts the flaps and slats, and aft thumbwheel rotation extends them.

When sweeping the wings, the flaps are limited by the wing-sweep position. Aft of 21° sweep, the auxiliary (inboard flaps) are disabled up. Aft of 50°, all flaps are disabled up. The slats are not inhibited by wing-sweep.

Position of the flaps and slats are indicated on the Wheels-Flaps Position Indicator.

- **FLAP light:** The FLAP light on the pilot Caution - Advisory Indicator indicates a malfunction in the flap system with flaps at non-symmetrical positions.
- **REDUCE SPEED warning light:** The REDUCE SPEED warning light on the left side of the Vertical Display Indicator (VDI) indicates flaps not retracted above 225 knots indicated airspeed.

## Speedbrakes

The speedbrakes on the F-14 Tomcat consist of three sections on the tail located between the engines and are powered by the combined hydraulic system.

- **Control:** The speedbrake controls are located on the right Throttle and can be set to the desired position depending on how long the switch is held to the extend position. Retraction always fully retracts the speedbrakes.
- **Protection:** The speedbrakes will start retracting above 400 knots and will continue to do so with increasing airspeed. Additionally, selection of MIL power or above automatically retracts them.
- **Fuel dump:** As the speedbrakes disturb airflow around the tail, the fuel dump is disabled with speedbrake extension to prevent the fuel from hitting the aircraft.

Position of the speedbrakes can be seen on the Wheels-Flaps Position Indicator.
