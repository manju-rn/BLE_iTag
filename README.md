# iTag_BLE_Button
Use an "iTag" device as a remote control button or switch using BLE controlled by an ESP32  

# iTag Device
The "iTag" is low cost BLE locator tag.  When on, the iTag provides a bluetooth low energy acting as a server and provides the services.
The 3 useful services are:
1. An ESP can be programed to connect as a client and request that the tag beep, as a means of locating a lost item.  The tag will also beep when the connection is dropped as a means to remind you that you're leaving an item behind.
2. Using the iTag button, it can send the notification on a specific BLE Characteristic.  This is similar function as used as a shutter release or to activate a voice recorder on the host phone. Paired with any other component in ESP (or integration with Home Automation software, such as Home Assistant), any actions based on this button event can be triggered

# Operation
- The device will search for known iTag devices.  During this search the LED will blink.
- If it find ones, it will connect.  The LED will go solid. 
- Once connected, a press of the iTag button will send the button click notification to ESP32
- Upon disconnect it will go back into scanning mode.
- (Future Release) Multi-click actions from iTag
Note: When the iTag goes out of BLE range of ESP32, it starts to beep for sometime before it timeouts or manual disabled via the click. As the use case for this is designed to work perpetually in connected environment, this may be less annoying 

# ESPHOME
The code can be used as a custom component in Esphome. 

# License
This is a release of draft version of the project and is under GPL v3.  

# Disclaimer

**Basically, use the materials in this repository at your own risk.**

BECAUSE THE PROGRAM & HARDWARE DESIGN IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY FOR THE PROGRAM & HARDWARE 
DESIGN, TO THE EXTENT PERMITTED BY APPLICABLE LAW. EXCEPT WHEN OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS 
AND/OR OTHER PARTIES PROVIDE THE PROGRAM & HARDWARE DESIGN "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A 
PARTICULAR PURPOSE. THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE PROGRAM & HARDWARE DESIGN IS WITH 
YOU. SHOULD THE PROGRAM OR HARDWARE DESIGN PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING, 
REPAIR OR CORRECTION.

IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING WILL ANY COPYRIGHT HOLDER, OR ANY OTHER 
PARTY WHO MAY MODIFY AND/OR REDISTRIBUTE THE PROGRAM OR HARDWARE DESIGN AS PERMITTED ABOVE, BE LIABLE TO YOU 
FOR DAMAGES, INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OR 
INABILITY TO USE THE PROGRAM OR HARDWARE DESIGN (INCLUDING BUT NOT LIMITED TO LOSS OF DATA OR DATA BEING RENDERED
INACCURATE OR LOSSES SUSTAINED BY YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM OR HARDWARE DESIGN TO OPERATE
WITH ANY OTHER PROGRAMS OR HARDWARE), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE POSSIBILITY OF
SUCH DAMAGES.

