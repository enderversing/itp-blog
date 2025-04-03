# Week 9


## Solar Project

I tried to connect the the Meshtastic device over Bluetooth and got this weird popup. Further research needed.
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/22937.png)

Meshtastic web client didn't show me that the board was misconfigured. 
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/IMG_2962.gif)

I always begin by setting the LoRa region for sending messages (in Meshtastic, I think you have to do this.)
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/24011.png)

I think I'll keep my solar powered repeater in client mode because the repeater is not in an "extremely stratefic" location.
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/24129.png)

Repeater and router modes require high power consumption.
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/24147.png)

I tried to configure the [Seeed Studio kit](https://www.seeedstudio.com/Wio-SX1262-with-XIAO-ESP32S3-p-5982.html) a few different ways, unsuccessful each time.
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/IMG_2965.gif)

I moved onto an Adafruit Feather / Featherwing DIY setup, which is nice to look at but I suspect it is not Meshtastic compatible.

I have been learning that - if I'm correct - not all 915.0 MHz radio chips are actually compatible with Meshtastic. There's few actual Meshtastic suppliers.
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/IMG_2968.gif)

It appeared that I was able to flash my CLIENT node with Meshtastic firmware, but the web client woudldn't allow me to actually send messages.
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/45458.png)

I tried to go back to the [XIAO ESP32S3 & Wio-SX1262 Kit](https://www.seeedstudio.com/Wio-SX1262-with-XIAO-ESP32S3-p-5982.html).
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/IMG_2961.jpeg)

![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/IMG_2963.jpeg)

I couldn't figure how to actually connect the two boards or how to use the antennas.
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/IMG_2964.jpeg)


I feel proud of myself whenever I manage to solder something, but I realized very late that this board probably can't run Meshtastic.

Left: assorted parts.

Right: Assorted parts soldered together.

![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/IMG_2966.jpeg)

Talking to resident Jess, I was informed that a project using only solar power (no batteries) to run could use the AEMSUCA board.

![AEMSUCA board checkout](https://enderversing.github.io/itp-blog/assets/img/energy/week9/aemsuca.png)

Allison Parrish used this board in one of her own projects.

![AEMSUCA in blog post](https://enderversing.github.io/itp-blog/assets/img/energy/week9/parrish.png)


## Harriet Prototype v1

Watch [this](https://www.instagram.com/reel/DHeEGpXJpe1/).

(I can't embed Instagram reels or videos in my Markdown-based SSG.)

We talked to multiple people who experience housing insecurity and found that this protoype might need a different enclosure because:
* electronics are often stolen by others
* electronics are confiscated/stolen by security guards at shelters
* for older members of our community, carrying around a phone feels strange, which makes it easier to forget/lose

In terms of functionality - texting is not a preferred commnication modality because it feels impersonal, and older members of our community just don't know how to do it.

## Harriet Prototype v2

Enclosure should be wearable to make it harder to lose or steal.

Functionality should focus on voice calls instead of texting.


### Prototype v2.1

The original plan:
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/v1.png)

### Prototype v2.2

The second plan, realizing PCB design is hard:
![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/v2.png)

### Prototype v2.3


The third plan - buy existing development boards with LoRa + Bluetooth capabilities that would connect to existing headphones to enable making phone calls over radio.

Current prototype - purchased:
* [Heltec WiFi LoRa 32](https://heltec.org/project/wifi-lora-32-v3/) (x2)
* Bluetooth (wireless) over-ear headphones with mic (x1)


Current prototype - in progress:

* custom-built Heltec WiFi LoRa 32 enclosure (x2)
  * circle / rectangle base with two hooks (like a smart watch)
    * hooks can be smushed down or pulled out depending on intended use case
    * can be attached to:
      * keychain
      * necklace
      * watch chain
      * hair clip
      * headphones
* power supply for Heltec WiFi LoRa 32 development board (x2)
  * ~~hoping it is possible to siphon the charge of the Bluetooth headphones (it isn't...)~~
  * hoping that my desired supercapacitor + votlage regulator power supply setup is sufficient ~~(probably isn't)~~
    * will try using AAA batteries with VIN (bypass LiPo charger)


![cell phone keychain](https://enderversing.github.io/itp-blog/assets/img/energy/week9/IMG_2957.JPG)

![cell phone keychain](https://enderversing.github.io/itp-blog/assets/img/energy/week9/IMG_2959.JPG)


![cell phone necklace](https://enderversing.github.io/itp-blog/assets/img/energy/week9/IMG_2960.JPG)

![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/inspo.jpg)

![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/future.jpg)

### Prototype v2.3 Power

![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/copilot_power_advice.png)

![](https://enderversing.github.io/itp-blog/assets/img/energy/week9/connect_alkaline.png)

### Prototype v2.3 (soft/hard) enclosure

Talking to resident Kay, we discussed how - in general, not just NiMH - batteries are too big to enable a true wearable like a hair clip or watch. Making a small bag to hold the large batteries would be more realistic.

Combining both hard and soft enclosures would lead to rugged durability but also aesthetic impact.
