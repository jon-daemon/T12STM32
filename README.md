# Soldering station pcb for T12 iron  
### Designed to be used with [Alexander's](https://www.hackster.io/sfrwmaker) firmware  
### Original project can be found [here](https://www.hackster.io/sfrwmaker/soldering-iron-controller-for-hakko-t12-tips-on-stm32-c50ccc)
___
### Here are some notes to help you build the pcb

* The pcb was designed to use a MP1584 step-down converter. I suggest you to use a pre-made MP1584 module and solder it on IN+,IN-,OUT+ through holes. If you solder a pre-made pcb do not solder anything on this area (It's actually the same circuit with the MP1584 module).  
![](https://files.hackermagnet.com/T12-voltage-adjust-components.png)  

* You should adjust the voltage on MP1584 before soldering the module on board, or before soldering any of the components that use 3.3V (STM32, opamp, lcd, eeprom).  
If for some reason you need to adjust the voltage later you must cut the 3.3V trace where you see the 'X' in the picture below before adjusting it, to avoid damaging the ICs.
![](https://files.hackermagnet.com/T12-voltage-trace.png)

* The LCD pins should be in that order 1>GND, 2>VDD, 3>SCK, 4>SDA

* This image shows the programming pins layout
![](https://files.hackermagnet.com/T12-programming-pins.png)

* D2 and D5 are the same component (18V zener) in different packages. Solder only one depending on what is available to you. D2 is a SOT23 (e.g. BZX84C18) and D5 is a miniELF.

* R25 and R27 are not resistors, they are capacitors 22nF. It's an annotation mistake.

* Build the firmware according to Alexander's instructions but keep in mind that you should invert the logic of the buzzer and the encoder (there are instructions in the comments).  

___
### Complete interactive [BOM](http://files.hackermagnet.com/T12-ibom.html) and [Schematic](http://files.hackermagnet.com/T12-schematic.pdf)
___
### [Download gerbers files](https://hackermagnet.com/download-t12-soldering-station-gerber-files/)
