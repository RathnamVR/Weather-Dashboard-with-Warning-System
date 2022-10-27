# Weather-Dashboard-with-Warning-System
A weather dashboard that will output given location's weather and weather warning system implemented using a NodeMCU.<br/>

The dashboard have three main tabs:
1. Weather
2. Charts
3. Settings

• Weather Tab<br/>

The user is able to enter the location as i) coordinates or ii) city and country through
a text field(s) and submit.<br/>
The title of the description section will be the location entered by the user. If coordinates
are used to specify the location, retrieve the city using OpenWeather.<br/>
Temperature, humidity, pressure, wind speed, wind direction, sunrise time, sun setting
time of the current day will be displayed. These data are updated every 30s by default.<br/>
Suitable customized gauges are used for the above parameters (e.g., a compass for wind direction).<br/>
There is a speaker icon, which, when clicked, would enable the user to hear the
description of the weather.<br/>
There is a warning limit for a selected parameter (e.g., temperature, pressure, ...).<br/>
Used a dropdown list to choose the parameter and a slider to set the limit. (e.g., 25◦C for
temperature, 30 km for wind, etc.). When this limit is exceeded, a notification will appear
as a warning displaying the current value of the parameter (e.g., Warning! Temperature is
30◦C. Exceeds the limit by 5◦C)

![alt text](https://github.com/RathnamVR/Weather-Dashboard-with-Warning-System/blob/main/images/weather.PNG?raw=true)
• Charts Tab<br/>

 There are charts that show the temperature, humidity, wind speed and pressure of the past hour.<br/>

![alt text](https://github.com/RathnamVR/Weather-Dashboard-with-Warning-System/blob/main/images/charts.PNG?raw=true)

• Settings Tab<br/>

The user is able to select whether the location is entered as i) coordinates or ii) city
and country.<br/>
The user is able to change the refresh time (use numeric palette).<br/>
A switch is used to turn the charts feature on and off.<br/>

![alt text](https://github.com/RathnamVR/Weather-Dashboard-with-Warning-System/blob/main/images/settings.PNG?raw=true)


Weather warning system part is implemented using a NodeMCU. Link the above dashboard to the NodeMCU via MQTT. 

![alt text](https://github.com/RathnamVR/Weather-Dashboard-with-Warning-System/blob/main/images/overview.PNG?raw=true)

• The built-in LED of the node-MCU will blink in a warning situation. The threshold/limit for the
warning situation is set as described in Part I.<br/>
• The blinking interval will change from 5s to 500ms according to the exceeded amount. For an example,
5s interval if the value is just above the warning limit and decreasing up to 500ms interval if it
reaches a maximum value. You may decide what the maximum value is.<br/>
