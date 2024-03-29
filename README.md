# esp32brewkettle
Simple project marrying two of my hobbies: technology and beer brewing. Handles brew kettle temperature tracking using an ESP32 dev board running ESPHome and a 3 wire PT100 RTD sensor and a small inexpensive 0.96 inch OLED screen. 

<img src="https://github.com/Mtbred/esp32brewkettle/blob/main/assets/photos/brewkettle5.jpg" width="270" height="480"/>


## Project Overview

### Why not just buy an off the shelf sensor?
A  brew kettle thermometer can be had off the shelf for under $20 off Amazon here: https://a.co/d/13JsgsW 
And while that option is a simple solution, it doesn't let me expand my knowledge or experience new things.
This project gave me an opportunity to learn some new skills like soldering and modeling in Fusion 360.
Plus, who doesn't love pretty graphs?
 
### Requirements/Goals
- Detachable from the brew kettle for simple cleaning
- Easily readable and out of the way during brew day
- Accurate at both boiling and sub-boiling temperatures
- Collect the data somewhere (Home Assistant currently, next stage being InfluxDB via MQTT so that I can collect and display multiple sensors from various phases of a brew day/fermentation)
- Learn something new
- Useable product before my next brew day, don't get stuck yak shaving (even though I did a few times)

## Assembly guide
### Hardware
#### Components
- HiLetgo ESP32 NodeMCU WROOM-32S: https://a.co/d/3XsYek3
- Electrocookie solderable breadboard: https://a.co/d/a9Ho8Mn
- Auber Instruments PT100 (I went with the 12ft braided cable with XLRCON-M connector option as it gave me a ton of flexibility on where the brains could sit during brew day): https://www.auberins.com/index.php?main_page=product_info&cPath=20_131_15&products_id=261
- Adafruit Max 31865 Amplifier: https://www.adafruit.com/product/3328
- various wires and pins/headers
- All but one components are mounted using M2 screws and nuts (the XLR  receptacle is attached using M3 screws/nuts).
- v2 makes use of 8x2mm magnets (8 of them): https://a.co/d/6sLEmh9

#### Case
The Original was printed on my Ender3 V2 using Elegoo PLA with a standard quality profile in Cura. 
- Infill: 20% 
- layer height: 0.2mm
- Nozzle size: 0.4mm
- wall count: 3
- supports: ZigZag

v2 was printed on my new Bambu Labs P1S using PETG-CF with some tweaked profiles with a hardened 0.4mm nozzle. Feel free to reach out if you want any of the profile configurations.

v2 of the case upgrades from a press fit connection to using 8x2mm magnets to hold it together as well as a redesign of the cable tie mounts so that they can print without supports. 


#### Wiring Diagram
WIP

#### Software
I already had ESPHome running in my homelab via their docker container(https://hub.docker.com/r/esphome/esphome) making it easy to build out configurations for each of the components. 
You'll find my original configuration which I hooked up to Home assistant under ESPHome/brewkettle_HA.yaml. (future iteration that I have feeding to an InfluxDB will be added). 

## Usage notes
Font files must be present in /config volume to be able to properly load them for the screen.

## Future Plans
-  Convert to MQTT/NodeRed/InfluxDB/Grafana stack for data polling and management (potentially?)
-  ~~Convert case join to magnetic connection~~
-  ~~Reprint case on Bambu P1S for textured finish~~
-  Upload photos of v2 case
-  Replace mounting holes with peg board solution
-  Really loving the round displays like the waveshare 1.28 in circular display lately. Would love to redesign the screen portion to use a circular screen with context information related to current process/target

https://www.aliexpress.us/w/wholesale-waveshare-1.28-circular.html?spm=a2g0o.productlist.search.0

### Lessons Learned
- The initial idea for a project is great, even fleshed out however if you are stepping into something new you will inevitably hit a point where you realize you could have made better decisions at the beginning. Don't be afraid to cut a foundational piece because you've spent time on it (Arduino vs ESP32)
- Prototyping to ensure measurements are accurate is always going to be helpful when it comes time to print a final product
- Goals for the project can change over time, but getting to the point of having a project in a functional state before you add on more bells and whistles feels great
- Snap fit is always tough as you change materials, PETG print was difficult as was other brands of PLA. The move to magnets in v2 felt like a huge upgrade
- Design with supports in mind!

### A few project photos (sorry the focus is awful)
<img src="https://github.com/Mtbred/esp32brewkettle/blob/main/assets/photos/brewkettle1.jpg" width="384" height="510"/>
<img src="https://github.com/Mtbred/esp32brewkettle/blob/main/assets/photos/brewkettle2.jpeg" width="270" height="480"/>
<img src="https://github.com/Mtbred/esp32brewkettle/blob/main/assets/photos/brewkettle3.jpg" width="384" height="510"/>
<img src="https://github.com/Mtbred/esp32brewkettle/blob/main/assets/photos/brewkettle4.jpg" width="384" height="510"/>
<img src="https://github.com/Mtbred/esp32brewkettle/blob/main/assets/photos/ec1.jpg" width="384" height="510"/>
<img src="https://github.com/Mtbred/esp32brewkettle/blob/main/assets/photos/prototype1.jpg" width="510" height="384"/>
<img src="https://github.com/Mtbred/esp32brewkettle/blob/main/assets/photos/kettle.jpg" width="384" height="510"/>

## License

MIT License © github.com/Mtbred
