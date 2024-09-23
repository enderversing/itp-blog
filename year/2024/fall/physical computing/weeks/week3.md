# Week 3

I'm not doing the readings for this week because the professor never asks us about them or references them in class.

It seems that we are supposed to focus on the labs alone, judging by the content of class discussions.

## [Lab: Tone Output Using An Arduino](https://itp.nyu.edu/physcomp/labs/labs-arduino-digital-and-analog/tone-output-using-an-arduino/)

Parts:
* 100-ohm to 220-ohm resistors
* 10-kilohm resistors
* force sensing resistor

I finished part one! I got the speaker working!

![speaker](https://enderversing.github.io/itp-blog/assets/img/week3/part1.png)

I finished part two! I played multiple notes!

![notes](https://enderversing.github.io/itp-blog/assets/img/week3/part2.png)


## [Lab: Servo Motor Control with an Arduino](https://itp.nyu.edu/physcomp/labs/labs-arduino-digital-and-analog/servo-motor-control-with-an-arduino/)

Parts to find:
* potentiometer
* 10-kilohm resistors
* force sensing resistor
* RC servometer
* phototransistor


> `millis()`: Returns the number of milliseconds passed since the Arduino board began running the current program

I'm not sure I understand this.

```
// if your sensor's range is less than 0 to 1023, you'll need to
// modify the map() function to use the values you discovered:
int servoAngle = map(analogValue, 0, 1023, 0, 179);
// move the servo using the angle from the sensor every 20 ms:
  if (millis() - lastMoveTime > 20) {
    servoMotor.write(servoAngle);
    lastMoveTime = millis();
  }
```

I can guess that the range of the servo motor is based on the bits of memory the Arduino can handle.

I understand that 1024 is `2^10`, but what is 180? That number seems arbitrary. 

Why not 256? I could be misunderstanding something fundamental.

Moving the servo every 20 seconds using a greater than `>` operator confuses me. I'm used to seeing a modulo operator `%` for this use case but I should still be able to understand this.

Now that I'm reading the code comments more closely it makes a little more sense. 

There is no absolute value `| |` operator so we know `millis()` is greater than `lastMoveTime`, or else the difference between them would be negative (as far as I can tell).

`lastMoveTime` starts at 0. When `millis()` reaches 20 seconds, our code changes the angle of the servo motor, and we update the value of `lastMoveTime`.

Okay. Next, I will post pictures.

I finished the lab! I was touching the force sensing resistor in order to turn the servo motor.

![servo motor](https://enderversing.github.io/itp-blog/assets/img/week3/second_lab.gif)
