# Electronic Horn | Car / Bike / Bicycle | 555 386 |
The LM555 generates an electronic horn signal which is amplified by an LM386.
The horn can be used on a car, scooter, cycle and motorbike.

**Full Video:**
[![Musical Bell](https://img.youtube.com/vi/yDZJ3qElCCo/maxresdefault.jpg)](https://youtu.be/yDZJ3qElCCo)

**Order PCB:**  [PCBWay](https://bit.ly/2VrASCW)

## Electronic Components
| Qty | Component | Buy |
| ------------- | ------------- | ------------- |
| 1 | IC 555 |[AliExpress](http://s.click.aliexpress.com/e/sCv1ACC) |
| 1 | IC LM386 |[AliExpress](http://s.click.aliexpress.com/e/c1pixqXe) |
| 2 | IC Holder |[AliExpress](http://s.click.aliexpress.com/e/cHvnfsrA) |
| 1 | 10Ω 1KΩ 2KΩ Resistor |[AliExpress](http://s.click.aliexpress.com/e/bh4eqrQs) |
| 3 | 10KΩ Potentiometer |[AliExpress](http://s.click.aliexpress.com/e/bN0jkp8y) |
| 1 | Tactile Momentary Push Buttons |[AliExpress](http://s.click.aliexpress.com/e/c77Ajrpq) |
| 1 | 5mm LED |[AliExpress](http://s.click.aliexpress.com/e/wuFpLXS) |
| 1 | 0.1uF 10uF 100uF 220uF Capacitor |[AliExpress](http://s.click.aliexpress.com/e/c9FHzl5W) |
| 1 | 10nF 47nF 0.1uF Capacitor |[AliExpress](http://s.click.aliexpress.com/e/SX7eHuG) |
| 1 | Speaker |[AliExpress](http://s.click.aliexpress.com/e/brMJh46c) |
| 1 | 9V Battery Holder |[AliExpress](http://s.click.aliexpress.com/e/c3jbp72Y) |
| 1 | 9V Battery |[AliExpress](http://s.click.aliexpress.com/e/bbDirGHE) |
| 1 | PCB |[AliExpress](http://s.click.aliexpress.com/e/dhgwzKY) |


| Tools | Buy |
|--|--|
|Soldering Iron|[AliExpress](http://s.click.aliexpress.com/e/E83bSJI) |
|Soldering Wire|[AliExpress](http://s.click.aliexpress.com/e/PdhB0nm) |
|Mini PCB Hand Drill + Bits|[AliExpress](http://s.click.aliexpress.com/e/b93tomjI) |
|Wire Cutter|[AliExpress](http://s.click.aliexpress.com/e/bHFL9vLi) |
|Wire Stripper|[AliExpress](http://s.click.aliexpress.com/e/4yJWedw) |
|Soldering Helping Hands|[AliExpress](http://s.click.aliexpress.com/e/cAQ2StNm) |

## Working
**LM555/NE555:**

The 555 is a highly stable device for generating accurate time delays or oscillation. Additional terminals are provided for triggering or resetting if desired. For stable operation as an oscillator, the free running frequency and duty cycle are accurate controlled with two external resistors and one capacitor. The circuit may be triggered and reset on falling waveforms, and he output circuit can source or sink up to 200mA or drive TTL circuits.

![Pinout](https://github.com/jonathanrjpereira/555-Electronic-Car-Horn/blob/master/img/pinout.png)
![Pin Description](https://github.com/jonathanrjpereira/555-Electronic-Car-Horn/blob/master/img/pindescription.png)

**LM386**

The LM386 is a power amplifier designed for use in low voltage consumer applications. The gain is internally set to 20 to keep external part count low, but the addition of an external resistor and capacitor between pins 1 and 8 will increase the gain to any value from 20 to 200.

The inputs are ground referenced while the output automatically biases to one-half the supply voltage.

![Pinout](https://github.com/jonathanrjpereira/555-Electronic-Car-Horn/blob/master/img/386pinout.png)
![Pin Description](https://github.com/jonathanrjpereira/555-Electronic-Car-Horn/blob/master/img/386pindescription.png)

**Circuit:**

An LM555 is used to generate the horn signal. The LM555 is connected such that it will trigger itself and free run as an astable multivibrator. The external capacitor charges through Ra+Rb and discharges through Rb. Thus the duty cycle may be precisely set by the ratio of these two resistors.

In this mode of operation, the capacitor charges and discharges between 1/3 VCC and 2/3 VCC. Hence the charge and discharge times, and therefore the frequency are independent of the supply voltage.

The change time (output high) is given by:
<img src="https://latex.codecogs.com/gif.latex?\inline&space;t_{1}&space;=&space;0.693&space;(R_{A}&space;&plus;&space;R_{B})C" title="t_{1} = 0.693 (R_{A} + R_{B})C" />

And the discharge time (output low) by:
<img src="https://latex.codecogs.com/png.latex?\inline&space;t_{2}&space;=&space;0.693(R_{B})C" title="t_{2} = 0.693(R_{B})C" />

Thus the total period is:
<img src="https://latex.codecogs.com/png.latex?\inline&space;T&space;=&space;t_{1}&space;&plus;&space;t_{2}&space;=&space;0.693(R_{A}&plus;2R_{B})C" title="T = t_{1} + t_{2} = 0.693(R_{A}+2R_{B})C" />

The frequency of oscillation is:
<img src="https://latex.codecogs.com/png.latex?\inline&space;f&space;=&space;\frac{1}{T}&space;=&space;\frac{1.44}{(R_{A}&plus;2R_{B})C}" title="f = \frac{1}{T} = \frac{1.44}{(R_{A}+2R_{B})C}" />

Hence
<img src="https://latex.codecogs.com/png.latex?\inline&space;R_{B}&space;=&space;\frac{1}{2}(\frac{1}{.7C&space;\times&space;f}&space;-&space;R_{A})" title="R_{B} = \frac{1}{2}(\frac{1}{.7C \times f} - R_{A})" />

![Block Diagram](https://github.com/jonathanrjpereira/555-Electronic-Car-Horn/blob/master/img/BD.png)

A momentary switch acts as an input trigger that enables the astable multivibrator to generate a signal of variable frequency.
This signal is then sent to an amplification unit before it is played through a speaker. The frequency and volume of the horn sound can be varied as shown.

![Schematic](https://github.com/jonathanrjpereira/555-Electronic-Car-Horn/blob/master/img/sch.png)

A potentiometer R3 (Rb) is varied in order to change the frequency of the signal generated by the LM555. The signal is then passed to the LM386 for amplification.

The input signal is passed through another potentiometer R4 before it reaches the LM386. This pot is used to change the amplitude (volume) of the input signal before amplification.

The LM386 has a 10uF capacitor and 10K potentiometer R5 connected between pins 1 and 8. By varying this pot, we can change the gain of the amplifier and thus the volume of the amplified signal.

A push button/ momentary switch is used to turn on the circuit thereby producing a loud horn sound. Capacitors connected across the supply terminals are used to minimize any noise signals.


## Contributing🛠
Are you an engineer or hobbyist who has a great idea for a new feature in this project? Maybe you have a good idea for a bug fix? Feel free to grab our code & schematics from Github and tinker with it. Don't forget to smash ⭐️ & the Pull Request button.

[![alt text][1.1]][1] [![alt text][2.1]][2] [![alt text][3.1]][3]

[1.1]: https://github.com/jonathanrjpereira/Social-Media-README/blob/master/youtube.png (YouTube)
[2.1]: https://github.com/jonathanrjpereira/Social-Media-README/blob/master/instagram.png (Instagram)
[3.1]: https://github.com/jonathanrjpereira/Social-Media-README/blob/master/github.png (GitHub)

[1]: https://www.youtube.com/channel/UCRW-41O1vy98KKgJRQoYzdg
[2]: https://www.instagram.com/electroguruji/
[3]: https://github.com/jonathanrjpereira
