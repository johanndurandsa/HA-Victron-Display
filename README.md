# HA-Victron-Display
Home Assistant Picture-Element Victron Display

Please find the Victron Background cards (I have created this in Photoshop) that you can place in /local/pictures, or your desired location and the Text file with Yuml code. This is very customizable. 

![image](https://github.com/johanndurandsa/HA-Victron-Display/assets/98578816/fa01e5ba-f9a2-4a3e-95a8-05fe75e5a0bb)

![image](https://github.com/johanndurandsa/HA-Victron-Display/assets/98578816/8982e585-4aab-4e37-acd8-97b80c91a577)


The Name: inside the code is created for each block to understand which one you working on
eg.
   1. name: Red Grid Block - Grid Name
   2. name: Red Grid Block - Eskom Grid Watt
   3. name: Red Grid Block - Load Shedding
   4. name: Red Grid Block - Icon
   5. name: Red Grid Block - Line
   6. name: Victron Block - Vebus State
   7. name: Victron Block - Icon
   8. name: Green AC Block - Grid Name
   9. name: Green AC Block - AC Loads
   10. name: Green AC Block - Icon
   11. name: Green AC Block - Grid Line
   12. name: Blue Battery Block - Battery SOC
   13. name: Blue Battery Block - Battery Power
   14. name: Blue Battery Block - Battery Voltage
   15. name: Blue Battery Block - Battery Current
   16. name: Blue Battery Block - Icon
   17. name: Blue Battery Block - Battery V-Line
   18. name: Blue Battery Block - Battery H-Line
   19. name: Blue Battery Block - Battery Hours Left
   20. name: Yellow PV Block - Grid Name
   21. name: Yellow PV Block - PV Power
   22. name: Yellow PV Block - Icon
   23. name: Yellow PV Block - PV Line

# Installation
1. Download Files to you machine
2. Connect to your Home Assistant and browse to your www folder
3. Create a picture folder under www folder
4. Copy an of the 2 png files in the /local/pictures location
5. Edit your configuration 
6. Add the following code in your configuration.yaml
   #### - Created Blank Sensor to Allow Text on Picture-Element Card - ####
         blank_blank:
           friendly_name: "Blank Blank"
           value_template: " "
7. Restart Home Assistant
8. Goto your Dashboard and create a new picture-element card
9. Copy and past the Victron yuml code in the text file in this new card
10. Save your card and test.
11. You can customize as your liking.

Thanks
Johann du Rand
