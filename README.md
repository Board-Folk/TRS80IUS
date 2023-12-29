# TRS80IUS

A remake of the TRS-80 Model I 1700069G motherboard.

![Built Board in Green](https://github.com/Board-Folk/TRS80IUS/blob/main/images/builtboard_usv1.0_small.jpg)

This reposistory contains the BOM, gerbers and Kicad files for a remake of the final version as far as we know, of the TRS-80 Model I original American version motherboard and some related projects and files. This project spawned after publishing its sister project, a recreation of the [TEC, Japanese version which can be found here](https://github.com/Board-Folk/TRS80IJP).

This is intended as a replica, but additional headers have been provided for the common modification of the 8 bit character set - "BIT6" and "D6" - and "L8" for connection of a character ROM substitute like the Gendon3 module. If original operation with 7-bit characters is required, solder jumper UC should be connected. No additional factory bodge capacitors were added either, for example the ones for the horizontal and vertical sync stabalization. You'll still need to add those yourself.

## Version 1.1 Bill-of-Materials

All resistors 1/4W unless specified. Suggested substitutes might be wrong. Any feedback welcome.

|Qty|Reference(s)|Value|Type|Notes|
|:--:|:--:|:--:|:--:|:--:|
|1|C1|220uF 16V|Electrolytic Capacitor||
|6|C2, C4, C5, C10, C11, C57|10uF 16V|Electrolytic Capacitor||
|1|C6|100uF 16V|Electrolytic Capacitor||
|1|C8|2200uF 35V|Electrolytic Capacitor (Axial)||
|1|C9|10000uF 16V|Electrolytic Capacitor (Axial)||
|1|C42|22uF 16V|Electrolytic Capacitor||
|1|C26|0.047uF|Film Capacitor||
|1|C27|0.022uF|Film Capacitor||
|35|C16-C19, C22, C23, C28-C34, C35-C39, C40, C41, C44-C56, C58, C59|100nF|Ceramic Capacitor||
|4|C3, C7, C14, C15|10nF|Ceramic Capacitor||
|2|C12, C13|470pF|Ceramic Capacitor||
|1|C20|330pF|Ceramic Capacitor||
|1|C21|750pF|Ceramic Capacitor||
|2|C24, C25|220pF|Ceramic Capacitor||
|1|C43|47pF|Ceramic Capacitor||
|1|CR1|1N4735A|6.2V Zener Diode||
|1|CR2|1N4733A|5.1V Zener Diode||
|2|CR9, CR10|1N982|75V Zener Diode||
|5|CR3-CR7|1N4148|Small Signal Diode||
|1|CR8|S2V B20|Rectifier||
|1|Q1|MPS3904|Transistor TO-92||
|2|Q2, Q5|MPS3906|Transistor TO-92||
|1|Q3|TIP29A|Transistor TO-220||
|1|Q4|2N6594|Transistor TO-3|See Links|
|1|Q6|MJE34|Transistor TO-220|See Links|
|1|R18|5R6 3W|Resistor||
|1|R4|0R33 2W|Resistor||
|1|R1|68R 1/2W|Resistor||
|1|R19|220R 1/2W|Resistor||
|1|R2|2K7|Resistor||
|1|R3|750R|Resistor||
|2|R5, R10|1K|Potentiometer|Piher PT10LH01|
|4|R6, R7, R16, R53|1K2|Resistor||
|1|R8|100K|Resistor||
|3|R9, R11, R12|3K3|Resistor||
|1|R13|2K2|Resistor||
|1|R14|12K|Resistor||
|1|R15|1K5|Resistor||
|1|R17|2K|Resistor||
|2|R20, R21|100K|Potentiometer|Piher PT10LH01|
|1|R22|75R|Resistor||
|1|R23|120R|Resistor||
|1|R24|680K|Resistor||
|1|R25|1.8M|Resistor||
|2|R26, R42|1M|Resistor||
|2|R27, R64|330R|Resistor||
|1|R28|270R|Resistor||
|1|R29|1.8K|Resistor||
|1|R30|47R|Resistor||
|1|R31|10R|Resistor||
|5|R32, R43, R44, R47, R65|10K|Resistor||
|2|R33, R36|360K|Resistor||
|5|R34, R35, R38, R41, R45|470K|Resistor||
|1|R37|560K|Resistor||
|16|R39, R40, R48-R51, R57-R62, R66-R69|4K7|Resistor||
|2|R46, R52|910R|Resistor||
|2|R54, R55|7K5|Resistor||
|1|R56|220K|Resistor||
|1|R63|4.7K|Resistor||
|1|R167|100R|Resistor||
|1|Z40|Z80CPU|IC||
|1|Z29|MCM667X|IC|Character ROM|
|8|Z13-Z20|4116 RAM|IC||
|7|Z45-Z48, Z61-Z63|2102 RAM|IC|8 if modified for 8 bit characters|
|1|Z33|2364 ROM|IC||
|1|Z34|2332 ROM|IC||
|2|Z1, Z2|LM723|IC||
|1|Z41|75452|IC||
|1|Z4|LM3900N|IC||
|1|Z5|74C00|IC||
|2|Z6, Z57|74C04|IC||
|3|Z7, Z69, Z70|74LS74|IC||
|1|Z8|74LS153|IC||
|3|Z9, Z42, Z52|74LS04|IC||
|2|Z10, Z11|74LS166|IC||
|4|Z12, Z32, Z50, Z65|74LS93|IC||
|1|Z21|74LS156|IC||
|11|Z22, Z38, Z39, Z44, Z55, Z60, Z67, Z68, Z72, Z75, Z76|74LS367|IC||
|4|Z23, Z25, Z36, Z73|74LS32|IC||
|2|Z24, Z53|74LS132|IC||
|1|Z26|74LS20|IC||
|2|Z27, Z59|74LS175|IC||
|1|Z28|74LS174|IC||
|2|Z30, Z37|74LS02|IC||
|6|Z31, Z35, Z43, Z49, Z51, Z64|74LS157|IC||
|1|Z54|74LS30|IC||
|2|Z56, Z58|74LS92|IC||
|1|Z66|74LS11|IC||
|1|Z74|74LS00|IC||
|1|Y1|10.6445MHz HC-49 Crystal|Crystal Oscillator|See Links|
|2|Z3, Z71|DIP16 Switch or Jumper Block|Switch||
|1|S1|Power Switch|Switch||
|1|S2|Reset Switch|Switch||
|3|J1,J2,J3|DIN5 180-degree Socket|Socket||
|1|K1|5V Reed Relay|Relay|Sensata-Cynergy3 S2-05P|

## Links

  [10.6445Mhz HC49U Quartz Crystal (UK)](https://www.mutant-caterpillar.co.uk/shop/product_info.php?products_id=5174)<br>
  [MJ15016 Transistor (Q4 Substitute) (UK)](https://www.cricklewoodelectronics.com/MJ15016.html)<br>
  [MJE15031 Transistor (Q6 Substitute) (UK)](https://www.cricklewoodelectronics.com/MJE15031.html)

## Credits

PCB Layout by Rob Taylor @peepouk. Schematics recreated by Ian Cudlip @grandoldian.

## Thanks

  * Chrissy @chris_jh and the rest of the Board Folk Team.
  * Adrian Black and friends for their test ROM which has been invaluable during testing. [TRS-80 Diagnostic ROM](https://github.com/misterblack1/trs80-diagnosticrom).

## Legal

As the product of this project is a replica of a proprietary product, the the author makes no claim of copyright to the schematics nor PCB layouts and releases these into the public domain, solely for the purposes of study and historical preservation.

You are free to produce PCBs based on this project's designs at your own risk and without limitation, for your own use or for sale and/or repair at a reasonable price. Attribution is appreciated. The authors are not obliged to provide support of any kind. 

Under no circumstances will the authors be held responsible or liable in any way for losses, damages or costs resulting from the use of the information and/or resources of this project. 

The resources are provided "as-is" without warranty of any kind, either expressed or implied, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose.
