# WarudoOVRT_CAM
[OVR Toolkit](https://store.steampowered.com/app/1068820/OVR_Toolkit/) custom application to send spawned overlay position to [Warudo](https://store.steampowered.com/app/2079120/Warudo/) to move the VTubing software's camera.

Exmaple video: https://www.youtube.com/watch?v=Hz5hxHi4nGU

**This software is more of a 'proof-of-concept' as implementation is very scuffed and requires some technically knowledge to get working.  I don't *recommend* using it on a production enviroment, but also it's better than using LIV**

## Requirements
If you would like to use this project, make sure you have the following set up:

### Programs
- [OVR Toolkit (OVRT)](https://store.steampowered.com/app/1068820/OVR_Toolkit/) for which this custom application was made.
- [Virtual Motion Capture (VMC)](https://www.patreon.com/sh_akira) to send SteamVR/OpenVR tracker positions to Warudo.
- [Warudo](https://store.steampowered.com/app/2079120/Warudo/) to receive the VMC information and display your character.
  
### Warudo
- An existing character ready for use in Warudo.
- A VMC Receiver asset in your Warudo scene.
- Import the 'DiscountLIV' blueprint json file.

### Virtual Motion Capture
- Requires the paid version of the app, can be obtained on [sh_akira's patreon.](https://www.patreon.com/sh_akira)
- Have a version of your character in VMC with the same skeleton heirachy as your character in Warudo.
  - I recommend creating a VRM of your character with a minimized mesh to act as a 'dummy character' just to send the necessary data.
- Enable OSC motion sender in the VMC configuration to match the port of your VMC Receiver in Warudo.

## Installation and Usage
To install the custom application, copy the entire WarudoOVRT_CAM application folder to OVRToolkit's LocalCustomApps Directory, which is located in OVRT's install location- usually: `steamapps/common/OVR Toolkit/LocalCustomApps`
I may push this repository to the OVR Toolkit workshop, but since it's very specialized I may just leave it here.

To use, while in SteamVR and with VMC, OVRT, and Warudo running, confirming that VMC is sending data to Warudo and Warudo is applying that data to your character:
Open the OVRT phone menu, and select the Warudo icon.  Finally, click on the Warudo icon in the center to open an overlay targeting Warudo.  The camera in your scene should now move while you move the OVRT overlay.
