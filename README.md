ProtoCentral ADS1292R ECG/respiration shield and breakout board 
================================

[![ECG](https://www.protocentral.com/3059-large_default/ads1292r-ecgrespiration-shield-v2.jpg)  
Dont have it yet? But one here: ADS1292R ECG/Respiration Shield for Arduino- v2 (PC-4128)](https://www.protocentral.com/arduino-shields/818-ads1292r-ecgrespiration-shield-v2.html)

[![bob](docs/img/ads1292r_breakout.jpg)  
Dont have it yet? But one here: ADS1292R ECG/Respiration Breakout for Arduino- v3 (PC-4116)](https://www.protocentral.com/analog-adc-boards/783-ads1292r-ecgrespiration-breakout-board.html?search_query=ecg&results=4)

Easily monitor ECG and respiration using your Arduino with this plug-in shield. The version 2 of this product adds a new SPI pin header making it compatible with newer Arduino devices including the Arduino Yun and 3.5mm connector for the electrodes. 

We now include the electrodes and cable also with the shield
Just plug it into an Arduino and you're ready to go. The 3.5 mm circular connector provides an easy way to connect electodes to the shield. The other end of this cable has snaps for standard ECG electrodes. We also include a pakc of 10 disposable EG electrodes. It accepts two ECG electrodes and one Driven Right Leg (DRL) electrode for common mode noise reduction. 

Another interesting feature of this shield is that you can also measure the respiratory activity using the same two electrodes connected to the shield. The ADS1292R uses a method known as impedance pneumography to measure respiration using the changes in chest impedance caused during respiration. 


Features:
----------
* ADS1292R Analog Front End IC
* Onboard 3.3V voltage regulator for low noise
* Onboard logic level transalators for Arduino interface
* Prototyping area for adding addtional components

Includes:
----------
* ADS1292R Arduino shield
* Electrode cable with 3.5mm connector and ECG electrodes connectors
* Pack of 10 disposable stick-on ECG electrodes.

Repository Contents
-------------------
* **/Libraries** - Arduino library and example sketches.
* **/Hardware** - All Eagle design files (.brd, .sch)
* **/extras** - includes the datasheet

Connecting the shield to your Arduino
-------------------------------------
Connect the ECG/Respiration shield to the Arduino by stacking it on top of your Arduino. This shield uses the SPI interface  to communicate with the Arduino. Since this includes the ICSP header, which is used on newer Arduinos for SPI communication,  this shield is also compatible newer Arduino boards such as the Arduino Yun and Due.
 

 
Wiring the Breakout to your Arduino
------------------------------------
 If you have bought the breakout the connection with the Arduino board is as follows:
 
|ads1292r pin label| Arduino Connection   |Pin Function      |
|----------------- |:--------------------:|-----------------:|
| VDD              | +5V                  |  Supply voltage  |             
| PWDN/RESET       | D4                   |  Reset           |
| START            | D5                   |  Start Input     |
| DRDY             | D6                   |  Data Ready Outpt|
| CS               | D7                   |  Chip Select     |
| MOSI             | D11                  |  Slave In        |
| MISO             | D12                  |  Slave Out       |
| SCK              | D13                  |  Serial Clock    |
| GND              | Gnd                  |  Gnd             |
 
Installing the Arduino libraries 
---------------------------------
If you have correctly installed the libraries, the example sketeches should now be available from within Arduino.

[Download the latest Arduino Sketch here for this board here.](https://github.com/Protocentral/ADS1292rShield_Breakout/releases/download/v1.0/Protocentral_ADS1292R-v1.0-arduino.zip)

Open up your Arduino IDE and run the Arudino sketch (.ino) file in the archive that you downloaded. Your Arduino should now be programmed to read the ecg data and sending over the USB-UART.  
 
Using the ProtoCentral ECG/Resp. GUI
-----------------------------------

The GUI for visulizing the ECG and Respiration as well as parameters like Heart rate and Respiration rate is written in Processing, based on Java and is cross-compilable across platforms. 
 
Java 8 is required on all platforms for running the processing-based GUI application. You can download Java for your platform from the following link.

[https://java.com/en/download/](https://java.com/en/download/)

### Processing GUI Installation

Download the zip file containing the executable files from the following links for 32-bit/64-bit Windows. If you do not know if you have a 64-bit or 32-bit computer, please download the 32-bit version.

* [Windows 32-bit Executable (ZIP)](https://github.com/Protocentral/ADS1292rShield_Breakout/releases/download/v1.0/protocentral_ads1292r_gui-v1.0-win32.zip)
* [Windows 64-bit Executable (ZIP)](https://github.com/Protocentral/ADS1292rShield_Breakout/releases/download/v1.0/protocentral_ads1292r_gui-v1.0-win64.zip)
* [MacOS Executable (ZIP)](https://github.com/Protocentral/ADS1292rShield_Breakout/releases/download/v1.0/protocentral_ads1292r_gui-v1.0-macos.zip)
* [Linux 32-bit Executable (ZIP)](https://github.com/Protocentral/ADS1292rShield_Breakout/releases/download/v1.0/protocentral_ads1292r_gui-v1.0-linux32.zip)
* [Linux 64-bit Executable (ZIP)](https://github.com/Protocentral/ADS1292rShield_Breakout/releases/download/v1.0/protocentral_ads1292r_gui-v1.0-linux64.zip)
* [Raspberry Pi - Raspbian (ZIP)](https://github.com/Protocentral/ADS1292rShield_Breakout/releases/download/v1.0/protocentral_ads1292r_gui-v1.0-rpi.zip)

Simply download the appropriate file for your operating system, unzip the contents and run the executable program contained in it. 

Select the port to which your Arduino is connected to from the "Select Port" dropdown box and data should immedaitely start coming in.


![ProtoCentral ads1292r_Shield/breakout](docs/img/ecg_plot.gif)

Connecting the ECG Electrodes
------------------------------
 A 3-electrode cable along with a standard stereo jack is provided along with the shield to connect the electrodes to the     shield. The electrode input connector is highlighted in the below picture.
 
 The other side of the electrode connector would connect to snap-on electrodes attached to the body. For testing purposes,    you can use an ECG simulator to provide inputs to the board. 

 Warning:
 When connecting the electodes to the body, it is safer to disconnect the mains power source to the Arduino. For example, if  you are using the Arduino along with a laptop, disconnecting the battery charger from the laptop would be a safe option.
 
Placing the Electrodes on the body
---------------------------------
![Wearing the Electrode](docs/img/body.png)


License Information
===================

This product is open source! Both, our hardware and software are open source and licensed under the following licenses:

Hardware
---------

**All hardware is released under [Creative Commons Share-alike 4.0 International](http://creativecommons.org/licenses/by-sa/4.0/).**
![CC-BY-SA-4.0](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)

You are free to:

* Share — copy and redistribute the material in any medium or format
* Adapt — remix, transform, and build upon the material for any purpose, even commercially.
The licensor cannot revoke these freedoms as long as you follow the license terms.

Under the following terms:

* Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
* ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

Software
--------

**All software is released under the MIT License(http://opensource.org/licenses/MIT).**

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


Please check [*LICENSE.md*](LICENSE.md) for detailed license descriptions.
