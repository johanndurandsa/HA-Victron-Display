# HA-Victron-Display
Home Assistant Picture-Element Victron Display

Please find the Victron Background cards (I have created this in Photoshop) that you can place in /local/pictures, or your desired location and the Text file with Yuml code. This is very customizable. 

![image](https://github.com/johanndurandsa/HA-Victron-Display/assets/98578816/fa01e5ba-f9a2-4a3e-95a8-05fe75e5a0bb)

![image](https://github.com/johanndurandsa/HA-Victron-Display/assets/98578816/8982e585-4aab-4e37-acd8-97b80c91a577)

![image](https://github.com/johanndurandsa/HA-Victron-Display/assets/98578816/a252308f-fa44-4d4b-b34b-b205cd961496)

The Name: inside the code is created for each block to understand which one you working on
eg.
| name: | Description |
   | --- | --- |
   | name: Red Grid Block - Grid Name | Name on top of block. You will need code below |
   | name: Red Grid Block - Eskom Grid Watt | Grid Value from Inverter |
   | name: Red Grid Block - Load Shedding | Loadshedding stage. You will need EskomSePush (ESP) intergration |
   | name: Red Grid Block - Icon | Eskom Tower Icon on Red Block |
   | name: Red Grid Block - Line | Line between Grid and Inverter |
   | name: Victron Block - Vebus State | Verbose state on top of Inverter to show the status |
   | name: Victron Block - Icon | Yellow Icon on the Inverter |
   | name: Green AC Block - Grid Name | Name on top of block. You will need code below |
   | name: Green AC Block - AC Loads | AC Load to the house |
   | name: Green AC Block - Icon | Home Icon on Green Block |
   | name: Green AC Block - Grid Line | Line between Inverter and Home
   | name: Blue Battery Block - Battery SOC | Battery % on Blue Block |
   | name: Blue Battery Block - Battery Power | Battery Power on Blue Block |
   | name: Blue Battery Block - Battery Voltage | Battery Voltage on Blue Block |
   | name: Blue Battery Block - Battery Current | Battery Current on Blue Block |
   | name: Blue Battery Block - Icon | Battery Icon on Blue Block |
   | name: Blue Battery Block - Battery V-Line | Virtical Line to Inverter |
   | name: Blue Battery Block - Battery H-Line | Line from Battery to V-Line |
   | name: Blue Battery Block - Battery Hours Left | 
   | name: Yellow PV Block - Grid Name | Name on top of block. You will need code below |
   | name: Yellow PV Block - PV Power | Display how long the battery will last with no Power. You will need the Sensor configuration at the bottom |
   | name: Yellow PV Block - Icon | PV Icon on Yellow Block |
   | name: Yellow PV Block - PV Line | PV Line to V-Line |

# Installation
1. Download Files to you machine
2. Connect to your Home Assistant and browse to your www folder
3. Create a picture folder under www folder
4. Copy an of the 2 png files in the /local/pictures location
5. Edit your configuration 
6. Add the following code in your configuration.yaml
```
sensor:
  - platform: template
    sensors:
      #### - Value bottom Center to spesify how long the battery will last with no Power - ####
      seconds_to_hours:
        friendly_name: "Seconds to Hours"
        value_template: "{{ (states('sensor.victron_system_battery_time_to_go')|float / 3600)|round(2) }}"
        unit_of_measurement: 'hours'

      #### - Created Blank Sensor to Allow Text on Picture-Element Card - ####
      blank_blank:
        friendly_name: "Blank Blank"
        value_template: " "
```
7. Restart Home Assistant
8. Goto your Dashboard and create a new picture-element card
9. Copy and past the Victron yuml code in the text file in this new card
10. Save your card and test.
11. You can customize as your liking.

Thanks
Johann du Rand
