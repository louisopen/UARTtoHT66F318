### UART with HT66F318 applications

Using the UART port(Same RS-485 driver) access to HT66F318 GPIO port, EEPROM(64bytes), ADC(8ch 12bits), 
PWM output(10bit), Capture, OLED display...
�M�קQ��PC or Raspberry Pi or Arduino �n��D���U�FUART�q�T���O(Same RS-485 driver)
�H�s��HT66F318 GPIO port, EEPROM(64bytes), ADC(8ch 12bits), PWM output(10bit), Capture, OLED display...

UART port baudrate setting 9600,N,8,1 ;Protocol format link as RS-485 Modbus & CRC-16 
�q�T��ĳ�榡�ѷ�RS-485�q�T��ĳ�榡(Modbus & CRC-16).

�bMCU�귽�����άO���θ˸m�ʥF��, �Y�i�H�s�y�ۤv�����θ˸m, Host�Y�i�z�LUART�ӱ���o�Ӹ˸m.

#### relevant information:

Tools: HT66F318 28ssop with HT-IDE3000 V8.02 & e-Link

Project Option: HXT (hi speed HXT);�i�ﶵHXT,HIRC8M,HIRC12M,HIRC16M,LXT,LIRC

* HT-IDE3000 V8.02
![Image](HT-IDE3000_version.jpg)
* HOLTEK C Compiler V3/Assembly
![Image](ProjectCompiler.jpg)
* HT66F318 Config, used 8Mhz X'tal external, VDD/VDDA binding
![Image](ProjectOption1.jpg)
![Image](ProjectOption2.jpg)
![Image](ProjectOption3.jpg)
![Image](ProjectOption4.jpg)
* HT66F318 28ssop Diagram
![Image](CircuitDiagram.jpg)


#### How to test or used:

�Q��PC�q�T�n�󰵬��D�ʤu��, ��ĳ(9600,n,8,1), �榡���RS-485�榡(PC���OCRC�� A0 0A�N��, MCU���X����CRC-16)
* For Example: 
* UART Formate(Get from MCU): 44 02 00 00 00 00 A0 0A   #Reture test
MCU return: 44 02 04 55 AA 55 AA CRC CRC
