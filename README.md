# esp32brewkettle
Simple project marrying two of my hobbies, technology and beer brewing. Handles brew kettle temperature tracking using an ESP32 dev board running ESPHome and a 3 wire PT100 RTD sensor and a small inexpensive 0.96 in OLED screen. 

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

#### Case
    Printed on my ender3 V2 using Elegoo PLA with a standard quality profile in Cura. 
    - Infill: 20% 
    - layer height: 0.2mm
    - Nozzle size: 0.4mm
    - wall count: 3
    - supports: ZigZag

## Usage notes

## Future Plans/Known issues

### Iterations/Lessons Learned
    I went through a few iterations of this project. initially starting with an Arduino UNO R3 and C++. I had a functional prototype on a breadboard with the sensor and screen displaying the temperature as expected. 

## License

MIT License © github.com/Mtbred