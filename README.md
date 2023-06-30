# HA-Victron-Display
Home Assistant Picture-Element Victron Display

![image](https://github.com/johanndurandsa/HA-Victron-Display/assets/98578816/fa01e5ba-f9a2-4a3e-95a8-05fe75e5a0bb)


Please find the Victron Background cards (I have created this in Photoshop) that you can place in /local/pictures, or your desired location and the Text file with Yuml code. This is very customizable. 

Add the following code in your configuration.yaml
 
#### - Created Blank Sensor to Allow Text on Picture-Element Card - ####
      blank_blank:
        friendly_name: "Blank Blank"
        value_template: " "
