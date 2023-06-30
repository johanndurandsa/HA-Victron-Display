# HA-Victron-Display
Home Assistant Picture-Element Victron Display

![image](https://github.com/johanndurandsa/HA-Victron-Display/assets/98578816/fa01e5ba-f9a2-4a3e-95a8-05fe75e5a0bb)


Please find the Victron Background cards (I have created this in Photoshop) that you can place in /local/pictures, or your desired location and the Text file with Yuml code. This is very customizable. 

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
