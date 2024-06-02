# General Design and Systems Overview

## Engines and Throttle Controls

The F-14A is powered by two Pratt & Whitney TF30-P-414A while the F-14B is powered by two General Electrics F110-GE-400, both of which are afterburning turbofan engines.

To provide the engines with an even subsonic airflow the F-14 has the AICS or Air Inlet Control System. This system controls the variable geometry intakes by moving the variable ramps mounted in them to slow the airflow. This is accomplished using various sensor inputs run through a calculation using set schedules which decides the positions of the ramps.

In addition, the TF30 uses two systems to improve reliable operation, the Mid Compression Bypass System (MCB) and the Mach Lever.

The MCB helps mitigate high angle of attack airflow onto the compressor fans to reduce the risk of an engine stall. This system vents air from the compressor section to bypass duct to stabilize the airflow for later compressor stages. Normally this system uses angle of attack and Mach number sensor data to activate, but with the landing gear handle in the down position this it is only activated with zone 5 afterburner. Additionally the WCS commands the MCB to activate with extension of the refuelling probe as well as when launching AIM-7 or AIM-9 missiles, air to ground rockets or firing the M61 Vulcan gun.

The Mach Lever also mitigates the risk of an engine stall by controlling min and max rpm allowed as a function of Mach number. In addition it also increases the minimum rpm in high angle of attack regimes while subsonic.

The two F110s in F-14B, on the other hand, are controlled by the AFTC (Augmenter Fan Temperature Control unit). The AFTC is an early engine control computer akin to an early version of a FADEC (Full Authority Digital Engine Control) used on newer turbine engines. This system controls both the engine itself as well as the variable exhaust nozzles controlling the engine exhaust gases and removes the need for the MCB and Mach Lever for the F110. The lack of such a system in the F-14A controlling its TF30s is one of the reasons for them being deemed less reliable than the F110s.

In case of a failure in the AFTC the MEC (Main engine control) is capable of assuming control of the engines to provide a fall-back, mechanical control. The normal mode, AFTC, is the primary mode (PRI) and called as such while the fall-back MEC is the secondary (SEC) mode. The selection of primary or secondary is automatic in case of a failure in the AFTC but can also be manually selected. Of note is that in secondary mode the engine nozzles are fully closed and disabled in addition to the afterburners being disabled with a corresponding loss of engine performance.

In addition both engines also drive separate fuel, hydraulic and electric generators to create redundancy.

**Note:**
The main difference between the TF30 and F110 engines (apart from lesser thrust in the TF30s) is that the TF30s are more sensitive to the quality of the airflow entering the compressor face. In general it is wise to avoid anything less than military power or afterburner while in high angle of attack maneuvers as well as avoiding large rudder inputs or asymmetric engine throttle settings. That said, the TF30s in the HB F-14A module have been extensively tuned using available data and SME expertise, resulting in an accurate modelling of an engine undeserving of its bad reputation. One “advantage” of the TF30’s mechanical fuel control is its high speed thrust, resulting in higher top speeds than the F110 can achieve. If flown within normal parameters, the TF30 engines behave well if a tad underpowered compared to the F110s.

## Throttle Controls

![throttles](../../img/throttles-schem1.png)

The throttles in the F-14 have detents preventing unintentional engine start and shutdown and unintentional selection of afterburner. In addition the throttles also controls several different systems depending on throttle position as shown in the diagram above. The most critical of these being the fuel cutoff and ignition systems in the respective engines.

For throttle operations there are three modes:

- **Manual Mode:** A mechanical mode in which the engines are controlled by mechanical linkages directly from the throttles to the engines. The manual mode is designed as a backup mode and may be inexact because of the mechanical nature of the controls.
- **Boost Mode:** The normal mode of operation in which electrical paths control actuators moving the same engine controls as the mechanical linkages but more exactly and with lesser force required.
- **Approach Power Compensator Mode (Auto Throttle Mode):** A system which allows for automatic throttle control for optimal angle-of-attack during approaches.

The controls for the throttle mode are located on the inlet ramps/throttle control panel to the side of the main throttles and allows for selection of all three modes. The auto throttle mode is solenoid held and will revert to boost mode if the criteria for automatic controls are not met.

To allow selection of auto mode the throttles need to be between 75 to 90% rpm, the gear handle needs to be down and with no weight on the wheels. If these criteria are no longer met, the throttles are manually overridden with force or the Cage/SEAM button on the left throttle is depressed the solenoid releases the switch and it reverts to boost.

For additional autothrottle tune the gain of the system can be set on the inlet ramps/throttle control panel. The settings are hot, normal or cold with hot increasing the throttle gain (and effective thrust) and cold decreasing it. These settings correspond to cold or hot external temperatures but should be set according to observed throttle control.

The RATS or reduced arrestment thrust system is a system limiting engine thrust after touchdown to limit it to levels appropriate for carrier environments. The system is enabled by weight on either main landing gear and is disabled by selection of afterburner on the throttles.

Finally, and implemented only for the F110-GE-400, is the asymmetric limiter, preventing asymmetric afterburner engagement if only one afterburner lights by keeping that afterburner at minimum afterburner thrust until the other afterburner also lights.

## Engine and Throttle Control Switches and Indicators

![inlet](../../img/inlet1.png)

The inlet ramps/throttle control panel contains most other engine related controls.

1. **THROTTLE MODE switch:** Sets throttle mode to AUTO, BOOST or MAN modes respectively, with auto being spring-loaded back to boost but held in place electrically as mentioned above.
2. **THROTTLE TEMP switch:** Controls the gain of the automatic throttle system also described above.
3. **INLET RAMPS switches:** Enable (AUTO) or disable, stow (STOW) the variable intake ramps.
4. **Engine crank switch:** Used to crank the engines to 20% rpm allowing for engine start by moving the respective throttle to idle from cut-off. The air to start the engine is sourced from an external air supply if connected or the other engine if no external source exists. At 50% rpm the crank switch automatically returns to off/center position. If this does not occur it should be manually set to off to prevent damage to the air turbine starter.
5. **BACK UP IGNITION switch:** Enables the backup ignition system in case of a failure in the main ignition circuits that are normally enabled by moving the throttles out of the cut-off position.

![asym](../../img/asym1.png)

**Note:** F-14B only.

1. **ASYM LIMITER switch:** On the ASYM limiter/engine mode select panel enables or disables the asymmetric afterburner thrust limiter. Default position is ON and the switch has a guard cover keeping it in that position.
2. **ENG (engine) MODE SELECT switches:** Setting the left (L ENG) and right (R ENG) to PRI, primary or SEC, secondary modes respectively.

![mcb](../../img/mcb1.png)

**Note:** F-14A only.

The MCB Test Panel, located in the RIO pit on the right horizontal panel, is used to test if the MCB system functions. The TEST switch set to the TEST position activates the test circuit which lights the two test lights for the left and right engine respectively if their MCB circuits function.

![externalenvironment](../../img/externalenvironment1.png)

The ENG/PROBE ANTI-ICE switch on the external environmental control panel enables the engine anti-ice and intake ramp anti-ice mode in addition to the various probe heaters. The ORIDE position enables the system, the AUTO position enables the system if icing is detected and the OFF position disable it.

## Engine Instrument Group (EIG), Related Indicators and Caution Lights

![instrument-group](../../img/instrument-group1.png)

The ENGINE INSTRUMENT GROUP displays engine RPM, TIT (Turbine Inlet Temperature, F-14A) or EGT (Exhaust Gas Temperature, F14B) and FF (fuel flow) to the pilot to allow for engine monitoring.

**Note:** Pictured above are the TF30 engine indicators, F110 EIG coming soon.

![exhaust](../../img/exhaust1.png)

The exhaust nozzle position indicators display respective engine’s current engine exhaust nozzle position, with zero being fully closed and full clockwise rotation being fully open. The F-14A indicates 0 to 6 units while the F-14B indicates 0 to 100 percent open (tens indicated on gauge).

![oil](../../img/oil1.png)

The oil pressure indicators display respective engine oil pressure allowing the pilot to check that engine oil pressure is at acceptable levels.

The caution lights relevant to engine operation are located on the pilot’s caution - advisory panel, and at the sides of the HUD.

The caution lights on the sides of the HUD are the engine stall warning lights which flashes at a 3 Hz rate when an engine stall is detected. The warning light on the left side of the HUD indicates an engine stall in the left engine and the one on the opposite side the right engine. This is also combined with an audio warning, a modulated tone at 320 Hz.

Below the left engine stall warning light is, amongst others, the AUTO THROT (auto throttle) caution light which illuminates for 10 seconds when the auto throttle system is disengaged by other means than the throttle mode switch.

On the main caution - advisory panel the relevant engine caution and warnings lights are:

- **INLET ICE:** Caution light indicating ice detection on the detector in the left engine inlet.
- **L & R INLET:** Caution lights indicating failure in AICS for respective variable intake system.
- **OIL PRESS:** Caution light indicating low oil pressure in either engine.
- **BLEED DUCT:** Caution light indicating hot air leakage in either engine.
- **L & R RAMPS:** Caution lights indicating respective engine intake ramp not being locked into position when supposed to.
- **L & R GEN:** Caution lights indicating that respective engine generator is inoperative.
- **L & R OIL HOT:** Caution lights indicating that respective engine oil is too hot.
- **L & R FUEL PRES:** Caution lights indicating engine fuel pressure below 9 psi in respective engine fuel boost pump.

**F-14A TF30-P-414A only lights:**

- **L & R OVSP/VALVE:** Caution lights indicating engine starter system malfunction or N1 rotor overspeed in respective engine.

**F-14B F110-GE-400 only lights:**

- **START VALVE:** Caution light indicating that the starter valve is open. Control engine crank position if lit after engine start completion.
- **L & R ENG SEC:** Caution lights indicating that respective engine is operating in secondary mode.
- **RATS:** Caution light indicating that RATS (reduced arrestment thrust system) is enabled.

**Note:** F-14A specific lights not yet implemented.

## Fuel System

![tanks](../../img/tanks.png)

1. Refueling Probe, 2. Ground refueling Port (Right Side), 3. Forward Fuselage Tank, 4. Left External Drop Tank, 5. Left Box Beam Tank, 6. Left Wing Tank, 7. Vent Tank, 8. Fuel Dump Mast, 9. Aft Fuselage Tank, 10. Right Box Beam Tank, 11. Right Wing Tank, 12. Right External Drop Tank.

The main fuel storage in the F-14 consists of two feed systems, one for each engine. The right engine feed system consists of the right wing and right box cells and the front fuselage cells while the left engine feed system consists of the left wing and left box cells in addition to the aft fuselage cells. This fact needs to be kept in mind when reading the fuel gauges.

The total usable fuel quantity is roughly 20,000 pounds distributed as in the table below.

| Tank group         | Pounds |
|--------------------|--------|
| Forward Fuselage   | 4,700  |
| Aft Fuselage       | 4,400  |
| Right Feed Group   | 1,600  |
| Left Feed Group    | 1,500  |
| Internal Wings     | 4,000  |
| External Tanks     | 3,600  |

## Fuel Quantity Indicators and Controls

![fuelquantity](../../img/fuelquantity1.png)

The fuel quantity indicator on the pilot right knee panel displays internal and external fuel carried.

1. **BINGO indicator:** Displays currently set BINGO fuel level, this quantity is set by rotating the knob (5) to desired amount. This indicator and control activates the BINGO caution light when total fuel level is below set amount.
2. **TOTAL indicator:** Displays total carried fuel.
3. **L and R indicators:** Normally shows fuel carried in left and right fuel feeds respectively. A rocker switch on the fuel management panel enables selection of the wing internal tanks (WING) or external fuel tanks (EXT) for display but is spring-loaded to return to showing the feed tanks (FEED) automatically. When displaying wing internal tanks or external fuel tanks, the left wing or left external tank is shown on the L counter and the right wing or right external tank on the R counter.
4. **FUS & FEED tapes:** Shows the AFT & L (aft fuselage and left feed) and FWD & R (forward fuselage and right feed) in thousands of pounds.
5. **SET knob:** Used to set BINGO fuel quantity. Turn to set desired quantity.

Additionally the RIO has a total fuel quantity display on the right instrument panel. This display counter can only show total fuel quantity. (See Fuel Quantity Totalizer.)

![fuel](../../img/fuel2.png)

The fuel management panel on the pilot’s left vertical console contains the applicable controls for the fuel system.

1. **QTY SEL rocker switch:** Detailed above under the description above about the L & R fuel displays.
2. **FEED switch:** Allows the pilot to correct fuel imbalances caused by single engine operation or feed failures by selecting both engines to feed from either the FWD (forward and right tanks) or AFT (aft and left tanks) instead of from one feed system each as normal NORM. The switch guard locks the switch to the NORM position when down.
3. **WING/EXT TRANS switch:** Controls fuel transfer from the wing and external tanks into the fuselage feed systems. The normal AUTO position enables this transfer as soon the landing gear is retracted. The ORIDE position enables this transfer regardless of landing gear position, enabling transfer when on the ground or during a malfunction in the electrical system inhibiting landing gear retraction detection. Additionally the OFF position disables this transfer but can be overridden automatically to AUTO when the INST test is performed on the MTS panel, the refuel probe is set to ALL EXTD or when dumping fuel.
4. **DUMP switch:** Enables fuel dump through the beaver tail fuel dump mast, it also enables all fuel transfer systems, enabling dump of fuel in wings and external tanks in addition to the fuselage. If there’s weight on the wheels or the speed brake is not fully retracted the fuel dump is inhibited.

**Note:** Even though technically possible to engage the afterburners after a fuel dump is in progress, this is not allowed due to the possibility of igniting the dumped fuel.

## In-Flight Refueling

The above panel also contains the control for the in-flight refueling system.

1. **REFUEL PROBE switch:** Controls the extension of the refueling probe as well as setting up the fuel system to receive fuel. The two extended positions (EXTD) are ALL, enabling refueling of all tanks, including wings and external tanks and FUS, allowing refuel of only the fuselage tanks. When selecting the ALL position the fuel feed from the wings and external tanks are disabled to allow refueling of these tanks. RET (Retract) retracts the refueling probe and resumes normal fuel system operation.

**Note:** Selecting EXTD ALL resets the WING/EXT TRANS switch to AUTO.

## Fire Detection and Suppression System

### Fire Detection System

The fire detection system in the F-14 has two fire sensing loops, one in each engine.

If these loops detects a temperature over 600 °F (about 316 °C) along its whole length or 1,000 °F (about 538 °C) in a single 6-inch section it triggers the fire detection circuits. The left detection loop illuminates the left fire warning light on the ACM panel and the right detection loop illuminates the right fire warning light, see Air Combat Maneuver Panel.

In addition there are also sensors designed to detect hot air leaks in the engines and illuminate the BLEED DUCT caution light on the pilot caution - advisory indicator (see Caution - Advisory Indicator) if temperatures above 575 °F (about 302 °C) are detected.

### Fire Suppression System

![left](../../img/left1.png) ![right](../../img/right1.png)

The fire suppression system in the F-14 contains two bottles filled with a fire suppression agent capable of being discharged into one engine selected by the pilot. Though the system contains two bottles, both are discharged at the same time making the system a one-shot system, capable of extinguishing only one engine.

As the effectiveness of the agent depends on it remaining in the engine until the fire is out the effectiveness is greater at lower airspeed as it takes longer for the agent to be blown clear of the engine. The agent itself is a low toxicity agent, designed to do as little damage to the engine as possible while still being an effective fire suppressant.

To activate the system the pilot pulls the FUEL SHUT OFF handle (pictured above) corresponding to the alight engine and pushes the fire extinguisher button behind that handle. The pull-out of the handle shuts off the fuel to the connected engine and the button behind it releases the fire suppression agent into that engine.

Two advisory lights are connected to this system, each one indicating low pressure in one of the fire suppression agent bottles. The ENG FIRE EXT indicates low pressure in the main bottle and the AUX FIRE EXT the same in the auxiliary bottle. Both are located on the pilot caution - advisory indicator, see Caution - Advisory Indicator.

The advisory lights will both illuminate after a successful application of the system and will also indicate if an error drains the pressure in the bottles.

### Fire Detection and Suppression System Test

Both systems can be tested by selection of the FIRE DET/EXT position on the master test panel switch. (See Master Test Panel.) This will illuminate both fire warning lights on the ACM panel if their respective loop is functional and the GO light on the master test panel will illuminate if the suppression system is functional. If the NO GO or no lights illuminate there’s a problem in either the suppression system or the test circuitry.

## Electrical Power System

All main electrical power in the F-14 is generated from the two engine driven AC generators. The generators connected to the gearboxes on the engines are each capable of generating enough power to individually drive all aircraft systems.

As for DC power generation the F-14 has two transformer-rectifiers supplying 28 V DC, and again each one is individually capable of driving all aircraft DC appliances.

The F-14 has an external power receptacle for AC power just aft of the nosegear, capable of driving aircraft AC and DC (through the transformer-rectifiers). External power is automatically disconnected from the aircraft power system when one of the internal generators come online.

### Emergency Power

The F-14 has an emergency generator driven by the combined hydraulic system generating a limited supply of AC and DC power. If the system loses main power the emergency generator takes over supply of flight critical systems within 1 second.

### Controls and Indicators

![generator](../../img/generator1.png)

The controls for the electrical systems are located on the master generator control panel.

1. **MASTER GEN switches:** Control connection of the main generators to the electrical buses. The NORM position on the switches connect the individual generators to the buses. The OFF/RESET position disconnects the generator and also resets any protection circuits that might have cut in because of the power supply being outside normal limits. The TEST position starts the generator but do not connect it to the electrical buses making it possible to test the generator without affecting other aircraft systems. The switch is locked to the on position and needs to be lifted to move it to the OFF/RESET position from NORM.
2. **EMERG switch:** Controls the emergency generator. In the NORM position the emergency generator is automatically connected to the essential buses if the main generators fail. The OFF/RESET position deactivates the emergency generator and also resets the associated protection circuits if tripped. The switch is guarded to the NORM position and that guard needs to be opened to move the switch to OFF/RESET.

Associated caution and advisory lights are located on the pilot Caution - Advisory Indicator. The L GEN and R GEN lights, when illuminated, indicate that the respective generator is not functioning correctly. Either because of a fault or because the engine driving the generator not running.

The TRANS/RECT advisory light indicates that only one or none of the transformer-rectifiers are functioning.

The emergency generator can be tested by selection of EMERG GEN on the MASTER TEST switch on the Master Test Panel. Completion of the test is indicated by the GO light illuminating. In case of a fault the NO GO light illuminates.

### Circuit Breakers

The circuit breakers in the F-14 are located on the pilot’s right and left knee panels and behind the RIO’s seat on his left and right sides. The breakers protect aircraft systems from overcurrent by popping out and isolating the system drawing too much current. This is indicated by a white line becoming visible on the breaker as it pops out. The breaker can be reset by pushing it in and it can also be pulled out manually.

These breakers will be detailed here when implemented in DCS.

## Hydraulic System

The F-14 has two separate hydraulic systems, the flight hydraulic system and the combined hydraulic system.

Both systems are driven by hydraulic pumps connected to each engine, the flight hydraulic system from the right engine and the combined hydraulic system from the left engine. Both systems are pressurized to around 3,000 psi when operating normally.

Flight control surfaces are supplied by both systems while the combined system also supplies pressure to secondary systems such as the flaps, landing gear and the refueling probe. This is so that both systems can drive the control surfaces independently from each other in case of a failure in the other.

Additionally, the hydraulic systems related to systems not necessary while airborne can be isolated by a switch next to the landing gear handle. This is so that damage to those systems won’t affect the combined system pressure and cause fluid loss. The systems that can be isolated are the landing gear, wheel brakes, anti-skid and nosewheel steering. This switch is mechanically locked to not isolating these systems by the landing gear handle when it’s in the down position.

If only one of the hydraulic pumps fail it’s possible to pressurize that system from the other pump via the hydraulic transfer pump. This pump is an omni-directional hydraulically driven pump that can supply either system from the other and will maintain a pressure between 2,400 and 2,600 psi if the driving system is at around 3,000 psi. If one system pressure falls below 500 psi the pump will be secured to prevent pump damage and preserve pressure in the working system. The pump can also be manually disengaged by the pilot.

In case of failure of both hydraulic pumps the flight hydraulic system can be driven by an electrical pump, called the emergency flight hydraulic pump. This pump is capable of independently driving the tail control surfaces, enabling the aircraft to return home and land even without pressure in either main hydraulic system. The electric pump is automatically enabled if both main systems drop below 2,100 psi and shut off if either reaches 2,400 psi again. The automatic pump activation activates the system in the low mode but it can also manually be selected to either low or high operation. The control surfaces will have a reduced deflection rate if driven by this pump, more so in low than high.

There is also a hand driven hydraulic pump that can be used to pressurize the refueling probe and wheel brake accumulator if there’s otherwise no pressure in the combined system. This is mainly for unpowered ground operation but can be used as a backup in the air.

### Controls and Indicators

![hydraulic](../../img/hydraulic1.png)

The HYD PRESS, hydraulic pressure indicator, contains two gauges indicating COMB, combined, and FLT, flight system hydraulic pressure in thousands of psi. The scales have markings for the nominal 3,000 psi pressure when the pumps are operating normally.

Below the gauges are flags indicating hydraulic pressure availability to the spoilers SPOIL and the operation of the EMER FLT, emergency flight hydraulic pump. The HI flag indicates on if the emergency flight hydraulic pump is operating in high and the LOW if it’s operating in low.

![brakepressure](../../img/brakepressure1.png)

The BRAKE PRESSURE gauge shows available pressure in the brake accumulators. PARK indicating parking brake pressure and the AUX indicating wheel brake pressure. The green area represents a pressure from about 2,150 psi to 3,000 psi and the red a pressure below that.

![hydraulictransferpump](../../img/hydraulictransferpump1.png)

The HYD TRANSFER PUMP, hydraulic transfer pump switch is located on its own panel on the pilot’s right side console. The switch allows for manual shut-off of the pump (SHUTOFF) but is normally in the NORMAL position allowing the pump to activate automatically if either hydraulic pump fails. The switch is guarded to the NORMAL position.

The emergency flight hydraulic pump is controlled by a guarded switch on the Master Test Panel. The guarded position, (AUTO)LOW allows the pump to automatically activate as detailed above and the two other positions, HIGH and LOW can manually activate those modes when the guard is up.

On the Caution - Advisory Indicator the only relevant caution light is the HYD PRESS light indicating that either main hydraulic system pressure is below 2,100 psi. It turns off when both systems are again above 2,400 psi.

## Wing-Sweep System

![sweepschedule](../../img/sweepschedule.png)

Wing-sweep schedule as function of Mach number and related flap interlocks.

The wing-sweep system controls the geometry of the F-14’s wings, allowing the wings to move from a 20° to a 68° position in the air. While on the deck an oversweep of 75° is also possible reducing the F-14’s wing span to 33 feet (about 10 meters).

The wings are moved by hydromechanical screwjack actuators which are interconnected mechanically, making sure they’re synchronized. As long as both main hydraulic systems are functioning the maximum wing-sweep change rate is about 15°/s. This can be affected negatively by negative g or large amounts of positive g.

In normal operation the CADC, Central Air Data Computer, controls the wing position as a function of current Mach via the wing-sweep program, this is known as the AUTO mode. The pilot can also select a wing position aft of the wing-sweep program manually or choose the BOMB mode that sets the wings to 55° or further aft depending on the program. Simply put, the CADC wing-sweep program determines the max forward position of the wings. All this is done electrically via two independent channels (for redundancy) to the wing-sweep actuators.

Currently commanded wing position, CADC program wing position and actual wing position can be seen on the wing-sweep indicator next to the ACM panel.

### Emergency Mode

While the normal mode controls the wing-sweep electrically, to supplement this it’s also possible to control the wing-sweep mechanically via the emergency mode. This is done via the emergency wing-sweep handle on the right side of the throttle. That handle is connected mechanically to the hydraulic valves in the wing-sweep system, providing a physical back-up control.

Normally this handle is moved with the electronic wing-sweep program by a servo located beneath it, making sure it’s at the actual wing position. To disengage the electric system and enable the emergency mode the guard over the handle is opened and then the handle is extended for additional leverage. Then the handle can be forced out of the spider-detent normally connecting it to the electrical servo and then used to manually set the wing position.

In this mode the pilot has to make sure to follow the following schedule to avoid damage to the wings:

| Speed (Indicated Mach) | Max Forward Wing Position |
|------------------------|---------------------------|
| 0.4                    | 20°                       |
| 0.7                    | 25°                       |
| 0.8                    | 50°                       |
| 0.9                    | 60°                       |
| 1.0                    | 68°                       |

To return to the normal mode of operation, the handle should be pushed into the desired position and pressed down and the guard closed. The MASTER RESET button on the fuel management panel should then be depressed and the wing-sweep system set to the same position as the handle. The servo will then drive to the commanded position and re-engage the handle to the spider detent, resuming normal operation.

### Oversweep

The emergency wing-sweep handle is also used to select the oversweep position of the wings. The oversweep is only used while on the ground to reduce the wing span to make it easier to spot the aircraft on the carrier deck. As the wing will sweep over the stabilizers on the tail the horizontal tail authority system is enabled to prevent the wings and stabilizers from damaging each other by restricting movement of the stabilizer.

To set the wings to oversweep the emergency wing-sweep handle should be moved to the 68° position and held in the extended position. This will deflate the wing-seal airbags and activate the horizontal tail authority system, indicated by the HZ TAIL AUTH caution light illuminating. When the HZ TAIL AUTH caution light goes out and the OVER flag on the wing-sweep indicator appears the oversweep interlocks are free and the handle can now be moved to the 75° position and stowed.

To move the wings out of oversweep the handle is pulled up and moved forwards of 68°. This will again illuminate the HZ TAIL AUTH caution light. When the wings have physically exited the oversweep the caution light and the OVER flag will turn off.

As with normal emergency mode operation the handle should now be set to the same position as the spider detent and the MASTER RESET button depressed.

### Controls and Indicators

The controls for the wing-sweep system are on the right throttle (electrical) and to the right of the right throttle (mechanical). See the Throttle and the Throttle Quadrant.

The wing-sweep hat on the right throttle is normally set to AUTO enabling CADC control of the wings, this is the upper position. The down position sets the wing-sweep to the BOMB mode, 55° or aft.

The AFT and FWD (forward) positions enable manual movement aft of the CADC scheduled position.

The emergency wing-sweep handle on the throttle quadrant is used to control the mechanical emergency mode, see emergency mode above.

![wingsweep](../../img/wingsweep1.png)

The wing-sweep indicator to the right of the ACM panel is used to indicate the current wing-sweep positions. The pointer on the left side shows the CADC scheduled wing position. The left tape shows the manually commanded position and the right tape shows the actual wing position.

The five windows on the right side show:

- **OFF:** System inoperable.
- **AUTO:** CADC controlling wing-sweep.
- **MAN:** Wings set manually with the control on the right throttle.
- **EMER:** Wings set with the emergency wing-sweep handle.
- **OVER:** Wings in oversweep.

The relevant warning and advisory lights are located on the Vertical Display Indicator (VDI) and the pilot Caution - Advisory Indicator.

The WING SWEEP advisory light on the right side of the VDI illuminates when both wing-sweep electrical channels are inoperable or the emergency mode is in use. If it illuminates without the emergency mode being used that mode should then be used as the electrical system might not work.

The WING SWEEP caution light on the pilot caution - advisory indicator illuminates when at least one electrical wing-sweep channel is inoperable.

### Wing-Sweep System Test

The wing-sweep system can be tested on the ground in pre-flight without moving the wings using the Master Test Panel.

To conduct the test, set the wing-sweep mode to AUTO and push the MASTER RESET button. Set the MASTER TEST switch to WG SWP.

The CADC commanded position indicator on the wing-sweep indicator will now move to 44°. The WING SWEEP and FLAP light will illuminate on the pilot Caution - Advisory Indicator and the REDUCE SPEED warning light on the Vertical Display Indicator (VDI).

**Note:** The WING SWEEP advisory light will illuminate after 3 seconds into test, turn off and then illuminate again at 8 seconds.

When the CADC commanded position indicator moves forward to the 20° position the test is over and the above light will turn off. The MASTER TEST switch can now be set to OFF and the test is complete. The test will take about 25 seconds to complete.

**Note:** The RUDDER AUTH and/or MACH TRIM lights might illuminate and the control stick might move. This can be ignored.

**Note 2:** The WG SWP test on the Master Test panel is not implemented yet.



# Flight Control System

The flight control system on the F-14 Tomcat is driven by the two main hydraulic circuits, powered by pumps connected to each engine.

- **Longitudinal (pitch) control:** Both tail stabilizers are deflected in unison, acting in the same way as traditional elevators.
- **Lateral (roll) control:** Produced by both the tail stabilizers and the spoilers working in unison. To produce roll, the stabilizers are deflected opposite each other to act as ailerons in combination with the spoilers on the side to which roll is commanded.
- **Rudders:** The F-14 has a standard rudder configuration albeit in a two-tail, two-rudder configuration.

Control surface position is indicated on the Control Surface Position Indicator and can also be used to check trim position with controls at neutral.

> **Note:** Above 15 units AOA, the rudders should be used for lateral (roll) control due to the different airflow along the aircraft control surfaces.

## Trim

- **Longitudinal and lateral trim:** Accomplished via the trim hat on the Control Stick. This changes the stick neutral position, thus trimming the aircraft.
- **Rudder trim:** Accomplished via the RUDDER TRIM switch on the Inlet Ramps/Throttle Control Panel, changing the neutral rudder position.

The Mach Trim and ITS (Integrated Trim System) automatically trim to compensate for changes in longitudinal trim. The Mach Trim system compensates for transonic and supersonic trim changes, and the ITS for trim changes due to flap and speedbrake position changes.

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

The spoilers, located on the upper surfaces of the wings, are used to control roll, for braking on the ground as part of the Antiskid system, and as a part of the DLC system.

- **Spoiler malfunction:** In case of a malfunction, the spoiler symmetry protection logic disables all spoilers in the same section as the failed spoiler, either inboard or outboard. If this occurs, the SPOILERS caution light on the Caution - Advisory Indicator illuminates. To override this, set the corresponding switch on the Spoiler Failure Override to ORIDE and depress the MASTER RESET button on the Fuel Management Panel.

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

# Landing Gear System

The F-14 Tomcat has a tricycle landing gear designed to be fully retractable and hardened enough to withstand the rigors of carrier traps. The landing gear extension and retraction is powered by the combined hydraulic system and has an emergency extension system. The emergency extension system has a nitrogen bottle that can be used for a one-shot emergency extension. With the emergency system triggered, it needs to be reset by technicians on the ground to allow further normal retraction.

For additional information on controls and indicators, see the Landing Gear Control Panel for controls and the Wheels-Flaps Position Indicator for the indicators.

## Nosewheel Steering

The nosewheel steering system on the F-14 can be activated with weight on wheels by depression of the nosewheel steering button on the Control Stick. The activation of this system is indicated via the NWS ENGA caution light on the left side of the HUD, see Wheels Warning/Brakes Warnings/ACLS/AP Caution/NWS Engage Caution/Auto Throttle Caution Lights.

Disengagement of this system occurs automatically with weight off wheels (take-off), electrical supply failure, or lowering of the launch bar. It’s also possible to deactivate the system by depression of the nosewheel steering button.

The nosewheel, with the system engaged, is controlled via the rudder pedals. It’s capable of a deflection of up to 70°, meaning that it will turn tightly enough that the inner wheel will move backward.

## Wheelbrakes

The wheelbrakes can be applied either via the rudder pedals by pressing on the upper part of them, rotating them forward, or via the parking brake handle located on the Landing Gear Control Panel.

- **Rudder pedals:** Used to apply the brakes gradually.
- **Parking brake handle:** Either on or off.

Normally, both systems are supplied from the combined hydraulic system, but if that system becomes depressurized, the brake system automatically switches to the backup accumulators. The Emergency Brake Pressure Indicator shows current pressure in the emergency accumulators.

- **Auxiliary accumulator:** Allows for about 13 to 14 wheelbrake applications from the pedals and the parking brake accumulator 3 parking brake applications minimum. These accumulators can be recharged via the Hydraulic Hand Pump.

- **BRAKES warning light:** On the left side of the HUD, indicates either parking brake applied, antiskid system fail, or that the brakes are operating in the emergency mode (only when the pedals are depressed).

## Antiskid

The antiskid system modulates the wheelbrakes to prevent skidding while on the ground. When armed in the air, the system prevents braking until both main wheels are on the ground and the wheels have spun up. The system is not operational below 15 knots.

- **Switch:** The antiskid system switch also controls the spoiler brake system that deploys the spoilers as brakes when the throttles are set to IDLE while on the ground.

> **Note:** The antiskid should be disabled during taxi as below 15 knots, the system may disturb normal braking even though the antiskid feature is not operational at those speeds.

- **ANTI SKID SPOILER BK switch:** On the Fuel Management Panel, controls the system. OFF disables the system, BOTH enables antiskid and the spoiler brake system, and SPOILER BK enables only the spoiler brake system.

## Catapult Launch and Arresting Gear

### Nosegear Catapult System

The nosegear of the F-14 contains the system allowing for catapult-assisted takeoff during carrier-based operations.

- **Components:** Nosewheel kneel functionality, launch bar, and holdback fitting.
- **Kneel:** Enable the system by kneeling the aircraft using the NOSE STRUT switch on the Landing Gear Control Panel. Hold the switch to the KNEEL position until downward movement stops. This drains hydraulic fluid from the shock absorber, compressing the nosegear strut 14 inches. When compressed, this also releases the lock on the launch bar, which can then be lowered manually by the deck crew or by turning the nosegear more than 10° from center.
  
  > **Note:** In DCS, the launch bar is automatically lowered with nosegear kneel.

- **Connection:** The aircraft can then be guided onto the catapult and connected to the shuttle, in DCS via default keybind U. The holdback bar is currently not modeled in DCS.
  
  > **Note:** Deselection of nosewheel steering should be done before final movement onto the shuttle and hookup to avoid misalignment.

- **Launch:** The final command to launch the aircraft, after proper procedures, is to salute the “shooter” or officer in command of catapult launch, default keybind Left Shift + U in DCS.

- **Post-launch:** After the catapult stroke, when the launch bar is released from the shuttle, stored hydraulic energy is released to impart a positive pitch moment to the aircraft. This also automatically raises the launch bar into its stowed position.

- **Indication:** The launch bar status is indicated on the Caution - Advisory Indicator via the LAUNCH BAR advisory light. The advisory light is on with weight on wheels when the launch bar is not up and locked and turns off if throttles are advanced to MIL to enable a lights-out for launch criteria. With weight off wheels, the LAUNCH BAR advisory light is on if the nose strut hasn’t fully extended, launch bar is not up and locked, or nosewheel hasn’t centered correctly. This inhibits nosegear retraction.

- **Launch Bar Abort Panel:** Contains the LAUNCH BAR switch used to disengage the launch bar in case of an aborted launch. This functionality is currently not implemented in DCS; unhooking the launch bar is currently accomplished by another depression of the hookup key, default key U.

### Arresting Gear

The arresting hook located on the underside of the tail of the F-14 is used for arrested landings during carrier operations.

- **Power:** Uses hydraulic power from both flight and combined hydraulic systems and is controlled electrically, thus requiring electrical power as well.
- **Operation:** Via the arresting HOOK handle on the Arresting Hook Panel. UP raises the arresting hook, and DN, down, lowers it to 37°, allowing it to catch the wire during a correctly executed carrier “trap.” The transition light next to the arresting HOOK handle illuminates whenever the arresting hook position does not correspond with handle position.
- **Mechanical backup:** If onboard failures do not allow for normal hook lowering, it’s possible to use a mechanical backup to deploy the hook. To activate the mechanical backup, pull the handle out and rotate it 90° counterclockwise. This releases the mechanical uplock and drains the hydraulic pressure keeping the hook up, thus lowering it.

  > **Note:** Hook position also affects the AoA indexer and approach lights, making them flash with gear down if the hook is not also down. This feature can be disabled using the HOOK BYPASS switch on the Master Light Control Panel.

# ECS Environmental Control System

The ECS or environmental control system controls and supplies temperature- and pressure-regulated air to cockpit systems and cooling for electronic equipment and weapons.

- **Air source:** Sourced from the engines, one or both, or if needed from the emergency ram air door on the fuselage inboard of the right glove.

## Systems Using ECS Air

- **Cockpit systems:** Cockpit pressurization and canopy seals, anti-g suit inflation, aircrew suit ventilation, seat cushion ventilation, and windshield anti-ice and defogging.
- **Other systems:** Pressurization of external drop tanks, wing airbag seals, electronics cooling, and cooling of the AN/AWG-9 radar and AIM-54 missiles via an air/liquid heat exchanger.

## Air Source and Cockpit Air Controls

- **Air source controls:** Set using the controls on the Air Conditioning Control Panel.
  - **L ENG:** Set air source to the left engine.
  - **R ENG:** Set air source to the right engine.
  - **BOTH:** Set air source to both engines (normal position while in use).
  - **RAM and OFF:** Enable the emergency ram door, but OFF turns off pressurization and heating.

- **Temperature control:** During normal operation, temperature in the cockpit is controlled using the TEMP switch and thumbwheel on the same panel. The thumbwheel sets the temperature, which is automatic regardless of airspeed and altitude if the TEMP switch is set to AUTO. If that switch is set to MAN, manual, it will vary depending on airspeed and altitude.

- **Cockpit pressurization:** The CABIN PRESS switch controls the cockpit safety valve, controlling whether the cockpit is pressurized or not. If set to NORM, cockpit pressure is at 8,000 feet up to 23,000 feet and after that 5 psi higher than the atmosphere outside. DUMP depressurizes the cockpit by opening the cockpit safety valve.

- **Cockpit air supply modulation:** The RAM AIR switch is used to modulate cockpit air supply temperature when the ram air door is in use by opening and closing the emergency ram air door. In this mode, that air is mixed directly with hot bleed air from the engines. INCR, increase, opens the ram door, decreasing temperature, and DECR closes the door and increases temperature. Spring-loaded to center.

  > **Note:** Selection of RAM or OFF inhibits gun firing.

- **Cabin air pressure altitude:** Shown on the Cabin Pressure Altimeter in front of the pilot control stick.

- **Caution lights:** 
  - **CABIN PRESS caution light:** On the RIO Caution-Advisory Panel, indicating less than 5 psi absolute pressure or above 27,000 feet cockpit pressure.
  - **COOLING AIR advisory light:** On the same panel, indicating overheat in the electronics cooling system, indicative of a failure in the ECS which might damage the electronics.

- **Anti-g suit pressurization:** Can be tested via the G-valve Button for the pilot and G-Valve Button for the RIO. The airflow through the suit, or seats if no suits are worn, is controlled by the VENT AIRFLOW thumbwheel on the pilot Oxygen-Vent Airflow Control Panel and RIO Oxygen-Vent Airflow Control Panel respectively.

## Windshield Anti-Ice and Defogging

- **Windshield anti-ice and defogging:** Controlled via the External Environmental Control Panel and Canopy Defog/Cabin Air Lever.
  - **Windshield switch:** The WSHLD switch on the external environment panel provides hot bleed air on the outside of the windshield to clear ice and rain on the glass. AIR enables airflow over the windshield, and OFF disables it.
  - **Canopy defog:** The Canopy Defog/Cabin Air Lever (for pilot) and Canopy Defog/Cabin Air Lever (for RIO) sets the amount of air through the canopy air diffusers to be used to defog the canopy. Lever set fully to CANOPY DEFOG selects all cockpit air to be through the canopy diffusers, while lever fully at CABIN AIR redirects 30% through the canopy diffusers and the rest to the cockpit diffusers.

- **WSHLD HOT advisory light:** On the pilot Caution - Advisory Indicator illuminates when the windshield is warmer than 300°F (149°C). This automatically closes the valve and stops warm air to the windshield until cooled down.

## AN/AWG-9 and AIM-54 Cooling

- **Cooling:** The AN/AWG-9 radar and AIM-54 missiles are liquid-cooled via independent liquid/air heat exchangers cooled by ECS air.
  - **Control:** The Liquid Cooling Control Panel controls these cooling systems and should be set to AWG-9 to enable only the AN/AWG-9 cooler if no AIM-54 Phoenix missiles are carried. If AIM-54 missiles are loaded, AWG-9/AIM-54 should instead be set to enable both systems. OFF turns off both systems and should not be set with systems in use as they will overheat.

- **Caution lights:**
  - **AWG-9 COND advisory light:** On the RIO Caution-Advisory Panel, indicates overheat in the AN/AWG-9 cooling system, continuing use of the AN/AWG-9 might damage it.
  - **MSL COND advisory light:** Indicates overheat in the AIM-54 cooling system or operation of the WCS with AIM-54s loaded and liquid cooling switch not set to AWG-9/AIM-54.

## External ECS Air Supply

For operation of systems requiring cooling on the ground or on deck, it’s possible to connect an external ECS air source to cool them.

- **Control:** The GND CLG switch on the IFF Antenna Control/Test Panel panel at the RIO right side console controls what is to be cooled:
  - **OBC/CABIN:** Provides the external ECS air to the cabin and all air-cooled electronics. This setting disables the AN/AWG-9 transmitter due to inadequate cooling.
  - **AWG-9/AIM-54:** Provides the external ECS air to the AN/AWG-9 and AIM-54 heat exchangers and to related electronics.
  - **OFF:** Turns off the external ECS air supply and is the normal mode used when the engines are running.

  > **Note:** Any setting on the GND CLG other than OFF should not be used when the engines are running.

  > **Note2:** For the Heatblur F-14 in DCS, the external ECS air supply is connected via the same command as the engine starter air.

# Oxygen System

The F-14 carries one or two 10-liter liquid oxygen bottles providing oxygen to the crew when needed.

- **Control:** The oxygen supply is controlled on the pilot Oxygen-Vent Airflow Control Panel and RIO Oxygen-Vent Airflow Control Panel respectively. Both panels contain an OXYGEN switch that sets oxygen supply to ON or OFF.
- **Indicator:** Liquid oxygen remaining is shown on the Liquid Oxygen Quantity Indicator on the pilot’s right side console. The gauge shows remaining liters of liquid oxygen up to 20 liters (if two bottles are installed). The indicator is electrically driven, and if it receives no power, an OFF flag will be visible, and it will display 0 liters remaining.
- **Caution light:** The RIO Caution-Advisory Panel has the OXY LOW caution light which illuminates when the liquid oxygen quantity is below 2 liters.

  During the INST test on the ref:MTPanel, the liquid oxygen meter shows 2 liters, and the OXY LOW caution light illuminates.

# Flight Instruments

Apart from the VDIG (HUD and VDI), the F-14 is equipped with:
- Two Standby Attitude Indicators
- Two Airspeed Mach Indicators
- Two Servopneumatic Altimeters
- A Vertical Velocity Indicator
- A Turn and Slip Indicator
- An Accelerometer
- A Standby Compass
- Two mechanical clocks

The types that have two installed have one installed on the RIO instrument panel as well as the pilot one.

All of these instruments that need electrical power are connected to the essential buses, meaning that they can be powered by the emergency generator if the main ones fail.

For more info on the instruments, see their respective cockpit panel descriptions linked above.

# Canopy

The rear-hinged F-14 canopy is operated hydraulically and pneumatically. Controls are present in both the pilot and RIO cockpits.

See Canopy Control Handle or Canopy Control Handle for the controls.

The CANOPY caution light on both the pilot Caution - Advisory Indicator and the RIO Caution-Advisory Panel illuminates if the canopy is not in the down and locked, secured position.

# Ejection System

The F-14 Tomcat is equipped with dual Martin-Baker GRU-7A rocket-assisted ejection seats, one for the pilot and one for the RIO. The ejection system is a zero/zero system, capable of successfully ejecting the crewmembers at zero airspeed, stationary, on the ground.

- **Ejection command lever:** This lever, located in the RIO cockpit, selects if the RIO ejects the pilot as well when he ejects. The lever is situated beside the sensor control panel, see Eject Command Lever. When set to PILOT, the pilot ejects both crewmembers, while the RIO ejects only himself. When set to MCO, both crewmembers eject both crewmembers.

  The system does not allow pilot-only ejection because it would be undesirable for the RIO to remain in the aircraft alone.

- **Indicator:** The pilot has an indication of what position the ejection command lever is at on the Landing Gear Control Panel, the EJECT CMD flip-flop indicator showing PILOT when the lever is in the pilot and MCO when in MCO.

- **Canopy jettison:** If the canopy does not jettison when initiating the ejection sequence, it’s possible to manually jettison it using the Canopy Jettison Handle in the pilot cockpit or the Canopy Jettison Handle in the RIO cockpit. If the canopy inhibited ejection after ejection initiation, jettisoning the canopy will most likely restart it. If ejection is needed during a flat spin, it’s also recommended to manually jettison the canopy and allow it to clear before initiating the ejection sequence as the canopy might need longer to clear during a flat spin.

# Lighting System

The F-14 Tomcat lighting system consists of the internal and the external lights.

## Internal Lighting

The internal lights are the red instrument panel and console lights, red and white floodlights, and a movable utility light at both crew stations.

- **Red instrument panel and console lights:** Normally used during nighttime, they back-light all instruments and controls, allowing their use while impacting night vision minimally.
- **Floodlights:** Allow for additional lighting of the cockpit panels, but care should be taken to avoid affecting night vision.
- **Utility lights:** Movable and can be used to illuminate a specific spot and as a map or reading light.

  Controls for the internal lights are on the Master Light Control Panel in the pilot cockpit and Interior Light Control Panel in the RIO cockpit, each controlling their own cockpit lighting.

  > **Note:** The utility light function is not modeled in DCS, but the flashlight function, default keybind Left Alt + L, which moves with the cursor, can be used, providing a similar function.

## External Lighting

The external lights are the position lights, the anticollision lights, the formation lights, the taxi light, the approach lights, and the refueling probe light.

- **Position lights:** Located on the left wing tip (red), right wing tip (green), top aft of the left vertical stabilizer (white), and upper and lower lights on the wing gloves on each side (red on the left glove and green on the right). The glove lights are additional lights supplementing the wing tip lights. When the wings are swept forward of 25°, the wing tip lights are active, and when aft of 25°, the glove lights are active instead. With the gear down, wings forward of 25°, and the position lights in steady mode, both the glove and wingtip position lights are lit. When the anticollision lights are on, the position lights can only operate in the steady mode; otherwise, they can be set to flash.

- **Anticollision lights:** Located on the chin pod or TCS pod, top front of the left vertical stabilizer, and top aft of the right vertical stabilizer. The anticollision lights are all red flashing lights. The chin pod-mounted lower light only operates while the nosegear wheel door is closed.

- **Formation lights:** Dim green lights used for formation flight, which can be dimmed gradually. They are located on the aircraft nose (behind the radome), the wing tips, on the fuselage aft of the wings, and on the top edge of the vertical stabilizers. All are duplicated on both sides of the aircraft.

- **Taxi light:** A fixed headlight located on the nosewheel strut. It’s automatically turned off with gear retraction if set to on.

- **Approach lights:** Located on the nosewheel strut and replicate the AoA indexer for the LSOs during carrier traps.

- **Refueling probe light:** Used to illuminate the refueling probe and is automatically enabled with probe extension.

  All external light controls are located on the Master Light Control Panel, except for the exterior lights switch on the left throttle (see Throttle), which disables or enables all external lights apart from the approach lights.

# Jettison System

The Jettison system has four modes of operation: emergency, ACM, selective, and auxiliary.

## Emergency Jettison

The emergency jettison is selected via the EMERG STORES JETT on the Landing Gear Control Panel. Selection causes the EMERG JETT caution light to illuminate on the pilot Caution - Advisory Indicator.

- **Requirement:** The emergency jettison requires only no weight on wheels indicated (no master arm) and ejects all stores except for Sidewinders.

## ACM Jettison

The ACM jettison is selected via the ACM JETT button under the ACM cover/switch on the Air Combat Maneuver Panel.

- **Requirement:** The ACM jettison, like the emergency jettison, requires no master arm but instead requires that the landing gear lever is up. Unlike the emergency jettison, the ACM jettison only ejects those stations selected by the RIO on the Armament Panel (set to SEL or B for stations 1 and 8).

## Selective Jettison

The selective jettison is set and executed by the RIO on the Armament Panel. This mode of jettisoning requires the landing gear handle to be in the up position and the master arm to be on.

- **Procedure:** To jettison in selective mode, set the desired station switches to SEL and hold the SEL JETT switch to JETT.

## Auxiliary Jettison

The auxiliary jettison mode is a backup mode to use when the other modes have failed. Like the selective jettison mode, it requires the landing gear handle to be up and the master arm to be on.

- **Limitation:** This mode can only eject air-to-ground stores and ejects them by actuating the normal release hooks. This means that the aircraft needs to fly straight and level as the stores are not ejected forcefully but instead just released and cleared using gravity.

> **Note:** No jettison mode can jettison ITERs or stores loaded on those; they need to be dropped like normal, with or without the fuzes armed.


# CADC Central Air Data Computer

The Central Air Data Computer or CADC is the computer acting as the spider in the web for most aircraft flight sensors and relaying this information to all systems needing them. In addition, it also controls the wing-sweep via the wing-sweep schedule and also controls the flaps and slats as they are limited by that same schedule.

# AN/AWG-9 Weapon Control System (WCS)

The AN/AWG-9 weapons control system (WCS) is an integrated system containing the F-14’s main sensors and computer providing detection, tracking, and engagement of targets in the air-to-air and air-to-ground roles.

## Detail Data Display (DDD) and Panel

![DDD Panel](images/dddpanel.png)

The DDD is the main control panel and display for the radar part of the AN/AWG-9 system. It contains all the controls for the radar except the scan volume and stabilization controls which are on the sensor control panel.

## TGTS, MLC, AGC and PARAMP Switches

The upper left part of the DDD panel contains four switches (1-4) controlling amplification, mainlobe clutter (MLC) suppression, and target size parameters.

| Switch | Function |
|--------|----------|
| **TGTS (targets) switch** | Selects expected target size used by the WCS to calculate missile launch zones and set parameters for target tracking in the radar. Sets the range at which the missile ATC is sent: SMALL (6NM), NORM (10NM), LARGE (13NM). Incorrect setting might negatively affect target tracking and engagement. |
| **MLC switch** | Controls how the system suppresses the MLC in the radar system while in pulse doppler mode. OUT disables the system, IN enables it, and AUTO enables the MLC filter if the antenna look-up angle is less than 3°. |
| **AGC switch** | Controls the automatic gain control used in the pulse doppler modes. NORM uses a longer time constant for amplification; FAST is used in jammed or heavy clutter environments but can make the radar less sensitive to real targets. |
| **PARAMP (parametric amplifier) switch** | Allows manual control of the parametric amplifier to amplify weaker targets in all radar modes. Disabling PARAMP reduces detection range by approximately 35%. |

**Note**: AGC, PARAMP, and TGTS switches are currently not implemented.

## AWG-9 Range Selection and Tracking Indication

In the upper central part of the DDD panel are the controls and indicators for setting the radar range in search modes and indicators for radar tracking in single target track (STT) modes.

**Range buttons**:
- Six round buttons (8), labeled 5, 10, 20, 50, 100, and 200, set desired radar range in pulse modes and IFF range.
- The range display drum (7) shows currently displayed scale on the DDD for pulse modes, blank in pulse-doppler modes, and ±10 in STT modes.

**Radar track indicator lights**:
- **ANT TRK**: Indicates the radar is tracking the target angle (azimuth and elevation).
- **RDROT**: Indicates the target is in the range or rate gate.
- **JAT**: Indicates the antenna is tracking a jamming source’s angle.
- **IROT**: Indicates target angle tracking via TCS.

## IR AUDIO Controls

The IR AUDIO controls (10-12) in the upper right part of the DDD panel were used with the original IR-sensor and are non-functional in modeled F-14 versions.

## Radar and Missile Frequency Selectors

Thumbwheels in the upper rightmost part of the DDD panel control the AN/AWG-9 radar emitter’s frequency (13) and the missile control channel for AIM-7 and AIM-54 (14). 

**Note**: Non-functional in DCS currently.

## Radar Mode Selectors

In the lower right part of the DDD panel are controls for display mode and radar mode and its indicator drum.

| Button | Function |
|--------|----------|
| **Display mode buttons (15)** | RDR, radar, mode is normally selected. IR mode is non-functional as the IR system is not installed. IFF button enables the IFF interrogator in one of its two operational modes. |
| **Radar mode buttons (16)** | STT buttons: PD STT (pulse-doppler STT) and P STT (pulse STT). Search buttons: PD SRCH (pulse doppler search), RWS (range-while-search), TWS AUTO and TWS MAN (track-while-scan), PULSE SRCH (pulse search). |

**Indicator drum (17)**:
- Shows currently selected radar mode: TWS MAN, TWS AUTO, RWS, MRL (manual rapid lockon), A-G (air-to-ground), VSL (vertical scan lockon), OPTTRK (TCS track), PLM (pilot lockon mode), PULSE (pulse search and pulse STT), PD (pulse doppler search and PD STT), and PAL (pilot automatic lockon mode).

## Aspect and Vc Switches

Located on opposite sides of the DDD:

**Vc switch (18)**:
- Controls the rate scale on the DDD in pulse doppler search modes: X-4 (800 knots opening to 4,000 knots closing), NORM (200 knots opening to 1,000 knots closing), VID (50 knots opening to 250 knots closing).

**ASPECT switch (21)**:
- Controls rate processing windows of the radar in pulse doppler search modes and tracking mode in pulse STT modes: NOSE (600 knots opening to 1,800 knots closing), BEAM (1,200 knots closing to 1,200 knots opening), TAIL (1,800 knots opening to 600 knots closing).

## Elevation Indicator

The elevation indicator scale (22) shows sensor elevations:

- **RDR needle**: Indicates current radar elevation in search modes.
- **IR/TV/EC needle**: Displays elevation center of the antenna scan pattern if HCU is set to RDR; shows current TCS elevation if HCU is set to IR/TV.

## Counter-Countermeasure Mode Controls

In the lower leftmost corner are three counter-countermeasure mode buttons (not currently implemented).

### Radar and DDD Control Knobs

| Knob | Function |
|------|----------|
| **PULSE VIDEO (5)** | Controls video intensity for pulse modes. |
| **BRIGHT (9)** | Adjusts brightness of the DDD. |
| **PULSE GAIN (20)** | Controls radar gain in pulse modes. |
| **ERASE (19)** | Controls the strength of the erase beam on the DDD. |
| **PD THRLD (26)** | Controls threshold for echo as contact in pulse-doppler modes. |
| **JAM/JET (24)** | Sets jamming intensity signal threshold. |
| **ACM THRLD (25)** | Sets threshold for target at ACM ranges. |

**Note**: JAM/JET and ACM THRLD not currently implemented in DCS.

## Detail Data Display

**Pulse**:
![Pulse Search](images/PSEARCH.png)
![Pulse STT](images/PSTT.png)

**Pulse-Doppler**:
![Pulse-Doppler Search](images/PDSEARCH.png)
![Pulse-Doppler STT](images/PDSTT.png)

The DDD screen shows radar returns and symbology depending on radar mode. 

**Pulse search mode**: Displays radar returns as range vs azimuth.
**Pulse doppler modes**: Adds AGC TRACE at the bottom indicating jamming intensity; displays rate vs azimuth.
**STT modes**: Shows target return, tracking gates, closing rate, and attack symbology if a missile is selected.

**Note**: AGC TRACE not yet implemented.

## Tactical Information Display (TID) and Associated Controls

![TID](images/tid1.png)

The TID is the main data display for the WCS, showing a tactical picture for identifying and selecting targets for long-range weapons.

**TID Display Control Knobs**:
- **Left knob**: Controls TCS display contrast.
- **Right knob**: Controls overall brightness of the TID.

**INS and Navigational Controls**:
- **INS status display (1)**: Indicates status of the INS and its alignment.
- **Left selector knob (12)**: Controls INS or AHRS mode and allows for INS alignment.
- **Right selector knob (6)**: Controls the source used for destination steering.

**TID Data Readout Drum**:
- Indicates the source of data displayed on the TID text readouts (WAY PT, ST, FIX PT, IP, HB, OWN A/C, TGT 1, SYMBOL).

**TRACK HOLD and CLSN buttons**:
- **TRACK HOLD (11)**: Extends track hold function to 2 minutes.
- **CLSN (7)**: Enables collision steering to currently tracked target.

**TID Control Panel**:
- Contains 8 buttons for selecting symbology to show on the TID and two selector knobs for display scale and TID mode.

**TID Data Readouts**:
![TID Indicators](images/tidindicators.png)

| Indicator | Function |
|-----------|----------|
| **Buffer Register** | Shows data currently being entered into the WCS. |
| **Data Readouts** | Displays data from hooked tracks or own aircraft. |
| **Computer Run Indicators** | Shows WCS program cycles. |
| **Antenna Elevation** | Shows radar antenna elevation. |
| **Scan Pattern Limits** | Shows altitude limits of selected scan pattern. |
| **Navigation Status** | Shows status of the navigation system. |
| **Target Closing Rate** | Shows closing rate of STT or TWS hooked target. |
| **Selected Weapon** | Indicates selected air-to-air weapon. |

### TID Symbology

| Element                                             | Shape             | Function                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Center Dot**                                      | ![Image](images/1.png)  | Marks coordinates of symbol, basic component of all symbols representing a coordinate.                                                                                                                                                                                                                                                                                                                                              |
| **Own Aircraft**                                    | ![Image](images/2.png)  | Symbol representing own aircraft. Antenna scan limits, jamming strobes emanate from this symbol. Moves and has a velocity vector in ground stabilized mode. Stationary in aircraft stabilized and attack modes. If the symbol moves outside of TID presentation a line is drawn from the center of the display to the edge of the display indicating direction of the own aircraft symbol.                                             |
| **TID Cursor**                                      | ![Image](images/26.png) | Circle used as a hook cursor. Controlled by the HCU when in TID mode. Half-action on the HCU enables display of the symbol and also enables the HCU stick to move the cursor. The cursor location is set by stick deflection. Full-action on the HCU hooks (selects) the closest symbol if one is present within 0.125 inches of cursor center. The hooked symbol gets brighter to indicate hook.                                              |
| **TWS Steering Centroid**                           | ![Image](images/27.png) | Steering centroid of TWS tracks selected by WCS for weapons engagement.                                                                                                                                                                                                                                                                                                                                                             |
| **Unknown Onboard Sensor Target**                   | ![Image](images/3.png)  | Unknown sensor track in RWS, TWS, and STT modes.                                                                                                                                                                                                                                                                                                                                                                                    |
| **Hostile Onboard Sensor Target**                   | ![Image](images/4.png)  | Track in TWS and STT modes designated as hostile by RIO.                                                                                                                                                                                                                                                                                                                                                                            |
| **Friend Onboard Sensor Target**                    | ![Image](images/5.png)  | Track in TWS and STT modes designated as friendly by RIO.                                                                                                                                                                                                                                                                                                                                                                           |
| **Angle-Tracked Radar Target**                      | ![Image](images/6.png)  | Radar target tracked only in angle (jamming target).                                                                                                                                                                                                                                                                                                                                                                                |
| **Angle-Tracked Radar Target with Altitude Difference** | ![Image](images/7.png)  | Radar target being tracked in angle only and range being computed by altitude difference ranging.                                                                                                                                                                                                                                                                                                                                   |
| **TCS-Angle Tracked Target**                        | ![Image](images/10.png) | Target being tracked in angle by TCS.                                                                                                                                                                                                                                                                                                                                                                                               |
| **TCS-Angle Tracked Target with Altitude Difference**   | ![Image](images/11.png) | Target being tracked in angle by TCS and range being computed by angle difference ranging.                                                                                                                                                                                                                                                                                                                                          |
| **Unknown Data Link Target**                        | ![Image](images/12.png) | Data link track identified as unknown by source.                                                                                                                                                                                                                                                                                                                                                                                    |
| **Hostile Data Link Target**                        | ![Image](images/13.png) | Data link track identified as hostile by source.                                                                                                                                                                                                                                                                                                                                                                                    |
| **Friend Data Link Target**                         | ![Image](images/14.png) | Data link track identified as friendly by source.                                                                                                                                                                                                                                                                                                                                                                                   |


| **Manually Entered Reference Points**               |                   |                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Home base**                                       | ![Image](images/15.png) | Waypoint representing home base, carrier or airfield.                                                                                                                                                                                                                                                                                                                                                                               |
| **Waypoint**                                        | ![Image](images/16.png) | WCS navigational waypoint, supplanted by number indicating waypoint 1, 2 or 3.                                                                                                                                                                                                                                                                                                                                                      |
| **Defended Point**                                  | ![Image](images/17.png) | Waypoint used to show area to protect.                                                                                                                                                                                                                                                                                                                                                                                              |
| **Fixed Point**                                     | ![Image](images/18.png) | Generic fixed-point waypoint.                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Hostile Area**                                    | ![Image](images/19.png) | Waypoint indicating a hostile area.                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Surface Target**                                  | ![Image](images/20.png) | Waypoint indicating a surface target.                                                                                                                                                                                                                                                                                                                                                                                               |
| **IP**                                              | ![Image](images/21.png) | Waypoint used for air-to-ground engagement, see Computer Initial Point.                                                                                                                                                                                                                                                                                                                                                             |


| **Data Link Reference Points**                      |                   |                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Home Base**                                       | ![Image](images/22.png) | Data link waypoint representing home base.                                                                                                                                                                                                                                                                                                                                                                                          |
| **Waypoint**                                        | ![Image](images/23.png) | Data link generic waypoint.                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Data Link Fixed Point**                           | ![Image](images/24.png) | Data link waypoint representing a fixed point.                                                                                                                                                                                                                                                                                                                                                                                      |
| **Data Link Surface Target**                        | ![Image](images/25.png) | Data link waypoint representing a surface target.                                                                                                                                                                                                                                                                                                                                                                                   |

| **Position Symbol Modifiers**                       |                   |                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mandatory Attack**                                | ![Image](images/28.png) | Additional symbology on a TWS track (horizontal bar through center dot) selected as mandatory attack by the RIO. Only one target can be designated thusly and always receives an engagement priority number.                                                                                                                                                                                                                       |
| **Data link Destroy**                               | ![Image](images/29.png) | Additional symbology on a data link track (horizontal bar through center dot) designated to be destroyed by data link source. Does not affect target prioritization in WCS.                                                                                                                                                                                                                                                         |
| **Do Not Attack**                                   | ![Image](images/30.png) | Additional symbology on a TWS or data link track (vertical bar through center dot) designated as do not attack (by RIO) or disengage (via data link). If set by RIO removes target from WCS target prioritization.                                                                                                                                                                                                                   |
| **Multiple Targets**                                | ![Image](images/31.png) | Additional symbology on a TWS or data link track (horizontal bar on left side of symbol) indicating that the track represents multiple targets. Can be set manually by RIO or received via data link.                                                                                                                                                                                                                                |
| **Data Link Challenge**                             | ![Image](images/32.png) | Additional symbology on a data link track (small V with apex at center dot) representing data link command to visually identify target.                                                                                                                                                                                                                                                                                             |
| **Track Extrapolated**                              | ![Image](images/33.png) | Additional symbology on TWS or STT track (small X with center at center dot) indicating that no update to target has occurred within 8 seconds. Track will be deleted after 14 seconds or 2 minutes if track hold function is enabled.                                                                                                                                                                                              |
| **Hooked Symbol**                                   | Symbol brightens   | When a symbol is hooked by HCU or CAP functions it brightens to indicate hook.                                                                                                                                                                                                                                                                                                                                                      |
| **Target Under Missile Attack**                     | Symbol brightens   | In TWS and STT symbols of tracks being engaged by own aircraft brightens during computed missile flight time plus 15 seconds to indicate missile engagement in progress.                                                                                                                                                                                                                                                            |
| **Target in Optimum Missile Launch Zone**           | Symbol blinks      | In TWS and STT symbols, launch zones and firing order numerics of target tracks blink when time to optimum missile range is less than 8 seconds.                                                                                                                                                                                                                                                                                    |
| **Altitude Numerics**                               | ![Image](images/34.png) | When altitude numerics are selected for display a number on the left side of the tracks indicate track altitude to nearest ten thousands of feet. The number four as an example indicates an altitude between 35,000 and 45,000 feet. Available on radar and data link tracks.                                                                                                                                                       |
| **Firing Order Numerics**                           | ![Image](images/35.png) | Indicates AIM-54 phoenix target prioritization (1 to 6) in WCS when in the TWS mode. Next missile launch will target track with number 1 and remove the number from that track to advance the other 5 track numbers one step to prepare for next launch. Mandatory attack selection on a target forces the WCS to always include that target in the prioritization. Next launch selection automatically sets hooked target as number one. |
| **Time-to-Impact (TTI)**                            | ![Image](images/47.png) | After AIM-54 launch the firing order number on a track is replaced with the TTI or time-to-impact indication, showing WCS calculated time until missile intercepts the target track. When the AIM-54 active command is sent the TTI numbers flash to indicate this.                                                                                                                                                                   |
| **Velocity Vector**                                 | ![Image](images/36.png) | Velocity vector emanating from center dot of tracks when velocity vector display is selected. Vector direction represents track heading and length represents track speed so that the max indicated speed (1,800 knots) is 1.5 inches on the TID. In TID ground stabilized mode the vector direction represents track true heading and the vector length represents track ground speed.                                                 |
| **Launch Zone Vectors**                             | ![Image](images/37.png) | ![Image](images/lzv.png) TUMR (Time Until Minimum Range), TUOR (Time Until Optimum Range) and TUIR (Time Until In-Range/Maximum Range). The launch zone vectors are activated manually by the RIO or when time to maximum launch range is less than 60 seconds and replaces the normal track velocity vectors.                                                                                                                      |
| **Jamming Strobe**                                  | ![Image](images/38.png) | Line extending from own aircraft symbol to edge of TID to indicate a jammer exceeding the set JAM/JET threshold.                                                                                                                                                                                                                                                                                                                    |
| **Radar Antenna Scan Pattern Azimuth Limits**       | ![Image](images/39.png) | The limits of the radar scan pattern in azimuth is displayed as two dashed lines extending from own aircraft symbol. Each dash and space represent 20 nautical miles each in all radar modes. In STT the two lines converge to a single tracking strobe to indicate that the antenna tracks a single target.                                                                                                                                                                 |
| **Data Link Jamming Strobe**                        | ![Image](images/40.png) | Jamming strobe received via data link indicated by a line emanating from a data link point towards the jammers direction.                                                                                                                                                                                                                                                                                                           |
| **Data Link Pointer**                               | ![Image](images/41.png) | Brightened cursor (circle) around a data link track used to indicate data link operator concern about the specific track.                                                                                                                                                                                                                                                                                                           |
| **Data link Priority Kill**                         | ![Image](images/42.png) | Additional symbology on a data link track indicating a target that must be destroyed. Will not by itself affect WCS prioritization.                                                                                                                                                                                                                                                                                                 |
| **Artificial Horizon**                              | ![Image](images/43.png) | Artificial horizon on TID representing aircraft roll and pitch. Angle of the line represents roll and vertical deflection on display represents pitch.                                                                                                                                                                                                                                                                               |
| **Steering Guidance Symbol**                        | ![Image](images/44.png) | Symbol representing steering error from optimal missile launch direction. Should be placed by the pilot as near as possible to the center of the ASE circle and at launch should be inside of that same circle.                                                                                                                                                                                                                     |
| **Allowable Steering Error Circle**                 | ![Image](images/45.png) | ASE circle used to indicate the allowable steering error for missile launch. Size varies with attack geometry, mode and selected missile.                                                                                                                                                                                                                                                                                           |
| **Breakaway Indication**                            | ![Image](images/27.png) | Large cross appearing in the center of the TID when target range is less than minimum missile launch range or gun firing range.                                                                                                                                                                                                                                                                                                     |


## Navigation Command and Control Grid (NAV GRID)

![NAV GRID](images/navgrid.png)

The NAV GRID enables easy navigation and CAP control from a common fixed reference point (YY). It allows TID readout of bearing and range from YY and displays a grid extending from YY along a set threat axis.

**NAV GRID entry**:
1. Set the TID MODE knob to GND STAB.
2. Select D/L category on the CAP CATEGORY knob.
3. Select the CAP MESSAGE button corresponding to NAV GRID.
4. Enter grid coverage angle using the ALT/4 button on the CAP.
5. Enter numbers of grid sectors using the NBR/2 button on the CAP.
6. Enter YY location using the LAT/1 and LONG/6 or RNG/5 and BRG/0 CAP buttons.
7. Enter the threat axis using the HDG/8 CAP button.

**NAV GRID exit**:
- Deselect the CAP MESSAGE button corresponding to NAV GRID under the D/L category on the CAP.

**NAV GRID in DCS**:
- YY set to mission bulls-eye for your faction and threat axis set from YY to first valid waypoint at hot spawning.
- Jester must be commanded to adjust these parameters via the Jester wheel in cold starting with Jester.

## Hand Control Unit (HCU)

![HCU](images/hcu1.png)

The HCU is the main input controlling the RIO WCS displays. It contains power controls and indicators for the WCS and TCS in addition to the stick and its controls.

**HCU Power Controls and Indicators**:
- **IR/TV overtemp indicator (2)**, **power reset indicator (4)**, **WCS power indicator (6)**.
- **IR/TV switch (1)**: Controls power to the TCS.
- **WCS XMT switch (7)**: Controls power to the WCS computer system and displays.

**HCU Mode buttons (12)**:
- **IR/TV**: Selects TCS mode.
- **RDR**: Selects radar mode.
- **DDD CURSOR**: Selects DDD cursor mode.
- **TID CURSOR**: Selects TID cursor mode.

**HCU Control Stick**:
- **Action trigger switch (11)**: Controls cursor display and super search acquisition mode.
- **Elevation vernier control (10)**: Fine tunes sensor elevation.
- **OFFSET button (9)**: Offsets TID tactical displays.
- **MRL button (8)**: Enables manual rapid lockon mode.

**Stick modes**:
- **TCS mode**: X (up/down) controls TCS elevation, Y (left/right) controls TCS azimuth.
- **Radar mode**: X controls range or rate, Y controls azimuth.
- **Cursor modes**: X controls up/down, Y controls left/right.

### Computer Address Panel (CAP)

![CAP](images/cap1.png)

The CAP is the RIO’s main interface for controlling and entering/reading data into/from the WCS computer.

**Numeric Keypad (3)**:
- **CLEAR**, **ENTER** buttons and **S/W**, **N/E** prefixes for coordinates.
- **Key functions**:
  - **1**: LAT
  - **2**: NBR
  - **3**: SPD
  - **4**: ALT
  - **5**: RNG
  - **6**: LONG
  - **8**: HDG
  - **0**: BRG

**CAP Message Matrix Indicator Drum and buttons**:
- **BIT (Built in Test)**: Not currently implemented.
- **SPL (Special)**: Contains various functions.
- **NAV (Navigation)**: Used for navigational fixes and updating data.
- **TAC DATA (Tactical Data)**: Controls hooks and selections for WCS waypoints.
- **DATA LINK**: Used for RIO data link responses.
- **TARGET DATA**: Modifies hooked track symbols.

**Program Restart Button**:
- **PRGM RESTRT**: Resets the currently running program in case of a computer hang-up.

**Data Readout/Entry Procedure**:
- Selection of symbol/function -> Prefix selection for display -> Data entry.

### Sensor Control Panel

![Radar and IR Control Panel](images/radarircontrol1.png)

The sensor control panel contains the main controls for the AN/AWG-9 radar antenna scan patterns and various TCS controls.

**Antenna Search Pattern Selection**:
- **STAB (stabilization) switch**: Stabilizes antenna scan pattern relative to horizon.
- **AZ CTR (azimuth control) and EL CTR (elevation control) knobs**: Set scan pattern centerpoint.
- **AZ SCAN (azimuth scan) and EL BARS (elevation bars) selector knobs**: Control size of antenna scan pattern.
- **VSL switch**: Activates vertical scan lockon acquisition mode.

**TCS Controls**:
- **SLAVE switch**: Slaves one sensor to the other.
- **TCS TRIM knobs**: Calibrate TCS line of sight.
- **ACQ (acquisition) switch**: Controls TCS lockon mode.
- **FOV (field of view) switch**: Sets TCS field of view.

## AN/AWG-9 Radar

The AN/AWG-9 radar in the F-14 is a multi-mode pulse doppler radar designed for long-range target detection and missile guidance.

**Radar Modes**:
- **Pulse**:
  - **Pulse Search**: Medium range search and detection.
  - **Pulse STT**: Short to medium range single target track and missile launch.

- **Pulse Doppler**:
  - **Pulse Doppler Search**: Long range search and detection.
  - **Range While Search**: Long range search, detection, and ranging.
  - **Track While Scan**: Long range search, detection, multiple target track, and missile guidance.
  - **Pulse Doppler STT**: Long range single target track and missile guidance.

**Note**: Detection-range approximation for a 5m²-target.

**Pulse Mode**:
- **Pulse Search**: Displays radar returns as azimuth vs range.
- **Pulse STT**: Tracks a single target, displays range gates, closing rate, and attack symbology.

**Pulse Doppler Mode**:
- **Pulse Doppler Search**: Displays returns as azimuth vs rate.
- **Range While Search (RWS)**: Adds FM-ranging to measure target range.
- **Track While Scan (TWS)**: Establishes track files for up to 24 targets.
- **Pulse Doppler STT**: Tracks a single target in doppler mode, displays synthetic target marker.

### Transitional Modes

**HCU Stick in Radar Mode**:
- **Supersearch mode**: Commands antenna to ±10° search pattern.

**TWS STT Acquisition**: Attempts STT lockon from TWS mode.

**ACM Modes**:
- **Pilot Lockon Mode (PLM)**: Commands antenna to ADL, locks onto first target.
- **Vertical Scan Lockon (VSL)**: Searches -15° to +55° elevation.
- **Pilot Automatic Lockon (PAL)**: Commands antenna to 8-bar ±20° scan pattern.
- **Manual Rapid Lockon (MRL)**: Commands one-bar supersearch pattern out to 5 NM.

**TCS Slave Radar Acquisition**: Uses TCS for angle tracking, radar for range and rate.

**Transition Between STT Modes**: Allows switching between pulse STT and pulse doppler STT.

**Transition Back to Search**: Reverts radar to search mode.

### AN/APX-76 IFF Interrogator

The AN/APX-76 IFF interrogator is integrated into the AN/AWG-9 operation, used for identification of friendly targets.

**IFF interrogation**: Enabled by the IFF switch on the DDD panel.

**Returns**: Overlaid on radar returns on the DDD, indicated by two bars above and below the radar return.

## Television Camera Set (TCS)

![TCS](images/tcs.png)

The TCS replaces the IRST, providing long-range visual identification capability.

**Fields of view**:
- **Narrow (NFOV)**: 0.44° or 10X magnification.
- **Wide (WFOV)**: 1.42° or 4X magnification.

**Controls**: Managed by the RIO using the sensor control panel, DDD, TID, and HCU.
