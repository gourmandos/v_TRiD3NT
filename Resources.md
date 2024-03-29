# Resources

## Guides

[Learn GIT](https://learngitbranching.js.org/)

[Formatting on github](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

[MarkDown - Getting started](https://www.markdownguide.org/getting-started/)

[WireViz - easy documenting for cables, wiring harnesses and connector pinouts](https://github.com/formatc1702/WireViz)

[Klipper Macros Beginners Guide](https://docs.vorondesign.com/community/howto/voidtrance/Klipper_Macros_Beginners_Guide.html)

[Klipper calculator - Calculating anything Klipper](http://docs.zerog.one/universal/klippercalculator)

[Flow Rate Calculator](https://www.advanced3dprinting.com/flow-rate-calculator/)

---

## CAD

[Voron Construct](https://github.com/PrintersForAnts/Voron-Construct)

[Voron Construct Fusion 360 Add-In](https://github.com/MapleLeafMakers/VoronConstruct360)

---

## Bed adhesive / release agent

[General Goop recipe](https://github.com/MakerBogans/docs/wiki/Printer-goop)

50% water, 50% ipa/metho, 1% pvp/pa by weight

---

## TMC driver current

Quick formula for stepper motor maximum voltage:

```
run_current = motor_peak_current * 0.707 * 0.80
```

## Automated probe accuracy testing

A collection of tests to help checking probe accuracy, precision and drift under different conditions [HERE](https://github.com/sporkus/probe_accuracy_tests)

## Input Shaping / Resonance / Belt Tension

[Klippain Shake&Tune Module](https://github.com/Frix-x/klippain-shaketune)

[Interpreting the Input Shaper Graphs ](https://klipper.discourse.group/t/interpreting-the-input-shaper-graphs/9879)

[ResHelper](https://github.com/lhndo/ResHelper)

Use Klipper to tension the belts, Discord message [HERE](https://discordapp.com/channels/712144492563791922/712144816707731456/1099543025836892281)

[Frequency testing](https://gist.github.com/kmobs/f6def5db272ca5c1b81727482f53bed8)

## Frequency Tester

Test a specific frequency that you hear when you do your resonance testing in Klipper.  
Link [HERE](https://gist.github.com/kmobs/f6def5db272ca5c1b81727482f53bed8)

## Spoolman

Keep track of your inventory of 3D-printer filament spools, see [HERE](https://github.com/Donkie/Spoolman)

## SETUP

### CanBUS / Katapult

[Esoterical guide](https://github.com/Esoterical/voron_canbus)

[How to Use CAN Toolhead Boards Connected Directly to Octopus](/other/How%20to%20Use%20CAN%20Toolhead%20Boards%20Connected%20Directly%20to%20Octopus.pdf)   -   Source [HERE](https://www.teamfdm.com/forums/topic/672-how-to-use-can-toolhead-boards-connected-directly-to-octopus-octopus-pro-on-canboot/)

[maz0r guide](https://maz0r.github.io/klipper_canbus/)

[USB to CAN bus bridge mode](https://www.klipper3d.org/CANBUS.html#usb-to-can-bus-bridge-mode)

### Fixing a wonky bed mesh

Discord message [HERE](https://discord.com/channels/460117602945990666/551488536256184331/1023369753470980197)

---

### Rotation_distance on extruders

>initial_mark_distance = initial mark on filament from the intake of the extruder body
subsequent_mark_distance = distance of mark on filament after extruding 100mm
actual_extrude_distance = <initial_mark_distance> - <subsequent_mark_distance>
actual_extrude_distance = 120mm - 20mm

```
rotation_distance = <previous_rotation_distance> * <actual_extrude_distance> / <requested_extrude_distance>

rotation_distance = 200 * 20mm / 100mm
```

### Misc
---

[Chamber Temperature & Exhaust Fan](https://github.com/eddietheengineer/VoronDocs/blob/master/setup/additional/chamber_temperature_exhaust_fan.md)

[Filament Runout Sensor](https://github.com/eddietheengineer/VoronDocs/blob/master/setup/additional/filament_runout_sensor.md)

[Fast gyroid infill](https://github.com/RomRider/klipper-FastGyroidInfill)

---

### Sensorless homing

[EZ Sensorless homing](https://github.com/kyleisah/EZ-Sensorless-Homing)

[Klipper official documentation](https://www.klipper3d.org/TMC_Drivers.html#configure-printercfg-for-sensorless-homing)

[Voron Design documentation](https://docs.vorondesign.com/community/howto/clee/sensorless_xy_homing.html)

[Finding the right StallGuard threshold](https://docs.vorondesign.com/community/howto/clee/sensorless_xy_homing.html#finding-the-right-stallguard-threshold)

---

## CALIBRATION 

[Advance resonance tuning](https://github.com/SnakeOilXY/SnakeOil-XY/blob/master/Doc/Manual/advance-resonance-tuning.md)

[Flow Calculator macros](https://github.com/agentk/klipper_macros/tree/main/FlowCalculator)

[Extrusion system Benchmark](https://github.com/CNCKitchen/ExtrusionSystemBenchmark)

[Bioshank - Flow Test Tool](https://docs.google.com/spreadsheets/d/1owDOOfIYF0fXw-70wJZLp1kmjqjqEDme/edit#gid=2039809214)

[Klippylyzer - Analyze your Klippy logs and more](https://klippylyzer.github.io/)  Github repo [HERE](https://github.com/Klippylyzer/klippylyzer#klippylyzer---analyze-your-klippy-logs-and-more)


---

## TROUBLESHOOTING

In case of under-extrusion, check that the printer/slicer is in relative and not absolute. Add M83 in the slicer if not. See Discord message [HERE](https://discord.com/channels/712144492563791922/712144816707731456/1105794634652844042)

