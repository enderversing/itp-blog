# Week 10

## Cobalt-Free Power (Maybe)

Jasper reached out to me through multiple channels after I ordered his AEMSUCA board, offering helpful advice.

![AEMSUCA board checkout](https://enderversing.github.io/itp-blog/assets/img/energy/week9/aemsuca.png)

Jasper offered Li-ion capacitors as an alternative to Li-ion batteries without the explosions/fires and cobalt material sourcing. 

Jasper also advised me to switch from the [AEMSUCA](https://www.tindie.com/products/jaspersikken/solar-harvesting-into-supercapacitors/) to the [AEMLIC](https://www.tindie.com/products/jaspersikken/solar-harvesting-into-lithium-ion-capacitor/) board.

## How does voice over LoRa work?

We would reference one of these codebases:
* [LoRa Codec2](https://github.com/dudmuck/lora_codec2)
* [MeshChat](com/liamcottle/reticulum-meshchat)
* [Lyra](https://github.com/google/lyra)
  * requires single-board computer, or a powerful external computer attached to a microcontroller

Voice calls over LoRa are, indeed, theoretically possible.

"LoRa technology offers a maximum bitrate of about 10 kilobits per second." [(source)](https://www.digikey.com/en/articles/speed-development-of-long-range-connectivity-with-a-certified-lorawan-module)

## Hardware

I've always found it difficult to source/purchase Meshtastic boards in a timely and efficient manner. I ordered two Heltec LoRa 32 boards that never arrived and am considering abandoning Meshtastic. 

Meshtastic is not designed for voice anyway, so maybe I'm not missing out on much. Leaving the Meshtastic software would allow me to change the hardware I'm using as well.

Resident Kay told us to design our enclosure around alkaline batteries. Professor Knox told us to build a "looks like" prototype that ignores battery requirements.

**What can I get help with?**    
1. Optimizing the protoyping process is one option. 
2. Also, the shape + functionality of the protoype. We got feedback that the first prototype is easy to steal or lose and that people prefer voice to text. Does that mean, though, that we should make a wearable device enabling phone calls? Maybe that's the wrong conclusion.
