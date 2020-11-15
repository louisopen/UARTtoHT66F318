## ※UART with HT66F318 applications
Using the UART port(Same RS-485 port) access GPIO port, EEPROM(64bytes), ADC(8ch 12bits), PWM output(10bit), Capture, OLED display... via HT66F318 UART port.<br>
專案利用PC or Raspberry Pi or Arduino 軟件主控下達UART通訊指令(Same RS-485 port)<br>
以存取HT66F318 GPIO port, EEPROM(64bytes), ADC(8ch 12bits), PWM output(10bit), Capture, OLED display...<br>

UART port baudrate setting 9600,N,8,1 ;Protocol format refer RS-485 Modbus & CRC-16 <br>
通訊協議格式參照RS-485通訊協議格式(Modbus & CRC-16).<br>
在MCU資源不足或是應用裝置缺乏時, 即可以自己製造簡單的應用裝置, Host即可透過UART來控制這個裝置.<br>
Project Option: HXT; 可選項還有(小心使用)HXT,HIRC8M,HIRC12M,HIRC16M,LXT,LIRC<br>

HT66F318 28ssop with HT-IDE3000 V8.02 & e-Link & e-WriterPro<br>
[HT66F318 Document](https://www.holtek.com.tw/search?key=ht66F318)<br>
[IDE3000 & ICE & Writer](https://www.holtek.com.tw/ice)<br>

### Relevant information
* HT-IDE3000 V8.02
![Image](HT-IDE3000_version.jpg)
* HOLTEK C Compiler V3/Assembly
![Image](ProjectCompiler.jpg)
* HT66F318 Config, used 8Mhz X'tal external, VDD/VDDA binding
![Image](ProjectOption1.jpg)
![Image](ProjectOption2.jpg)
![Image](ProjectOption3.jpg)
![Image](ProjectOption4.jpg)
* HT66F318 28ssop Schematic Diagram
![Image](CircuitDiagram.jpg)

### How to test or used
利用PC通訊軟件做為主動工具, 協議(9600,n,8,1), 格式比照RS-485格式(PC指令CRC用 A0 0A代替, MCU反饋的為CRC-16)

* For Example: 
* UART Formate(Get from MCU): 44 02 00 00 00 00 A0 0A   #Reture test
MCU return: 44 02 04 55 AA 55 AA CRC CRC
