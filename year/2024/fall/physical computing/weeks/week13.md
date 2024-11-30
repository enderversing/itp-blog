# Week 13

## Hardware Progress

I expect that I will be racing against Tuesday's deadline to produce visual documentation of the actual hardware I'm making.
I'm going to Doc Lab next week, so hopefully I'll be done in time for that session.

## I made a site for this project

I made a [site for the Harriet Network](https://harrietnetwork.com)! 

[(What is that?)](https://harrietnetwork.com/faq)

## Copilot Chat

I had the following chat with [Copilot](https://copilot.microsoft.com) and I think it may have possibly saved my Physical Computing project. I am documenting this chat transcript for transparency and also for my own records:

---

**Q:** How do I connect an Arduino Nano 33 IoT and LoRa radio to an Android or iOS smartphone?

**A:** Connecting an Arduino Nano 33 IoT and a LoRa radio to a smartphone involves a few steps. Here's a general guide to get you started:

### **Connecting Arduino Nano 33 IoT to a Smartphone:**

1. **Bluetooth Connection:**
   - The Arduino Nano 33 IoT has built-in Bluetooth Low Energy (BLE) capabilities.
   - You can use the ArduinoBLE library to create a BLE service and characteristics.
   - Use an app like **Arduino Create** on your smartphone to connect and interact with the board.

2. **Steps:**
   - Open the Arduino Cloud Editor.
   - Go to the Libraries tab and search for the ArduinoBLE library.
   - Open the LED sketch under Examples > Peripheral.
   - Rename the sketch as desired and upload it to the Nano 33 IoT.
   - Connect your smartphone to the Nano 33 IoT via Bluetooth using the Arduino Create app.

### **Connecting LoRa Radio to a Smartphone:**

1. **Using Meshtastic:**
   - Meshtastic is a popular app for LoRa communication.
   - Download and install the Meshtastic app on your Android or iOS device.
   - Follow the instructions to set up and sync your LoRa devices.

2. **Steps:**
   - Connect your LoRa radio to your smartphone using a USB OTG cable.
   - Open the Meshtastic app and follow the setup instructions to configure your LoRa radio.
   - Use the app to send and receive messages over LoRa.

### **Additional Resources:**
- **Arduino Documentation:** [Connecting an Arduino Nano 33 IoT to a mobile device over Bluetooth](https://forum.arduino.cc/t/connecting-an-arduino-nano-33-iot-to-a-mobile-device-over-bluetooth-classic/967208)
- **Meshtastic Documentation:** [Initial Configuration](https://meshtastic.org/docs/getting-started/initial-config/)
- **DIY Projects:** [DIY Smartphone LoRa Connection](https://www.hackster.io/pulsartronic/diy-smartphone-lora-connection-bde258)

Would you like more detailed instructions on any specific part of the process?


**Q:** Do I need any parts besides the LoRa radio and Arduino in order to add LoRa communication to a smartphone?

**A:** Besides the LoRa radio and Arduino Nano 33 IoT, you might need a few additional components to enable LoRa communication with a smartphone. Here's a list:

1. **Antenna:** For better range and signal strength, you'll need an antenna compatible with your LoRa module.

2. **Battery or Power Supply:** Depending on your project setup, you may need a battery pack or a power supply to power the Arduino and LoRa module.

3. **USB OTG Cable:** If you're planning to connect your LoRa radio directly to your smartphone via USB, you'll need a USB On-The-Go (OTG) cable.

4. **Connectors and Cables:** You might need jumper wires, connectors, and possibly a breadboard to connect the LoRa module to the Arduino.

5. **Enclosure (Optional):** For a more robust and portable setup, consider an enclosure to house your components.

### **Summary:**
- **Antenna**
- **Battery or Power Supply**
- **USB OTG Cable**
- **Connectors and Cables**
- **Enclosure (Optional)**

These additional components will help ensure a successful connection and enhance your project’s performance. Would you like more details on how to set everything up?

Should I connect the Arduino Nano 33 IoT to the smartphone devices using BLE, USB OTG, or both? What are the pros and cons of each choice?

You can connect the Arduino Nano 33 IoT to a smartphone using either Bluetooth Low Energy (BLE) or USB On-The-Go (OTG), depending on your project needs. Here are the pros and cons of each method to help you decide:

### **Bluetooth Low Energy (BLE):**
**Pros:**
- **Wireless:** No physical connection needed, which allows for more flexibility and mobility.
- **Low Power:** BLE consumes less power, making it suitable for battery-powered applications.
- **Ease of Use:** Simple to set up with existing libraries and apps (e.g., Arduino Create).
- **Range:** BLE provides a decent range for short-distance communication (up to 100 meters in ideal conditions).

**Cons:**
- **Data Rate:** Lower data transfer rates compared to wired connections.
- **Latency:** May experience higher latency compared to USB OTG.
- **Interference:** Susceptible to interference from other wireless devices.

### **USB On-The-Go (OTG):**
**Pros:**
- **High Data Rate:** Faster data transfer rates, which can be beneficial for applications requiring high-speed communication.
- **Low Latency:** Minimal latency compared to wireless connections.
- **Power Supply:** Can provide power to the Arduino, eliminating the need for an additional power source.

**Cons:**
- **Wired Connection:** Requires a physical connection via a USB OTG cable, limiting mobility.
- **Compatibility:** Not all smartphones support USB OTG, so you need to verify compatibility.
- **Power Consumption:** May consume more power from the smartphone compared to BLE.

### **Combination of Both:**
Using both BLE and USB OTG can provide flexibility and redundancy. For instance, you can use BLE for regular communication and switch to USB OTG for tasks requiring higher data rates or when updating firmware.

### **Decision Factors:**
- If you prioritize **mobility and power efficiency**, BLE is the better choice.
- If you need **high-speed data transfer and low latency**, go with USB OTG.
- If your project demands **flexibility and redundancy**, consider using both methods.

I hope this helps! Would you like guidance on setting up either of these connections?

**Q:** Do you think a phone accessory or an actual phone alternative with a built in screen and keyboard is more useful for creating a telecommunications device that can communicate over long distances without WiFi or mobile data? Would a LoRa enabled accessory be better, or a complete phone alternative with a LoRa radio embedded?

**A:** That's an interesting question! Both options have their pros and cons, so it really depends on your specific needs and preferences.

### Phone Accessory with LoRa
- **Pros**: 
  - **Cost-effective**: You can use your existing phone, which means you only need to purchase the accessory.
  - **Flexibility**: You can switch between regular phone use and long-distance communication as needed.
  - **Ease of use**: Integrates with your current phone setup, making it easier to handle.

- **Cons**: 
  - **Limited functionality**: The accessory might not offer all the features of a dedicated device.
  - **Compatibility**: Not all phone models may support the accessory, limiting its usability.

### Complete Phone Alternative with Embedded LoRa Radio
- **Pros**: 
  - **Dedicated functionality**: Designed specifically for long-distance communication, potentially offering better performance.
  - **All-in-one solution**: No need for additional accessories or compatibility concerns.
  - **Customization**: Can be tailored for specific use cases, such as emergency communication or remote areas.

- **Cons**: 
  - **Higher cost**: You'll need to invest in a new device, which can be more expensive.
  - **Less versatile**: Limited to communication purposes, unlike a regular phone.

### Conclusion
If you need a **cost-effective and flexible solution**, a LoRa-enabled accessory might be the way to go. However, if you require **dedicated and potentially more reliable long-distance communication**, a complete phone alternative with an embedded LoRa radio could be a better choice.

What do you think? Do you have a specific use case in mind?

___

Q: Hi! I want to create an wooden enclosure for a circuit wired using a 5cm x 7cm proto-board. What size and kind of wood should I buy?

A: That sounds like an exciting project! To create a wooden enclosure for your 5cm x 7cm proto-board, here’s what you should consider:

### Size
1. **Inner Dimensions:** Ensure there’s some extra space around the proto-board for wiring and components. A good rule of thumb is to add at least 1-2cm on each side. So, for a 5cm x 7cm board, the inner dimensions of your enclosure should be around 7cm x 9cm.
2. **Height:** Depending on the height of your components, you might need anywhere from 3-5cm of internal height. Measure the tallest component on your board and add a little extra space to avoid any issues.

### Wood Type
1. **Plywood:** It's sturdy, inexpensive, and easy to work with. Plywood is a great option for a small enclosure like this.
2. **Hardwood:** If you want something more aesthetically pleasing, you could use a hardwood like oak, walnut, or cherry. It’s more expensive but offers a beautiful finish.
3. **Softwood:** Woods like pine or cedar are also good options if you prefer something lightweight and easy to cut.

### Thickness
For small enclosures, a thickness of around 0.5cm (5mm) should be sufficient. It provides enough strength without being too bulky.

### Additional Tips
1. **Ventilation:** Consider adding holes or slots for ventilation if your circuit generates heat.
2. **Mounting:** Plan how you will mount the proto-board inside the enclosure. You might need standoffs or adhesive mounts.
3. **Finish:** Sand the wood smooth and consider applying a finish to protect it and give it a nice look.

Would you like more specific guidance on any of these steps? Or maybe some design ideas for the enclosure?

Q: Wait, how big does the block of wood need to be? I still don't get it.

A: I understand, let's break it down step-by-step to make it clearer:

### Dimensions
For a 5cm x 7cm proto-board, let's figure out the size of the wood block needed:

1. **Length & Width:** You want to add some extra space around the proto-board for wiring and ease of fitting. Adding about 1-2cm on each side:
   - **Length:** 7cm (board length) + 2cm (extra space) = 9cm.
   - **Width:** 5cm (board width) + 2cm (extra space) = 7cm.

   So, the base of your enclosure should be around 9cm x 7cm.

2. **Height:** Measure the tallest component on your board and add some extra space. If your tallest component is 2cm, you might want the enclosure to be at least 3-4cm in height.

### Wood Block Size
If you're buying a single piece of wood and planning to cut it, you'll need to account for all sides of the enclosure:

- **Bottom:** 9cm x 7cm.
- **Top:** 9cm x 7cm (same as the bottom).
- **Sides (Length):** You'll need 2 pieces, each 9cm x 4cm (height).
- **Sides (Width):** You'll need 2 pieces, each 7cm x 4cm (height).

### Total Wood Required
If you want to buy a block and cut all pieces from it, you'll need a block that's at least:
- **Width:** 9cm (longest dimension).
- **Height:** 4cm.
- **Length:** Add up all pieces for the length: 9cm (bottom) + 9cm (top) + 9cm (side) + 9cm (side) = 36cm.

So, a block that is at least 9cm wide, 4cm high, and 36cm long should be sufficient. 

Would you like more details or tips on building your enclosure?

Q: This is great. Where can I buy a block of wood with those dimensions?

A: You can find wood blocks in various sizes at local hardware stores, lumber yards, or online retailers. Here are a few options:

1. **Local Hardware Stores:** Stores like Home Depot, Lowe's, or your local hardware store often carry wood in different sizes. You can ask them to cut the wood to your specific dimensions if needed.
2. **Online Retailers:** Websites like Amazon, Etsy, and specialized wood suppliers often have wood blocks in various sizes. You can search for "wood block 9cm x 4cm x 36cm" to find suitable options.
3. **Lumber Yards:** Local lumber yards can provide custom-cut wood blocks to your exact specifications. It's a good idea to call ahead and check if they offer this service.

Would you like me to help you find a specific retailer or provide more details on any of these options?

Q: I want to get this block shipped to me by Monday morning, ideally. I'm on a tight timeline.

A; Got it! Here are a few online retailers that offer quick shipping and can provide wood blocks in the dimensions you need:

1. **Timbersource**: They offer a made-to-measure service where you can specify the exact dimensions you need. You can order online and have it delivered quickly.
2. **Wickes**: They have a variety of planed square edge timber that can be cut to size. Check their delivery options for expedited shipping.
3. **Amazon**: You can search for wood blocks and filter the results by delivery date to find options that can arrive by Monday morning.

Would you like me to help you find more specific options or place an order for you?

Q: Which of those options would ship to the US by Monday morning?

A: Based on my search, **Amazon** is the best option for shipping to the US by Monday morning. They offer **AmazonGlobal Standard Shipping** and **Priority Global Shipping**, which can deliver within 2-4 business days. 

Would you like me to help you find a specific wood block on Amazon, or do you need assistance with anything else?

---

Ugh. I do not like Amazon.

--- 
Q: Please help me find a specfic wood block on Amazon.

A: I found a few options on Amazon that might work for you:

1. **Unfinished MDF Wood Blocks for Crafts** - These are 1 inch thick wooden square blocks (4x4 inches) and come in a pack of 4. You can order multiple packs to get the size you need.
2. **Solid Hard Wood Blocks** - These are 5 1/4 inches long by 2 inches wide and come in a pack of 6. You can cut them to your desired size.
3. **Bright Creations Unfinished Wood Rectangles for Crafts** - These are 6x4 inches and come in a pack of 4. You can also order multiple packs and cut them to size.

Would you like me to help you find more options or place an order for you?


Q: For each option, how many blocks of each would I need for this specific project?

A: Let's figure out how many blocks you'll need for each option, based on the dimensions of your enclosure:

### 1. **Unfinished MDF Wood Blocks for Crafts** (4x4 inches, pack of 4)
- **Bottom/Top Pieces:** 9cm x 7cm is approximately 3.5 inches x 2.75 inches.
- **Side Pieces (Length):** 9cm x 4cm is approximately 3.5 inches x 1.6 inches.
- **Side Pieces (Width):** 7cm x 4cm is approximately 2.75 inches x 1.6 inches.

Each block is 4x4 inches, so you'll need to cut them down to the sizes mentioned above:
- Bottom/Top: Each block can be used for one bottom or top piece.
- Sides (Length/Width): Each block can be cut into the smaller side pieces, but you may need additional blocks to have enough material.

### 2. **Solid Hard Wood Blocks** (5 1/4 inches long x 2 inches wide, pack of 6)
- Bottom/Top: 5.25 inches is a bit shorter than the required length, so you may need to combine pieces or get creative with your design.
- Sides (Length/Width): Each block can be used for the smaller side pieces.

### 3. **Bright Creations Unfinished Wood Rectangles for Crafts** (6x4 inches, pack of 4)
- Bottom/Top: Each rectangle is 6x4 inches, so you would need to piece together two rectangles to cover the 9cm x 7cm area. 
- Sides (Length/Width): Each rectangle can be used for the side pieces, with some cutting.

### Summary
For a 9cm x 7cm x 4cm enclosure:
- **Unfinished MDF Wood Blocks for Crafts**: You may need around 4-6 packs (depending on how efficiently you cut the blocks).
- **Solid Hard Wood Blocks**: These may not be ideal for bottom/top but could work for sides. You might need multiple packs.
- **Bright Creations Unfinished Wood Rectangles for Crafts**: You may need around 3-4 packs for the entire enclosure.

Since you’re on a tight timeline, it's essential to consider the cutting and assembly process. 

Which option do you think will work best for you? Or do you need more assistance?

Q: Can you provide links to option 1 and 3? The links from above didn't work for me.

A; Sure! Here are the updated links for the options:

1. **Unfinished MDF Wood Blocks for Crafts** (4x4 inches, pack of 4): [Amazon Link](https://www.amazon.com/Bright-Creations-Unfinished-Blocks-Crafts/dp/B07R51CY99)
2. **Bright Creations Unfinished Wood Rectangles for Crafts** (6x4 inches, pack of 4): [Amazon Link](https://www.amazon.com/Bright-Creations-Unfinished-Rectangle-Blocks/dp/B07R4YD1FF)

I hope these work for you! If you need any more assistance, feel free to ask.

 ---

 Wow. I'm not sure about spending this much without even knowing that what I'm buying will be useful.

![Amazon price](https://enderversing.github.io/itp-blog/assets/img/week13/cost.png)

--- 

Q: What enclosure from Adafruit (does not have to be made of wood) would work for this project?

A: Here are a few Adafruit enclosures that could work for your project:

1. **Small Plastic Project Enclosure - Weatherproof with Clear Top** (Product ID: 903)
   - **Dimensions:** 100mm x 68mm x 36mm
   - **Material:** Machinable ABS plastic with a clear polycarbonate cover
   - **Features:** Weatherproof with a built-in gasket seal

2. **Extruded Aluminum Enclosure Box - 100mm x 67mm x 26mm** (Product ID: 2229)
   - **Dimensions:** 100mm x 67mm x 26mm
   - **Material:** Solid anodized aluminum
   - **Features:** Lightweight, durable, easy to machine or drill

3. **Flanged Weatherproof Enclosure With PG-7 Cable Glands** (Product ID: 3931)
   - **Dimensions:** 100mm x 68mm x 36mm
   - **Material:** Machinable ABS plastic with a tough polycarbonate cover
   - **Features:** Weatherproof with built-in gasket seal and mounting flanges

These enclosures should provide a good fit for your 5cm x 7cm proto-board with some room for wiring and components. You can find them on the Adafruit website:

- [Small Plastic Project Enclosure - Weatherproof with Clear Top](^https^://www.adafruit.com/product/903)
- [Extruded Aluminum Enclosure Box - 100mm x 67mm x 26mm](^https^://www.adafruit.com/product/2229)
- [Flanged Weatherproof Enclosure With PG-7 Cable Glands](^https^://www.adafruit.com/product/3931)

Would you like more information on any of these options?

Q: Can you provide an alternative to the aluminum? I guess I'm wondering which of these options is the easiest to work with.

A: Sure! If you're looking for an alternative to aluminum that's easy to work with, the **Small Plastic Project Enclosure - Weatherproof with Clear Top** (Product ID: 903) from Adafruit is a great option. It's made of machinable ABS plastic with a clear polycarbonate cover, making it easy to cut and modify if needed. Plus, it's weatherproof and has a built-in gasket seal.

Would you like more details on this enclosure or help with anything else?

Q: Can you show me options for completely clear enclosures that would fit my project's dimensions, or for enclosures in different colors?

A: Sure! Here are some options for clear and colored enclosures that would fit your project's dimensions:

### Clear Enclosures
1. **Polycase Clear Plastic Cover Electrical Box** - These enclosures are made from durable, UV-stable polycarbonate and come with a clear cover for easy visual access to internal components. They are available in various sizes, including options that should fit your 9cm x 7cm x 4cm requirement.
   - [Polycase Clear Plastic Cover Electrical Box](^https^://www.polycase.com/clear-cover-enclosures)

2. **Mouser Electronics Clear Enclosures** - Mouser offers a wide range of clear enclosures suitable for electronics projects. You can filter the results by size and cover color to find the perfect fit.
   - [Mouser Electronics Clear Enclosures](^https^://www.mouser.com/c/enclosures/enclosures-boxes-cases/?color=Clear)

### Enclosures in Different Colors
1. **IP Enclosures UK Colored Electrical Enclosures** - They offer enclosures in various colors, including RAL7035 Grey, RAL6005 Moss Green, RAL2000 Orange, and R13 Signal Red. You can choose the color that best suits your project.
   - [IP Enclosures UK Colored Electrical Enclosures](^https^://www.ipenclosures.co.uk/coloured-electrical-enclosures/)

2. **Hammond Manufacturing Colored Enclosures** - Hammond offers enclosures in different colors, such as black, white, and gray. These enclosures are made from ABS plastic and are suitable for various indoor and outdoor applications.
   - [Hammond Manufacturing Colored Enclosures](^https^://www.digikey.com/en/products/detail/hammond-manufacturing/1555VALGY/13165462)

Would you like more details on any of these options or help with anything else?


Q: Wait, I would prefer Adafruit options.


A: Got it! Here are some Adafruit options for clear and colored enclosures:

### Clear Enclosures
1. **Clear Enclosure for Arduino or Metro** (Product ID: 3597)
   - **Dimensions:** 75mm x 60mm x 19.5mm (3.0" x 2.4" x 0.8")
   - **Material:** Clear plastic
   - **Features:** Fits classic Arduino boards, easy to machine, drill, cut, and shape
   - **Link:** [Adafruit Clear Enclosure for Arduino or Metro](https://www.adafruit.com/product/3597)

2. **Small Plastic Project Enclosure - Weatherproof with Clear Top** (Product ID: 903)
   - **Dimensions:** 100mm x 68mm x 36mm (3.9" x 2.7" x 1.4")
   - **Material:** Machinable ABS plastic with a clear polycarbonate cover
   - **Features:** Weatherproof with a built-in gasket seal
   - **Link:** [Adafruit Small Plastic Project Enclosure - Weatherproof with Clear Top](https://www.adafruit.com/product/903)

### Colored Enclosures
1. **White Enclosure for Arduino** (Product ID: 271) - Discontinued, but similar options are available
2. **Smoke Translucent Enclosure for Arduino** (Product ID: 821)
   - **Dimensions:** 91mm x 126mm x 34mm (3.6" x 5.0" x 1.3")
   - **Material:** Gray translucent plastic
   - **Features:** Easy to machine, drill, cut, and shape
   - **Link:** [Adafruit Smoke Translucent Enclosure for Arduino](https://www.adafruit.com/product/821)

Would you like more details on any of these options or help with anything else?

---

This looks more reasonable. I wanted my enclosure to be biodegradable, but I didn't make it in time.

![Adafruit price](https://enderversing.github.io/itp-blog/assets/img/week13/better_cost.png)
