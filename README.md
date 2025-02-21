# Incremental Podometer Hardware

On this repo you'll find details about our journey to make a little pcb board which counts steps and keep you entertained !
You can take a look at schematics in the /pcb directory or just keep reading this!

**If you want to look at the software of the Incremental Podometer look at [this repo](https://github.com/theMathR/incremental-podometer/tree/main)**

# Its history

So first, what is the Incremental Podometer ?
It's a podometer ! (No wwwaaaaayyyyy) But. With. An. Incremental Game !!!!!!!
You'll have stats about your physic activity but you'll remain entertained ! Amazing no ?

So we started to brainstorm a bit and established a list of essential components :
- A screen, needed for having a UI for the game
- A micro controller (with circuitpython, I dont code in C)
- Some buttons (Our first idea was 8 buttons)
- An accelerometer (For counting steps)

So with that in mind, we started to look individually at these components:
First for the microcontroller, we chosed a Pico W because it's cheap, easy to use and mainly because it has wireless capabilities
Second, the screen. We planned to use [the same as the sprig]([url](https://www.adafruit.com/product/358)). But we quickly realised it will be not cheap enough so we finally opted for an [equivalent screen from a german seller.](https://www.az-delivery.de/fr/products/1-8-zoll-spi-tft-display?variant=6106727841819)

Our main problem during this project _was the cost of the podometer_. Our first prototype was 30$/board. We planned to make 30 of them and with 450$ at this price we could only make 15 of them. :/ 
We cut the costs by dont ordering the picos from JLPCB (6$ less via digikey !), using another screen (4,50$/screen) and soldering all these parts. I also regrouped all the parts we need assembled by the pcb maker on the same side because double sided assembly is SO EXPENSIVE !!!
And we finally opted for an ADXL345 over an ADXL335 because it has I2C and is more power efficient (And 2$ less!)

## Components list

- Pico W
- ADXL345
- Some [adafruits buttons](https://www.adafruit.com/product/3101l)
- [BH-AAA-B5AA005](https://www.lcsc.com/product-detail/Button-And-Strip-Battery-Connector_MYOUNG-BH-AAA-B5AA005_C2979170.html) (battery holder)
- [1N5817](https://www.lcsc.com/product-detail/Schottky-Barrier-Diodes-SBD_LGE-1N5817_C7544876.html)
- [JS202011SCQN](https://www.lcsc.com/product-detail/Slide-Switches_C-K-JS202011SCQN_C221666.html) (slide switch)
- Some 1uf capacitors

![image](https://github.com/Spectralo/IncrementalPodometerHardware/assets/122629939/8b52cbc5-6c25-48c8-80b6-783f29762f13)
