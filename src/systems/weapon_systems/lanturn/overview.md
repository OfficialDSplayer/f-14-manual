# LANTIRN

![LANTIRN](../../img/lantirn.png)
*U.S. Navy photo by Photographer’s Mate 2nd Class Felix Garza Jr. (030325-N-4142G-009)*

## Description

The LANTIRN or Low Altitude Navigation and Targeting Infrared for Night began life as combined targeting and navigation pods designed for the F-15E and F-16. When the US Navy became interested in using the F-14 Tomcat in the A/G role Martin Marietta (now Lockheed Martin) began its own program to show that the LANTIRN could quickly be adapted for F-14 use.

As the pod was adapted for the F-14 the secondary navigational pod was deleted, keeping only the targeting pod. The pod was wired up to its own control panel as the F-14 didn’t have the required 1553-bus for complete integration. The control panel was patched into the TCS -> TID video feed allowing it to select either the TCS or the LANTIRN for display on the TID and VDI.

While the pod can read waypoints and selected weapon from the WCS, the pod has its own GPS receiver and is otherwise self-contained and controlled only via its own control panel. Additionally, it also has its own weapons release guidance removing the need to boresight the pod to the aircraft, a time-consuming task.

The FLIR sensor itself has three different zoom levels or fields of view (FoV). The Wide FoV limits are 5.9° and allows a maximum slew rate of 8.5°/s. The Narrow FoV limits are 1.7° and allows a maximum slew rate of 1.8°/s. The last mode, the Expanded FoV is a digital zoom of the Narrow FoV, meaning that the resolution will be worse in this mode. The FoV limits for the Expanded FoV are 0.8° with a max slew rate of 0.7°/s.

## Controls and Displays

All the controls for the LANTIRN are situated on its own control panel mounted on the RIO’s left side console when the pod is present, including the switch controlling what video feed the TID and VDI display in the TV mode.

### LANTIRN Video Elements

The FLIR (Forward Looking InfraRed) video-feed from the LANTIRN has superimposed data readout for the crew’s use. This video-feed can be viewed both on the TID (in TV-mode) and on the VDI (also in TV-mode) when the FLIR feed is selected on the control panel.

Amongst other things the displays show own aircraft position, target position as well as targeting cues to the crew. When using the LANTIRN for A/G attack these readouts are also used as targeting and release cues.

![FLIR](../../img/FLIR.png)

1. Own aircraft data is shown in the upper left corner, showing position, altitude, groundspeed and pitch angle (dive).

2. The pod displays whether it’s using white hot or black hot (WHOT and BHOT) as well as if the AGC (Automatic Gain Control) or MGC (Manual Gain Control) is in use.

3. The lower left datablock shows pod information, SR is slant range (line of sight range), AZ and EL is pod line of sight azimuth and elevation relative aircraft ADL (with AZ having L or R for left or right of aircraft heading). Below that is current UTC time and then IBIT codes below that.
   > **Note:** IBIT codes are not implemented currently and the clock will show local time.

4. The lower middle shows current pod mode (A/A or A/G) and track mode (AREA, POINT or Q designations) on the left side. The right side shows currently selected weapon and laser code while above and in the center an L is shown when the laser is armed and flashing when firing the laser.

5. The lower right shows data for currently selected Q (slewpoint) except for QSNO, QADL and QHUD, TTG being time to go until on top of currently selected Q, the rows below that, bearing and range to Q, ELEV indicating elevation in feet of Q and lastly, below that, Q location.

6. The crosshairs showing tracked position, in this case we have a bounding box, indicating currently tracked target in point mode. The two widest zoom modes will have boxes showing the field of view for the next, narrower, mode. Additionally there’s a small white square (FLIR pointing cue) moving around showing the current pod line of sight relative to aircraft from a top-down perspective. In this case it’s right next to the upside-down ^, top center, indicating that the pod is looking ahead of the aircraft. If the square is centered the pod is looking straight down and below center it indicates the pod looking aft.

7. The steering guidance towards the selected Q, the top one being commanded heading and the vertical one on the right the bomb release cue. 
   - The commanded heading shows current aircraft heading above the inverted ^, with the commanded heading being displayed as a relative bearing either L (Left) or R (Right) of current aircraft heading below the line. The commanded heading is also indicated by a vertical line bisecting the horizontal one.
   - The right, bomb release cue, is only shown if the selected Q is QDES and shows a vertical line along which a release cue travels downwards. This release cue is only visible with a valid weapon selection (bomb) and when it reaches the two tick marks, that’s the cue to release. Below the line is the indicated TREL (Time to Release) in seconds, changing to TIMP (Time to Impact) after release.

Around this all is the masking curve, indicating at what angles the pod will be masked by own aircraft (looking into the aircraft hull). This is relative to the FLIR pointing cue, when the cue moves outside the masking curve the sensor will be blocked by the hull.

### Control Panel

The control panel contains all the controls for the pod, including the control stick.

![Control Panel](../../img/panel.png)

1. The power switch for the LANTIRN pod is located top left with OFF disabling power to the system, IMU (blocked in above image) powering only the LANTIRN IMU and POD powering the whole system.
   - **Note:** IMU selection has no current DCS function.

2. The MODE switch switches the POD sensor between STBY (Standby) and OPER (Operational).

3. The LASER ARMED light illuminates when the laser is armed while the LASER switch arms it. (ARM and SAFE positions available.)

4. Down right is the VIDEO switch which controls what video is fed to the TID and VDI, FLIR selecting LANTIRN FLIR video and TCS selecting TCS video.

5. The four grouped indicator lights indicate various error states in the LANTIRN system and the IBIT button initiates the IBIT (Initialized Built-In-Test).
   > **Note:** The IBIT and fault indicators are not currently implemented in DCS.

### Control Stick

The control stick for the LANTIRN operates the LANTIRN’s sensor itself, note though that the stick itself does not move, the buttons and hats on the stick are used to control the pod.

![Control Stick](../../img/stick1.png)

1. The left four-way hat, S3, allows selection of QWp- and QWp+ (left/right) in addition to Point Track (up) and Area Track (down) modes.

2. The center slew hat is used to slew the sensor line of sight itself and depression of this hat switches between white hot (WHOT) and black hot (BHOT) sensor modes.

3. The right four-way hat, S4, allows for selection of QADL/QHUD (up), QDES (right) and QSNO (down) in addition to declutter level which is cycled by momentary depression of the hat. The left slider additionally changes the right hat function as detailed further down.

4. The red button on top is used to cycle between the three fields of view (zoom levels) of the IR sensor.

5. The two-way hat on the side selects either the A/G or A/A modes of operation for the pod.

6. Located on the left side of the stick head is a two-way slider, spring-loaded to return to center. This switch changes the function of the right four-way hat.
   - Sliding it forwards allows for selection of manual gain while releasing and sliding it forwards again reselects automatic gain. Change of the manual gain with manual gain already selected can be done by sliding the switch forwards and holding it for 2 seconds. With this mode active up/down on the right hat increases and decreases the gain while left/right decreases and increases level.
   - Sliding the switch aft momentarily allows selection of used laser code, while sliding it aft and holding allows for focus control. When set to laser code change, the right four-way hat selects digit to change with left/right and increases and decreases the selected digit with up/down. In focus control up/down increases and decreases focus.

7. Located on the front of the stick is a two-stage trigger, first detent manually lasing while the second detent fires the laser and designates QDES at current sensor position.

8. Lastly on the front side of the stick is the latched laser fire button. Selecting it fires the laser for 60 seconds which can be overridden by pressing and releasing the first trigger detent. A renewed press on the laser latch button resets the latched laser fire timer to 60 seconds, beginning a new 60-second countdown.

## Operation

### Startup

To start the LANTIRN from cold, set the power switch to POD. This will start the LANTIRN power-up sequence which takes 8 minutes. When ready, this will be indicated by the MODE switch showing STBY.

When at STBY, depression of the MODE button switches the system to OPER (Operational), enabling the LANTIRN sensor after a 30-second initialization.

Lastly, to allow display of LANTIRN FLIR video, select FLIR on the VIDEO switch.

### Sensor Modes and Operation

The LANTIRN has two “master” modes, A/A and A/G. Both work similarly but are optimized for different types of targets. Additionally, the A/G mode allows for bomb release guidance.

The pod has two main ways of controlling the sensor line of sight, either via contrast lock (image following) or via being slaved to a Q designation.

The Area and Point Track modes are the two contrast lock modes in which the LANTIRN locks onto contrast differences in the LANTIRN FLIR video itself. This in itself only allows for angle tracking which gives imprecise ranging using own aircraft position and pod line of sight to calculate target position. It does however allow the system to track moving targets.

The last tracking mode has the sensor slewed to a stored location/direction, called a Q. The directional Qs do not allow for guidance to a location while the location Qs do.

QSNO and QADL/QHUD are directional. QSNO slaves the sensor to the ground 15 NM directly in front of the aircraft along own aircraft heading. QADL and QHUD slave the sensor to either ADL (in A/A) or the aircraft wings symbol on the HUD (in A/G).

The location Qs have two sources, QWp- and QWp+ on the stick’s left hat can be used to cycle through the WCS waypoints, allowing the RIO to slew to the different waypoints for navigation and target localization.

The other source is via pod designation. By selecting the second detent on the LANTIRN trigger the current sensor track or location is lased and a new location stored using that data. This is called the QDES and is used to designate targets for engagement as well as allowing the RIO to select a new location for navigational reference on the fly. The QDES can not however be automatically transferred to the WCS, but the RIO can enter it manually using the target location information in the pod video feed.

The lower right datablock is enabled for the location Qs only but will remain even when the pod is slewed away in area or point track modes. As soon as another Q is selected however, it will update to that location instead or be removed if a directional Q is selected.

### A/G Target Engagement and Designation

The LANTIRN steering cues for ground target engagement are automatically enabled when the LANTIRN is slewed to QDES or a new QDES is designated. The QDES itself will remain even if a new Q is selected and as long as it exists, the steering cues will point towards QDES even if slewed to another point. This is important to keep in mind as it is easy to think that the steering commands are to the current sensor location instead of the QDES.

The laser designation itself can however point to a different location than the QDES as the laser always points to the current track. This can be used to quickly change back to a target marked by the QDES if desired and when lasing a moving target a QDES should be set at an estimated target location at impact (estimated manually) and then the point track mode or manual slew can be used to designate the actual target more precisely.

To change laser code, move the stick left side slider aft and release, this will change right hat (S4) into laser code mode. The currently selected digit will blink and the S4 hat can then be used to set the digits. Left/right change what digit to set and up/down change the value of the digit. Renewed selection of aft on the left slider will then exit the laser code mode.

If the right, S4, hat is depressed while in laser mode the automatic lase mode will be enabled, indicated by the M (for manual) left of the digits changing to an A (autolase). Repeat to switch back to manual mode. While activated, the autolase mode will begin firing the laser at 10 seconds TIMP until TIMP zero +4 seconds.

The bomb release cue is only visible with a valid weapon (bomb) selected and the selected bomb is read from the weapon selector wheel on the RIO armament panel via the WCS. The actual bomb release can be accomplished using the computer pilot or computer target modes but the manual mode is recommended. In manual mode the pilot follows the cues in the LANTIRN video feed on the VDI and releases the bomb when cued by the LANTIRN.
