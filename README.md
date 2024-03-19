[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication)
![Project](https://img.shields.io/badge/Project-SPI-light.svg?style=flat&logo=arduino&logoColor=white&color=%23F7DF1E)

# Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication
<strong>Solo Project: Whatsapp Bot-based Weather monitoring using SPI communication</strong><br><br>
Coming Soon...

<br><br>

## Project Requirements
| Part | Description |
| --- | --- |
| Development Board | • STM32F103C8T6<br>• Wemos D1 Mini |
| Code Editor | Arduino IDE |
| Programmer Tools | ST-Link/V2 |
| Serial Communication Tools | FTDI USB |
| Driver | • ST-Link<br>• USB-Serial CH340 |
| Application Support | Whatsapp Bot |
| IoT Platform | • Twilio<br>• ThingESP |
| Communications Protocol | • Serial Peripheral Interface (SPI)<br>• Hypertext Transfer Protocol (HTTP) |
| IoT Architecture | 4 Layer |
| Programming Language | C/C++ |
| Arduino Library | • SPI (default)<br>• ThingESP |
| Sensor | • MH-RD: Raindrop Sensor (x1)<br>• LDR: Luminous Intensity Sensor (x1)<br>• LM35: Air Temperature Sensor (x1) |
| Other Components | • Micro USB cable - USB type A (x1)<br>• Jumper cable (1 set)<br>• Breadboard (x1) |

<br><br>

## Download & Install
1. Arduino IDE

   <table><tr><td width="810">
         
   ```
   https://www.arduino.cc/en/software
   ```

   </td></tr></table><br>

2. ST-Link Driver

   <table><tr><td width="810">

   ```
   https://bit.ly/STLink_Driver
   ```

   </td></tr></table><br>

3. STM32CubeProgrammer

   <table><tr><td width="810">
   
   ```
   https://bit.ly/STM32_Cube_Programmer
   ```

   </td></tr></table><br>
   
4. USB-Serial CH340

   <table><tr><td width="810">
   
   ```
   https://bit.ly/CH340_Driver
   ```
   
   </td></tr></table>
   
<br><br>

## Project Designs
<table>
<tr>
<th width="420">Block Diagram</th>
<th width="420">Infrastructure</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication/assets/54527592/212dc946-700a-46a5-ac47-4d0f39a3c07c" alt="Block-Diagram"></td>
<td><img src="https://github.com/devancakra/Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication/assets/54527592/7d02d585-384f-42f7-b954-2a1c55ddae12" alt="Infrastructure"></td>
</tr>
</table>
<table>
<tr>
<th width="420">Pictorial Diagram</th>
<th width="420">Wiring</th>
</tr>
<tr>
<td><img src="" alt="Pictorial-Diagram"></td>
<td><img src="" alt="Wiring"></td>
</tr>
</table>

<br><br>

## Basic Knowledge
Basically, a device can be communicated with other devices either wirelessly or by cable. Communication between commonly used hardware is ``` Serial Communication ```. It can be known that there are three types of ``` Serial Communication ```, which include: ``` UART (Universal Asynchronous Receiver-Transmitter) ```, ``` SPI (Serial Peripheral Interface) ```, and ``` I2C (Inter Integrated Circuit) ```. The ``` Serial Peripheral Interface (SPI) ``` is a ``` synchronous serial communication ``` used by microcontrollers to communicate with one or more peripheral devices in close proximity. It can also be used for communication between two microcontrollers. ``` SPI Serial Communication ``` allows a device to act as a ``` master ``` or ``` slave ```. The ``` Master ``` is the primary device that has full authority over the control of the Slave, while the ``` Slave ``` is the secondary device that is under the authority of the Master device. ``` SPI communication ``` requires 3 lines namely ``` MOSI ```, ``` MISO ```, and ``` SCK ```. ``` MOSI (Master Output Slave Input) ``` means that if configured as a ``` master ``` then the ``` MOSI pin acts as an output ```, but if configured as a ``` slave ``` then the ``` MOSI pin acts as an input ```. ``` MISO (Master Input Slave Output) ``` means that if configured as a ``` master ``` then the ``` MISO pin acts as an input ```, but if configured as a ``` slave ``` then the ``` MISO pin acts as an output ```. ``` CLK (Clock) ``` means that if configured as a ``` master ``` then the ``` CLK pin acts as an output ```, but if configured as a ``` slave ``` then the ``` CLK pin acts as an input ```.

<br><br>

## Arduino IDE Setup
1. Open the ``` Arduino IDE ``` first, then open the project by clicking ``` File ``` -> ``` Open ``` :

   <table><tr><td width="810">
   
      • ``` Master.ino ```
      
      • ``` Slave.ino ```

   </td></tr></table><br>
   
2. Fill in the ``` Additional Board Manager URLs ``` in Arduino IDE

   <table><tr><td width="810">
      
      Click ``` File ``` -> ``` Preferences ``` -> enter the ``` Boards Manager Url ``` by copying the following link :
   
      ```
      https://github.com/stm32duino/BoardManagerFiles/raw/main/package_stmicroelectronics_index.json
      http://arduino.esp8266.com/stable/package_esp8266com_index.json
      ```

   </td></tr></table><br>
   
3. ``` Board Setup ``` in Arduino IDE

   <table>
      <tr><th>
         
      i
         
      </th><th width="780">
            
      How to setup the ``` STM32F103C8T6 ``` board
   
      </th></tr>
      <tr><td colspan="2">

      • Click ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Install ``` STM32 MCU based boards ```.

      • Then click ``` Tools ``` -> ``` Board ``` -> ``` STM32 boards groups ``` -> ``` Generic STM32F1 series ```.
              
      </td></tr>
   </table><br><table>
      <tr><th>
         
      ii
         
      </th><th width="775">

      How to setup the ``` Wemos D1 Mini ``` board
            
      </th></tr>
      <tr><td colspan="2">

      • Click ``` Tools ``` section -> ``` Board ``` -> ``` Boards Manager ``` -> Install ``` esp8266 ```.

      • Then click ``` Tools ``` -> ``` Board ``` -> ``` ESP8266 Boards ``` -> ``` Wemos D1 Mini ```.
            
      </td></tr>
   </table><br>
   
4. ``` Change the Board Speed ``` in Arduino IDE

   <table>
      <tr><th>
         
      i
         
      </th><th width="780">
            
      How to change the speed of ``` STM32F103C8T6 ``` board
   
      </th></tr>
      <tr><td colspan="2">

      Click ``` Tools ``` -> ``` Upload Speed ``` -> ``` 9600 ```
              
      </td></tr>
   </table><br><table>
      <tr><th>
         
      ii
         
      </th><th width="775">

      How to change the speed of ``` Wemos D1 Mini ``` board
            
      </th></tr>
      <tr><td colspan="2">

      Click ``` Tools ``` -> ``` Upload Speed ``` -> ``` 115200 ```
            
      </td></tr>
   </table><br>
   
5. ``` Change Board Part Number ``` in Arduino IDE

   <table>
     <tr><th>
         
      How to change Board Part Number of ``` STM32F103C8T6 ``` board

     </th></tr>
     <tr><td width="810">
         
      Click ``` Tools ``` -> ``` Board part number ``` -> ``` BluePill F103C8 ```

     </td></tr>
   </table><br>
   
6. ``` Change U(S)ART Support ``` in Arduino IDE

   <table>
     <tr><th>
         
      How to change U(S)ART Support of ``` STM32F103C8T6 ``` board

     </th></tr>
     <tr><td width="810">
         
      Click ``` Tools ``` -> ``` U(S)ART Support ``` -> ``` Enabled (generic 'Serial') ```

     </td></tr>
   </table><br>

7. ``` Change Upload Method ``` in Arduino IDE
  
   <table>
     <tr><th>
         
      How to change Upload Method of ``` STM32F103C8T6 ``` board

     </th></tr>
     <tr><td width="810">
         
      Click ``` Tools ``` -> ``` Upload method ``` -> ``` STM32CubeProgrammer (SWD) ```

     </td></tr>
   </table><br>
   
8. ``` Install Library ``` in Arduino IDE

   <table><tr><td width="810">
         
      Download all the library zip files. Then paste it in the: ``` C:\Users\Computer_Username\Documents\Arduino\libraries ```

   </td></tr></table><br>

9. ``` Port Setup ``` in Arduino IDE

   <table><tr><td width="810">
         
      Click ``` Port ``` -> Choose according to your device port ``` (you can see in device manager) ```

   </td></tr></table><br>

10. Change the ``` WiFi Name ```, ``` WiFi Password ```, and so on according to what you are currently using.<br><br>

11. Before uploading the program please click: ``` Verify ```.<br><br>

12. If there is no error in the program code, the next step is to use the ``` STM32 ``` programming tool according to the procedure. Then click: ``` Upload ```. While ``` Wemos D1 Mini ``` can be done directly without using programming tools.<br><br>

13. If there is still a problem when uploading the program, then try checking the ``` driver ``` / ``` port ``` / ``` programmer tool ``` / ``` others ``` section.

<br><br>

## ST-Link/V2 Setup
<img width="840" src="https://github.com/devancakra/Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication/assets/54527592/54bf34f8-62c0-482e-8e91-0ab1fe603b76"><br><br>

<strong>Notes:</strong>

<table><tr><td width="840">

   • The JTAG or ``` Serial Cable Debugging (SWD) ``` interface module is basically used to communicate with the ``` STM32 ``` board.
   
   • You can see the wiring between the ``` ST-Link/V2 ``` and the ``` STM32 ``` board in the picture above.

   • To upload the program, besides using the ``` ST-Link/V2 ```, you can also use other programming tools such as: ``` CP2102 USB ```, ``` CH340 USB ```, ``` PL2303 USB ```, or with ``` FTDI USB ```.
   
   • Based on experience, I admit that using the ``` ST-Link/V2 ``` is much better than other programming tools because the process is easier, faster, and more stable.

</td></tr></table>

<br><br>

## FTDI USB Setup
<img width="840" src="https://github.com/devancakra/Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication/assets/54527592/c5b0ab44-b999-4ed8-a254-1349347889d1"><br><br>

<strong>Notes:</strong>

   <table><tr><td width="840">

   • Serial communication on this ``` STM32 ``` board is very possible, especially for ``` Serial Monitor ``` and ``` Serial Plotter ``` purposes. Tools that can be used for serial communication include: ``` CP2102 USB ```, ``` CH340 USB ```, ``` FTDI USB ```, or with ``` PL2303 USB ```.

   • You can see the wiring between the ``` FTDI USB ``` and the ``` STM32 ``` board in detail in the picture above.

   • Based on experience, I admit that using ``` FTDI USB ``` or ``` CP2102 USB ``` is much better than ``` PL2303 USB ``` or ``` CH340 USB ``` because they are known to be more stable in performance.
   
   </td></tr></table>

<br><br>

## Twilio Setup
1. Getting started with Twilio :
   
   <table><tr><td width="810">
      
   • Go to the following url: <a href="https://www.twilio.com/">Click Here</a>.

   • Click ``` Log in ``` to access the service.

   • if you do not have an account, then click ``` Sign up ```.

   </td></tr></table><br>

2. Fill in all the required fields.<br><br>

3. Verify your ``` phone number ``` and ``` email ```.<br><br>

4. Access the ``` WhatsApp sandbox ``` in the ``` Settings ``` menu and ``` send the code ``` to the ``` provided WhatsApp number ```.
   
<br><br>

## ThingESP Setup
1. Getting started with ThingESP :
   
   <table><tr><td width="810">

   • Go to the following url: <a href="https://thingesp.siddhesh.me/#/">Click Here</a>.

   • Click ``` Login ``` to access the service.

   • if you do not have an account, then click ``` Create Account ```.

   </td></tr></table><br>

2. Fill in all required fields.<br><br>

3. Click ``` Project ``` in the sidebar -> then select ``` Add New Project ```.<br><br>

4. After the project has been created, enter the ``` Twilio WhatsApp Endpoint URL ``` into ``` ThingESP ``` to connect.
   
<br><br>

## Get Started
1. Download and extract this repository.<br><br>
   
2. Make sure you have the necessary electronic components.<br><br>
   
3. Make sure your components are designed according to the diagram.<br><br>
   
4. Configure your device according to the settings above.<br><br>

5. Please enjoy [Done].

<br><br>

## Demonstration of Application
Via Whatsapp: <a href="https://github.com/devancakra/Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication/">Weathersia Bot</a>

<br><br>

## Highlights
<table>
<tr>
<th width="840">Hardware</th>
</tr>
<tr>
<td><img src="" alt="hardware"></td>
</tr>
</table>
<table>
<tr>
<th width="840" colspan="2">Whatsapp Bot</th>
</tr>
<tr>
<td width="420"><img src="" alt="wa_bot1"></td>
<td width="420"><img src="" alt="wa_bot2"></td>
</tr>
</table>

<br><br>

## Component Testing
You can download the component test file via the following link: <a href="https://github.com/devancakra/Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication/">Click Here</a>

<br><br>

## Appreciation
If this work is useful to you, then support this work as a form of appreciation to the author by clicking the ``` ⭐Star ``` button at the top of the repository.

<br><br>

## Disclaimer
This application has been created by including third-party sources. Third parties here are service providers, whose services are in the form of libraries, frameworks, and others. I thank you very much for the service. It has proven to be very helpful and implementable.

<br><br>

## LICENSE
MIT License - Copyright © 2024 - Devan C. M. Wijaya, S.Kom

Permission is hereby granted without charge to any person obtaining a copy of this software and the software-related documentation files to deal in them without restriction, including without limitation the right to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons receiving the Software to be furnished therewith on the following terms:

The above copyright notice and this permission notice must accompany all copies or substantial portions of the Software.

IN ANY EVENT, THE AUTHOR OR COPYRIGHT HOLDER HEREIN RETAINS FULL OWNERSHIP RIGHTS. THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, THEREFORE IF ANY DAMAGE, LOSS, OR OTHERWISE ARISES FROM THE USE OR OTHER DEALINGS IN THE SOFTWARE, THE AUTHOR OR COPYRIGHT HOLDER SHALL NOT BE LIABLE, AS THE USE OF THE SOFTWARE IS NOT COMPELLED AT ALL, SO THE RISK IS YOUR OWN.
