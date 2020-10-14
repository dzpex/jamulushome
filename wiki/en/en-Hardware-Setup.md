---
layout: wiki
title: "Hardware Setup"
lang: "en"
permalink: "/wiki/Hardware-Setup"
---


# Hardware Setup

## General info

**For the Jamulus software to run stable it is recommended to use a PC with at least 1.5GHz CPU frequency.**

**Windows users**: You need to install an ASIO driver. If you haven't installed one yet, please do so. Best use a sound card with a native ASIO driver to ensure the lowest possible latencies. If your sound card doesn't provide one, try using this [free ASIO driver (ASIO4All)](http://www.asio4all.org) instead. To setup ASIO4All, have a look at this [basic setup guide](https://github.com/corrados/jamulus/wiki/Installation-for-Windows#setting-up-asio4all).

Example setups can be found further down this page.

## Compatible hardware

Success with Jamulus is partially dependent on the quality of your audio device / sound card. Some built-in sound cards will not have low enough latency, or good enough hardware, to work properly. Please see this list of [known good hardware](Sound-Devices).

## Points to note about inputs

- If you want to connect 2 or more sources (eg voice + synth + guitar), it is important to note that Jamulus currently handles only input 2 channels (L/R). So the hardware being used must provide a mixed-down stereo output to Jamulus.
- Audio interfaces generally output a mixed signal on their analog output, but separate signals (1 per source) on their digital output (USB/Firewire/Thunderbolt).
- Mixers generally only output mixed-down signals on their analog output.
- Mixers with USB/Firewire/Thunderbolt generally output mixed-down signal on their **analog** output AND separate signals only (no mixed-down signal) on their **digital** output.
- A few Mixers with USB/Firewire/Thunderbolt will either send **only** a mixed down signal to the **digital** output (small/budget mixers), or else also ADD a stereo mix-down signal to the separate signals on the digital output.

_(Thanks to [pcar75](https://github.com/pcar75) for this information)_

## Example Setups

Setting up hardware usually burns down to 4 points, although each setup is different.

1. Plug the interface into a USB port on your computer
2. Close all programs and start Jamulus (don't forget to choose the right inputs in Jamulus's settings)
3. Plug in your instrument/microphone and headphones
4. Connect to a Jamulus server and have fun!

### Hardware Setup for Linux Clients with QJackCtrl
Assume you have installed `qjackctrl` with your Jamulus installation. If not see installation of `qjackctrl` with your package manager and your Linux-Distribution (the linux install script in the directory [`/distributions/installscripts`](https://github.com/corrados/jamulus/tree/master/distributions/installscripts) of this repository installs `qjackctrl` for you. Otherwise Linux setup guide on this Wiki.
1. **(Device Plugin)** Plug the interface into a USB port on your computer
2. Plug in your instrument/microphone and headphones in your audio interface (e.g. Focusrite 2i2)
3. **(Input Device/QJackControl)** before starting Jamulus start QJackControl e.g. with `qjackctl` from shell and go to settings of QJackControl. Select your input device e.g. Focusrite 2i2 for jamming with your guitar or for mircophone.
4. **(Output Device/QJackControl)** if you want to listen with your headphones plugged in your Focusrite 2i2, then select also e.g. the Focusrite as output device. 
5. **(Save Settings/QJackControl)** Save your setting with an appropriate name in settings so that you can reload the settings for your next Jamulus session. For next start replace step 3. and 4. by loading your Jack control setting for your audio interface, 
   * set the Sample Rate to 48000 and 
   * set the Frames/Period to 128 and Periods/Buffer at 2 at first
6. **(Restart QJackCrtl)** Restart Jack-Server so that your hardware audio interface is properly set as recording/input device. 
7. **(Start Jamulus)** Start Jamulus after the Jack-server was restarted, so that Jamulus will receive the input of your guitar of microphone from your USB audio interface. Then you can connect to your own server or connect to public available servers for jamming with other musicians on the internet. 

### Linux: Low Latency Kernels for Jamulus
You might want to install Ubuntu Studio (URL: https://ubuntustudio.org/ ) it adds a second options in your boot menu for a low-latency kernel. The key of successful jamming is "low latency" between servers and connected Jamulus clients. If the underlying Linux system is started with a low-latency then it has a positive impact on latency for your Jamulus Sessions.

### Windows: Audio interface connection - ASIO4All
 
This is an example Windows client installation with audio device [Behringer U-CONTROL UCA202](https://www.amazon.com/Behringer-U-Phono-UFO202-Audiophile-Interface/dp/B002GHBYZ0).
The following instructions might be similar with other audio devices.

_**The exact method of connecting your instrument will of course vary depending on your hardware.**_

#### 1. Plug the interface into a USB port on your computer 

In the future, always use the same USB port for the audio device. 

**Windows users**: If not already done: download and install the [free ASIO sound driver (ASIO4All)](http://www.asio4all.org). Some people have also reported success using [this ASIO native driver](http://www.behringerdownload.de/_software/BEHRINGER_2902_X64_2.8.40.zip), although it's not listed on Behringer's product pages as of April 2020.


#### 2. Start Jamulus

Configure Jamulus to use the correct sound setup (see [this excellent guide](https://www.facebook.com/notes/jamulus-online-musicianssingers-jamming/idiots-guide-to-jamulus-app/510044532903831/) by [Simon Tomlinson](https://www.facebook.com/simon.james.tomlinson?eid=ARBQoY3KcZAtS3pGdLJuqvQTeRSOo4gHdQZT7nNzOt1oPMGgZ4_3GERe-rOyH5PxsSHVYYXjWwcqd71a) on Facebook). 

Make sure you have switched off the monitor button on your Behringer U-CONTROL UCA202 (otherwise you will hear both the original sound you are sending to the Jamulus server as well as the returning sound, and may get feedback).

#### 3. Plug in your instrument and headphones 

Connect your instrument to the input plugs of the Behringer U-CONTROL UCA202. Plug in your headphones into the Behringer U-CONTROL UCA202.

#### 4. Connect to a Jamulus server.

You're done! Have fun!

## Having problems?

Please see the [Client Troubleshooting FAQ](Client-Troubleshooting)

***


## Other examples

**This video documents a [live jam session](https://youtu.be/c8838jS2g3U).** I am using a Lexicon Omega USB audio card on a 2009 Mac Mini. My bandmates all use Windows 10 and have Behringer audio cards, e.g. the Behringer Xenyx 1204USB. My internet connection is 10 Mbps down / 1 Mbps upstream via DSL.

**Jamulus user [Andrew Evans](https://sourceforge.net/u/belvario/profile/)**: With bandmates all within one city (but spanning 2 ISPs) and achieving consistent 20ms ping time, running the server on a separate dedicated Windows machine and a client on a Macbook Pro. Remote players on Macbook Air. Everyone on wired Ethernet connections to their home router/gateways. We used WhatsApp video to see each other (with audio muted - it's funny to see how far behind the Whatsapp audio lags from Jamulus though!)

**Messengers for visual connections:** There are different messenger for communication (Signal, Telegram or even SIP-Videotelephony). Keep in mind, that Wifi connection of the mobile devices might consume additional bandwidth for upstream and downstream for your DSL connection at home. If you have a data stream flatrate on your mobile device your might want swap from DSL connection of the mobile device via wifi to your mobile internet to reduce the amount of upstream and downstream traffic for your wired connection with Jamulus to the DSL router.

