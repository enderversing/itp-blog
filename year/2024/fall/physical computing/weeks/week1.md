# Week 1
`9.5.24`

It's the first week! 

Duties to complete before next week:
* share link to this blog in class spreadsheet
* read Bret Victor + Timo Arnall pieces
* complete interactive electronics labs

I wanted to make a mecha suit previously - explained in [[fall/index]] - but now I feel that I may want to make a game console designed for interactive fiction instead ([[finalproj]]).

I'm thinking tangible computing. My ideas may change further.

## Bret Victor notes
> Hands do two things. They are two utterly amazing things, and you rely on them every moment of the day


I don't appreciate the assumption that all readers are able-bodied and possess hands. 

> Go ahead and pick up a book. Open it up to some page.

Bret continues to make assumptions about an able-bodied reader.


The whole essay reminds me of ["extreme technological optimism"](https://eprint.iacr.org/2015/1162.pdf). I don't feel that Bret is addressing me or people with my  concerns.

> Before we think about how we should interact with our Tools Of The Future, let's consider what a tool is in the first place.

But who is this "we"? I really dislike when writers try to say that they and the reader make up some kind of "we" without describing what that "we" is like or how it came about.

Being generous - I know that ~the point~ is to differentiate the tactile expressiveness of everyday things from the way touch screens rarely provide tactile or haptic feedback. 

I am interested in tangible computing not because of some hypothetical future in which "we" are also marching toward progress, but because of the real-world benefits of tangible computing for accessibility.

We have different visions of tangible computing. Maybe we aren't even both thinking of the same thing, because Bret never says "tangible computing" by name.

## Timo Arnall notes

Is there a reason we are reading pieces from people who worked at Apple? 

Okay. I like this reading a lot better. Timo also uses that dreaded "we", but the points made are more amenable.

I really like discussing the myths around immaterial computing! [Programmed Visions: Software and Memory](https://direct.mit.edu/books/oa-monograph/3341/Programmed-VisionsSoftware-and-Memory) is such a good book that I'm thinking about reading Timo's arguments.

Natural and intuitive design, to add to Timo's disdain, is often natural or intuitive in certain contexts or certain cultures. There is no monolithic human experience, in my opinion, to design computers for. There is no singular, monolithic human intuition that can be leaned on to make designs more natural.

I do think that the fascination with invisible, or immaterial interfaces goes back to [Wendy Chun's timeline](https://direct.mit.edu/books/oa-monograph/3341/Programmed-VisionsSoftware-and-Memory) of the quest for programmable machines.

By design, computers (standard von Neumann computers bought at Best Buy) obscure their inner workings. The trend is to do more of this, not less.

### Lab Notes

**Electricity: The Basics**
* actuators convert electrical energy into other forms of energy
* electronics read changes in electrical properties as information
  * this is interesting!!
  * I wonder if information theory has an connection?
    * probably not...I just saw the word *information* in two places
* transduction changes one type of energy into another
  * devices that do this are transducers
    * so all actuators are transducers?
  
* much of physical computing is figuring out what transducer you need 
  
* voltage measures difference in electrical potential energy
  * what is electrical potential energy?

* current measures magnitude of electron flow 
* resistance is a material's ability to...oppose current (?)
  * measured in Ohms
* loads are what use the source of electrical energy in a circuit and convert it to some other energy

* a short circuit has no load
  * seems undesirable, bad consequences

* make sure the load can take the voltage produced by the source
* we mostly talk about direct current (DC) circuits in our class

* schematic diagrams explain a circuit's flow of electricity

* insulators prevent the flow of electricity
  * resistors *resist* flow but don't block it
  
* capacitors store energy while current flows in
  * release energy once current is removed
  * make sure you take note of its maximum voltage

* diodes permit electricity in one direction
  * LED = light emitting diode 
  
* `voltage = current * resistance`

* `watts = voltage * current`
  * watts = electrical power

* current tends to follow path of least resistance
* in any circuit, total voltage around path of circuit = 0


**Understanding DC Power Supplies**

**V**: Volts

**A**: Amperes

**W**: Watts

**mA**: milliAmperes
* The class website misspelled this!

**VA**: Volt Amperes

**VAC**: Volts AC

**VDC**: Volts DC

**DC**: Direct Current

**AC**: Alternating Current

* most phone chargers output **5V**, which will power an Arduino
  * however, programming may not be possible using a mobile phone charger

* consider the power supply needed for each of your electronics projects
  * what current is consumed by the circuit as a whole?


**Lab: Components**

* a datasheet is a spec sheet
  * describes characteristics of a 
    * sensor
    * electronic component

* voltage regulator
  * different circuits have different voltages
    * Arduino Uno operates at 5V  
    * regulators take a set *range* of DC input and convert it to constant voltage
    * 7800 series regulators
      * left leg connected to input voltage
      * middle leg connected to ground
        * ground is the direction of the flow of electricity
      * right leg is output voltage

* LEDs emit light given  the correct voltage and current
  * as a diode, LEDs are *polarized*
    * only operate when oriented correctly in the circuit
    * **anode** connects voltage
    * **cathode** connects to ground
    * can handle limited current and voltage

* what is an LED lens?

* solderless breadboards are good for prototyping
  * holes on either side of board used as *voltage* and *ground* buses
    * `what is a bus?`
      * columns on sides (positive, negative)
        * specific to this breadboard
        * `which is voltage?`
          * positive?
        * `which is ground?`
          * negative?

* resistors placed in a series
  * reduce voltage
  * limit current

* potentiometer
  * variable resistors
  * movable contact called the *wiper* produces variable resistance
  * trimmer potentiometers are very small

* force sensing resistors
  * change their resistance in response to force

* flex sensing resistors
  * change their resistance as they bend
  * about the length of a finger
  * can measure the bend of a *finger*
    * could measure human finger bend

* force sensing potentiometer
  * value of `_____` changes depending where along its length you progress

* photocell
  * light-dependent resistors
  * increasingly being replaced by phototransistors
    * can be less toxic
    * `which components are considered toxic? why?`
      * trying to avoid heavy metals
        * might be difficult to dispose
        * avoiding e-waste
          * things you don't want in drinking water
          * disposal is a concern

* thermistor
  * resistance changes as temperature changes

* Switches
  * momentary
    * pushbutton
      * remain closed only when you press them
  * toggle
    * stay in one position when you flip them
    * can be used to turn a device on or off
      * because they stay in place

* rotary encoder
  * produces electrical pulses as shaft of encoder is turned
  * what is an [encoder](https://www.pjrc.com/teensy/td_libs_Encoder.html)? what is a shaft? what is an encoder shaft?
    * encodes position
      * always used for position
    * shaft points out


* capacitor
  * ceramic
    * unpolarized
    * small capicitance values
  * electrolytic
    * store more charge than ceramic capacitors
      * longer lasting
    * polarized
      * positive leg
      * negative leg
        * current flows through them more efficiently one way than the other
        * **+** or **-** on one side
  * value of magnitude
    * number
  * order of magnitude
    * ex: microfarad


* diode
  * permit voltage to flow in one direction
    * block it in the other direction

* 1N4001 diodes 
   *  useful for stopping voltage
   *  power diode
      *  capable of carrying more current than other diodes
  
*  Zener diode
   *  after a certain current threshold, they allow current to flow in both directions
  
* transistor
  * electronic switch
  * Darlington transistor
    * usually controls *high-current* loads
  * **MOSFET**
    * Metal Oxide Semiconductor Field Effect Transistors
    * good for controlling high current loads
    * sensitive to static electricity damage

* phototransistors
  * controlled by light instead of electricity
  * can look like an LED
  * what is an *analog input circuit*?

* power jack
  * connect breadboard to DC power supply
  * becoming less common because of USB connectors, USB wall plugs

* battery holder
  * connect batteries to your project
  * `what is a *battery snap*?`
    * keeps battery in place


* servo motor
  * motor + encoder
    * encoder example: potentiometer
    * position/speed readings
    * control messages
      * feedback loop
    * plastic bits are *horns*
      * let you attach motor to mechanism you want to control

* DC motor
  * induction -> rotate central shaft
  * reverse direction of rotation by reversing leads

* motor driver
  * H Bridge
  * enables voltage to be applied across a load in either direction
  * can control direction of DC motors

* electromechanical relay
  * electronic switch
  * slower, prone to wearing out

* screw terminal
  * electrical connectors
  * hold wires in place
    * using clamping screw

* sensor module
  * application-specific integrated circuit
  * read a particular property and produce a measurement


* accelerometer
  * sensors that measure changing acceleration
  * increasingly built into microcontrollers, other devices

* infrared distance ranger
  * measure distance in about a 1 range meter
  * uses infrared light

* ultrasonic distance ranger
  * emit pulsed ultrasonic waves

* speaker
  * cone (paper, plastic) mounted to coil of wire
  * coil mounted next to a magnet
  * current passed through wire induces a magnetic field 
    * attracts or repulses magnet
      * this makes the cone vibrate -> produce sound
      * `is this what happens inside headphones?`
**Lab: Setting up a breadboard**

* when inserting or removing breadboard components, *unplug power supply first*

This diagram is helpful for figuring out which pins are which:

![Arduino Nano 33 pins](/assets/img/pin.png)


finished!

**Lab: Electronics and using a Multimeter**

I couldn't get the LED to light up...

**Lab: Switches**

[//begin]: # "Autogenerated link references for markdown compatibility"
[fall/index]: ../../index.md "beginning a new semester"
[finalproj]: finalproj.md "Final Project"
[//end]: # "Autogenerated link references"
