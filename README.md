# Home_Automation
Ever thought of a life where you could just command your home appliances to work as you need just by using your voice? Gone are the days where you have to be a billionaire to have an automated house which is voice activated.
Here is a small project to showcase how electronic appliances like T.V, fans, lights etc can be controlled over the internet with your voice using ESP8266, blynk application and google assistant.

## REQUIRED EQUIPMENTS
- [ ] ESP8266 NodeMCU
- [ ] Relay
- [ ] Jumper cables
- [ ] Bread Board
- [ ] Smart phone

## Home Automation Using NodeMCU and Google Assistant.


![Image of Home_Automation](https://github.com/BhupendraNegi/Home_Automation/blob/master/Pictures/Home%20Automation.png)


- [ ] Download and Installing the Blynk App on the Smartphone.
* Login and create a new project by clicking ‘New Project’.
* Select the hardware device as NodeMCU and select the connection type as WIFI.
* Blynk will send an Auth token to your email id.
* Create a button to control the first relay. Select the pin as digital pin D3.

- [ ] Download Arduino IDE and Configure the Blynk Libraries.

- [ ] Upload the code to NodeMCU.
* Go to Tools > Board and select ‘NodeMCU 1.0 (ESP-12E Module)’ as the board.
* Go to Files > Examples > Blynk > Boards_WIFI > ESP8266_Standalone. 
* Change the Auth token, ssid and password.

- [ ] Hardware Assembly.


![Image of Hardware](https://github.com/BhupendraNegi/Home_Automation/blob/master/Pictures/Espnode%20module.jpg)



![Image of ESP8266](https://github.com/BhupendraNegi/Home_Automation/blob/master/Pictures/HardwareAssembly.png)

- [ ] Connect Google Assistant (using IFTTT) to make the NodeMCU work with voice commands.
We cannot connect the Google Assistant to the NodeMCU directly, and that is the only reason we are using the Blynk app. Blynk app can directly connect to the NodeMCU and send data to it. So, if we can send the voice commands interpreted by google assistant directly to the Blynk app, the Blynk app can then forward those commands to the NodeMCU. But the problem is Google Assistant cannot directly understand foreign commands like “turn on the fan” or “turn on relay one” etc. on its own. So, to solve this we use another intermediate app/website called ‘IFTTT’.

* Go to IFTTT’s website and sign up to it using your Google Account.
* After Signing in click on My Applets from the header and select New Applet.
* Create two Triggers of Google Assistant to turn ON ans OFF light.
* In the URL field type this URL:
http://188.166.206.43/ YourAuthTokenHere / update / DigitalPinToBeUpdateHere

