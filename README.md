# Mixbus Mixer Remote Layout for TouchOSC

Layout for TouchOSC Mk1 app on ipad-sized tablets to control Mixbus DAW.
It consists of five panels mainly to control the mixer functionality of Harrison's Mixbus.
Transport panel, mixer overview, selected channel view, sends on fader pane and a master and monitor pane.

## Requirements
- TouchOSC (MK-1): To install and use this layout you need to get the app [TouchOSC MK1](https://hexler.net/touchosc-mk1) for iOS or Android, if you do not have it yet. We can consider ourselves lucky that they continue the old version.
To transfer the layout to your tablet you need the editor for the desktop. It's [available](https://hexler.net/touchosc-mk1#resources) for all three major operating systems (Java based) and it is free of charge.

- Mixbus 7: Second you need [Mixbus 6 or 7](https://harrisonconsoles.com/product/mixbus). It's available for Linux, Mac and Windows, too.

## How to get it run
- In Mixbus' Edit Menu -> Preferences -> Control Surfaces activate Open Sound Control (OSC)
- Show Protocol Setting -> Either choose **preset file** [n15n-mixbus7remote](n15n-mixbus7remote.preset), which you have to copy to your home directory before you start Mixbus
(please create the osc directory, if it's not there already and substitute *username*)
  - Linux: /home/username/.config/mixbus7/osc
  - Windows: C:\Users\username\AppData\local\Mixbus7\osc 
  - MacOS: /Users/username/Library/Preferences/Mixbus7/osc

  or try **manual settings**:
  
   ### OSC Setup
   - Port Mode: Manual (Specify Below)
   - Reply Manual Port: 8000
   - Bank Size: 32
   - Send Page Size: 0
   - Plugin Page Size: 0
   - Gain Mode: /strip/fader (Position)
   - Debug: Off

   ### Default Strip Types
   - Strip Types Value: 19 (cannot be edited directly)
   - Activate Audio Tracks, Midi Tracks and Control Masters

   ### Default Feedback
   - Feedback Value: 16638 (cannot be edited directly)
   - Select all options EXCEPT Strip Buttons, Metering as a LED Strip, Signal Present, Play Head Position as Samples, Play Head Position as Minutes Seconds, Extra Select Only Feedback.



## The Panels

### Transport Panel
Intuitively set range markers to mark a loop or a punch area,
recording controls include count in and preroll recordings,
jog wheel lets you easily relocate song position on the fly,
keep track of your recording by managing position markers.

![image](https://user-images.githubusercontent.com/8352411/121231631-e81d1d00-c890-11eb-8c43-772d1d2f67c7.png)

### Mixer Panel
8 channels view banked: per channel control of gain, input monitoring, volume control, rec enable, mute, solo, hide option and selection per channel. Every channel has a meter to estimate the volume. Master channel meter features a K-12 inspired and a DPM scale to get a decent volume.

![image](https://user-images.githubusercontent.com/8352411/122676475-93f23100-d1de-11eb-834a-de836ea1f262.png)

### Selected Channel
Detailed channel view of selected channel. Dynamic Control, Equalizer. Simple on/off control for set up plugins, viewport for selectable 32 channels, fader automation and bus routing.

![image](https://user-images.githubusercontent.com/8352411/121231949-519d2b80-c891-11eb-8196-3f68af1e6152.png)

### Sends On Fader
![image](https://user-images.githubusercontent.com/8352411/121232018-67aaec00-c891-11eb-9563-539e6b8ebce3.png)

### Master & Monitor
![2021-06-20 22 48](https://user-images.githubusercontent.com/8352411/122688020-0c2a1800-d21a-11eb-8070-db50ddfdb538.png)
