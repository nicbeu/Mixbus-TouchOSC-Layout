# Mixbus Mixer Remote Layout for TouchOSC
![transport_pane](https://user-images.githubusercontent.com/8352411/122967358-ac06b380-d38a-11eb-8baf-3a3c00b04ea8.jpg) ![mixer](https://user-images.githubusercontent.com/8352411/122967379-b163fe00-d38a-11eb-918f-c9a23c9bb488.jpg) ![selected](https://user-images.githubusercontent.com/8352411/122967426-bde85680-d38a-11eb-8b61-6922929972ee.jpg) ![sendsonfader](https://user-images.githubusercontent.com/8352411/122967402-b6c14880-d38a-11eb-88d7-613618bef66f.jpg) ![master](https://user-images.githubusercontent.com/8352411/122967464-c50f6480-d38a-11eb-9084-78e5f298d168.jpg)

This is a layout to use with TouchOSC MK-1 App. It is used to control Mixbus DAW remotely (WLAN,LAN,USB) via open sound control (OSC) protocol. It is designed for old ipad-sized tablets.
My goal is to create a simple mixer interface and recording control that makes full use of Mixbus' and TouchOSC' possibilities.
I want it to have as much overview and control functions as possible on one panel. On the other side controls like buttons, wheels and faders should not be too small. They should be easy and safe to hit. 

The [Mixbus Remote Layout](mixbus10remote-0.1.1.touchosc) consists of five panels mainly to control the mixer functionality of Harrison Mixbus.
Transport panel, mixer overview, selected channel view, sends on fader pane and a master and monitor pane.

## Requirements
- TouchOSC (MK-1): To install and use this layout you need to get the app [TouchOSC MK1](https://hexler.net/touchosc-mk1) for iOS or Android, if you do not have it yet. We can consider ourselves lucky that they continue the old version.

- Mixbus 10: Second you need [Mixbus 10](https://store.harrisonaudio.com/all-products/mixbus-10). It's available for Linux, Mac and Windows, too.
(Initially made the layout for Mixbus 6/7. OSC support in Mixbus 8 and 9 was very buggy and hardly usable.
Mixbus 10 now supports almost all commands required by the layout.)

## How to get it run
- In Mixbus' Edit Menu -> Preferences -> Control Surfaces activate Open Sound Control (OSC)
- Show Protocol Setting -> Either choose **preset** _Ardour Factory Setting_ or try **manual settings**:
  
   #### OSC Setup
   - Port Mode: Manual (Specify Below)
   - Reply Manual Port: 8000
   - Debug: Off  

- Load [Mixbus Remote Layout](mixbus10remote-0.1.1.touchosc) into TouchOSC on your tablet (for more Information see [TouchOSC-MK1 Manual](https://hexler.net/touchosc-mk1/manual/configuration-layout)).
- In the settings dialog of TouchOSC OSC needs to be enabled, the host's IP address must be filled in and the port numbers must match Mixbus'.
    - Port (outgoing) you find at the top of Mixbus' protocol settings: Looks like *Connection: osc.udp://xxx.xxx:3819*. You are looking for the last 4 digits.
    - Port (incoming) corresponds to the Manual Reply Port of Mixbus' OSC Setup. *8000* in this example.
- Once the OSC controller is connected to Mixbus all the other settings are overwritten when you switch between the panels. Each panel switch sends a new connect request.

## Caveats and Todos
  - Compressor mode selection does not react as expected, but the switching works nevertheless.
  - Compressor ratio setting does not work due to a bug in Mixbus which does not recognize the documented command.
  - Screenshots on this page has not been updated.
  - New features of Mixbus 10 are not implemented.

## The Panels

### Transport Panel
Intuitively set range markers to define a loop or punch area. Recording controls include count-in and pre-roll options. The jog wheel allows you to quickly adjust the song position on the fly, and position markers help you keep track of your recording.

![Transport Panel](https://user-images.githubusercontent.com/8352411/121231631-e81d1d00-c890-11eb-8c43-772d1d2f67c7.png)

### Mixer Panel
8 channels are viewed in a banked layout, with individual controls for each channel including gain, input monitoring, volume, record enable, mute, solo, hide option, and selection. Each channel is equipped with a meter to monitor volume levels. The master channel meter includes a K-12 inspired scale and a DPM scale for accurate volume assessment.

![Mixer Panel](https://user-images.githubusercontent.com/8352411/122676475-93f23100-d1de-11eb-834a-de836ea1f262.png)

### Selected Channel
The detailed view of the selected channel includes dynamic control and an equalizer. It features simple on/off controls for previously set up plugins, a viewport for selecting up to 32 channels, fader automation, and bus routing.

![Selected Ch Panel](https://user-images.githubusercontent.com/8352411/121231949-519d2b80-c891-11eb-8196-3f68af1e6152.png)

### Sends On Fader
![SendsOnFader Panel](https://user-images.githubusercontent.com/8352411/121232018-67aaec00-c891-11eb-9563-539e6b8ebce3.png)

### Master & Monitor
![Master & Monitor Panel](https://user-images.githubusercontent.com/8352411/122688020-0c2a1800-d21a-11eb-8070-db50ddfdb538.png)
