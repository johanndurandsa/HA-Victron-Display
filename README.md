# HA-Victron-Display
Home Assistant Picture-Element Victron Display

Please find the Victron Background cards (I have created this in Photoshop) that you can place in /local/pictures, or your desired location and the Text file with Yuml code. This is very customizable. 

![image](https://github.com/johanndurandsa/HA-Victron-Display/assets/98578816/fa01e5ba-f9a2-4a3e-95a8-05fe75e5a0bb)

![image](https://github.com/johanndurandsa/HA-Victron-Display/assets/98578816/8982e585-4aab-4e37-acd8-97b80c91a577)

![image](https://github.com/johanndurandsa/HA-Victron-Display/assets/98578816/a252308f-fa44-4d4b-b34b-b205cd961496)

The Name: inside the code is created for each block to understand which one you working on
eg.
name:
   | --- |
   | name: Red Grid Block - Grid Name |
   | name: Red Grid Block - Eskom Grid Watt |
   | name: Red Grid Block - Load Shedding |
   | name: Red Grid Block - Icon |
   | name: Red Grid Block - Line |
   | name: Victron Block - Vebus State |
   | name: Victron Block - Icon |
   | name: Green AC Block - Grid Name |
   | name: Green AC Block - AC Loads |
   | name: Green AC Block - Icon |
   | name: Green AC Block - Grid Line |
   | name: Blue Battery Block - Battery SOC |
   | name: Blue Battery Block - Battery Power |
   | name: Blue Battery Block - Battery Voltage |
   | name: Blue Battery Block - Battery Current |
   | name: Blue Battery Block - Icon |
   | name: Blue Battery Block - Battery V-Line |
   | name: Blue Battery Block - Battery H-Line |
   | name: Blue Battery Block - Battery Hours Left |
   | name: Yellow PV Block - Grid Name |
   | name: Yellow PV Block - PV Power |
   | name: Yellow PV Block - Icon |
   | name: Yellow PV Block - PV Line |

# Installation
1. Download Files to you machine
2. Connect to your Home Assistant and browse to your www folder
3. Create a picture folder under www folder
4. Copy an of the 2 png files in the /local/pictures location
5. Edit your configuration 
6. Add the following code in your configuration.yaml
| sensor:
  - platform: template
    sensors:
      seconds_to_hours:
        friendly_name: "Seconds to Hours"
        value_template: "{{ (states('sensor.victron_system_battery_time_to_go')|float / 3600)|round(2) }}"
        unit_of_measurement: 'hours'

#### - Created Blank Sensor to Allow Text on Picture-Element Card - ####
      blank_blank:
        friendly_name: "Blank Blank"
        value_template: " " |
7. Restart Home Assistant
8. Goto your Dashboard and create a new picture-element card
9. Copy and past the Victron yuml code in the text file in this new card
10. Save your card and test.
11. You can customize as your liking.

Thanks
Johann du Rand
