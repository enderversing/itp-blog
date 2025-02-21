# Week 4

## Weekly Reading

I tried to read Chapter 3 of Energy. I did skim through the first few pages. It is dry.

## Kinetic Energy Project

I received a large motor in the mail.




The gear produces so much torque that I have to crank it with pliers.

This is a gif in which I use the motor to light up the LED on a Feather M0 with LoRa (briefly)

Open Circuit Voltage: 4-7 V

Short Circuit Current: .7-1.0 A

![LED](https://enderversing.github.io/itp-blog/assets/img/kinetic_2.gif)


The voltage regulator is for 3.3 V but the voltage that comes out of the voltage regulator is 3.27 V (not 3.3 V exactly).

---

I cannot get the Feather M0 to light up (consistently) at the moment, probably for the same reason that I struggle to program it.

When I plug in the Feather M0 to my computer, it blinks and fades quickly. At first, I thought the board was dead.

![Feather M0 blink then fade](https://enderversing.github.io/itp-blog/assets/img/energy/week4/1.gif)

I have to double click the reset button twice to turn on the board while it is plugged into my laptop. 
![Feather M0 blinking](https://enderversing.github.io/itp-blog/assets/img/energy/week4/2.gif)

I decided to try the Arduino Nano 33 IoT instead. Predictably, the board powered on without issue.
![Nano 33 IoT consistent blinking](https://enderversing.github.io/itp-blog/assets/img/energy/week4/3.gif)

I measured the open circuit voltage as 3.28 V.
![cranking, multimeter, dimly lit hallway](https://enderversing.github.io/itp-blog/assets/img/energy/week4/4.gif)

The short circuit current seems to range from ~.6-.9 A.
![cranking, multimeter, dimly lit hallway](https://enderversing.github.io/itp-blog/assets/img/energy/week4/5.gif)

