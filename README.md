# Mixbus Mixer Remote Layout for TouchOSC
![transport_pane](https://user-images.githubusercontent.com/8352411/122967358-ac06b380-d38a-11eb-8baf-3a3c00b04ea8.jpg) ![mixer](https://user-images.githubusercontent.com/8352411/122967379-b163fe00-d38a-11eb-918f-c9a23c9bb488.jpg) ![selected](https://user-images.githubusercontent.com/8352411/122967426-bde85680-d38a-11eb-8b61-6922929972ee.jpg) ![sendsonfader](https://user-images.githubusercontent.com/8352411/122967402-b6c14880-d38a-11eb-88d7-613618bef66f.jpg) ![master](https://user-images.githubusercontent.com/8352411/122967464-c50f6480-d38a-11eb-9084-78e5f298d168.jpg)

This is a layout to use with TouchOSC MK-1 App. It is used to control Mixbus DAW remotely (WLAN,LAN,USB) via open sound control (OSC) protocol. It is designed for old ipad-sized tablets.
My goal is to create a simple mixer interface and recording control that makes full use of Mixbus' and TouchOSC' possibilities.
I want it to have as much overview and control functions as possible on one panel. On the other side controls like buttons, wheels and faders should not be too small. They should be easy and safe to hit. 

The [Mixbus Remote Layout](mixbus7remote-0.1.1.touchosc) consists of five panels mainly to control the mixer functionality of Harrison's Mixbus.
Transport panel, mixer overview, selected channel view, sends on fader pane and a master and monitor pane.

## Requirements
- TouchOSC (MK-1): To install and use this layout you need to get the app [TouchOSC MK1](https://hexler.net/touchosc-mk1) for iOS or Android, if you do not have it yet. We can consider ourselves lucky that they continue the old version.

- Mixbus 7: Second you need [Mixbus 6 or 7](https://harrisonconsoles.com/product/mixbus). It's available for Linux, Mac and Windows, too.

## How to get it run
- In Mixbus' Edit Menu -> Preferences -> Control Surfaces activate Open Sound Control (OSC)
- Show Protocol Setting -> Either choose **preset** _Ardour Factory Setting_ or try **manual settings**:
  
   #### OSC Setup
   - Port Mode: Manual (Specify Below)
   - Reply Manual Port: 8000
   - Bank Size: 32
   - Send Page Size: 0
   - Plugin Page Size: 0
   - Gain Mode: /strip/fader (Position)
   - Debug: Off

   #### Default Strip Types
   - Strip Types Value: 19 (cannot be edited directly)
   - Activate Audio Tracks, Midi Tracks and Control Masters

   #### Default Feedback
   - Feedback Value: 16638 (cannot be edited directly)
   - Select all options EXCEPT Strip Buttons, Metering as a LED Strip, Signal Present, Play Head Position as Samples, Play Head Position as Minutes Seconds, Extra Select Only Feedback.


- Load [Mixbus Remote Layout](mixbus7remote-0.1.1.touchosc) into TouchOSC on your tablet (for more Information see [TouchOSC-MK1 Manual](https://hexler.net/touchosc-mk1/manual/configuration-layout)). 
  - If you use the _Ardour Factory Setting_ you have to switch between the panels, eg. go to "Mixer" and then back to "Transport". Each panel switch sends a new connect request.

  - Simply push the _refresh_ button in the upper right corner of the first panel, if you use the _manual setup_.


## Caveats and Todos
I have tried to create a stable, reliable and working layout. But particularly unfortunate is the shaky support of the panorama setting (input channels does not get reliable feedback from Mixbus, but control panorama setting works) and the incomplete OSC implementation of the master and monitor busses. In addition, the handling of prefader sends has not yet been solved from my side. Bugs has been reported to Harrison, but so far they did not come back to me. Nevertheless chances are good that future releases solve some issues, because Mixbus builds upon [Ardour](https://www.ardour.org) and Ardour does not have, for example, the panorama problem.

## The Panels

### Transport Panel
Intuitively set range markers to mark a loop or a punch area,
recording controls include count in and preroll recordings,
jog wheel lets you easily relocate song position on the fly,
keep track of your recording by managing position markers.

![Transport Panel](https://user-images.githubusercontent.com/8352411/121231631-e81d1d00-c890-11eb-8c43-772d1d2f67c7.png)

### Mixer Panel
8 channels view banked: per channel control of gain, input monitoring, volume control, rec enable, mute, solo, hide option and selection per channel. Every channel has a meter to estimate the volume. Master channel meter features a K-12 inspired and a DPM scale to get a decent volume.

![Mixer Panel](https://user-images.githubusercontent.com/8352411/122676475-93f23100-d1de-11eb-834a-de836ea1f262.png)

### Selected Channel
Detailed channel view of selected channel. Dynamic Control, Equalizer. Simple on/off control for set up plugins, viewport for selectable 32 channels, fader automation and bus routing.

![Selected Ch Panel](https://user-images.githubusercontent.com/8352411/121231949-519d2b80-c891-11eb-8196-3f68af1e6152.png)

### Sends On Fader
![SendsOnFader Panel](https://user-images.githubusercontent.com/8352411/121232018-67aaec00-c891-11eb-9563-539e6b8ebce3.png)

### Master & Monitor
![Master & Monitor Panel](https://user-images.githubusercontent.com/8352411/122688020-0c2a1800-d21a-11eb-8070-db50ddfdb538.png)
