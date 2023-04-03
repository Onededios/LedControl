# LedControl
This is just my tutorial of controlling an array of leds connected to an ESP8266. It creates and hosts a webpage accesible to all the hosts of the network to update the state of the leds. 

## License

This repository is licensed under the Creative Commons Attribution-ShareAlike (CC-BY-SA) license. This means that you are free to use, share, and modify the code and any derivative works, as long as you give credit to the original creator and share any derivative works under the same license. 

### Attribution Requirements

If you use this code in your own work, please provide a clear attribution to the original creator and a link back to this repository.

### Share-Alike Requirements

If you create derivative works based on this code, you must share them under the same CC-BY-SA license.

### Questions

If you have any questions about this license or would like to discuss using this code in a different way, please contact me at "joel10olor@gmail.com". 

## Starting with
### Power Source

<img src="https://admin.minebizs.com/Attachments/Product/TNK-SWITCHING-POWER-SUPPLY-(12V-SERIES)-ADPATN-S1230A-1190325152909335.png" width="200"/>

#### Where to buy
<a target="_blank" href="https://www.amazon.es/dp/B0BWYX325K?ref_=cm_sw_r_apan_dp_TH1KMMPY642XRWSNBFZW&_encoding=UTF8&tag=onededios-21&linkCode=ur2&linkId=d8503585f5c1ffee0d05dd50e375de36&camp=3638&creative=24630">Amazon</a> | 28€/u

<a target="_blank" href="https://www.amazon.es/dp/B07BLR16PB?ref_=cm_sw_r_apan_dp_AT95E9B3V2G6XXBZGVRQ&_encoding=UTF8&tag=onededios-21&linkCode=ur2&linkId=39fa3b91a6287f4bd06f8989f1840007&camp=3638&creative=24630">Amazon</a> | 29€/u

<a target="_blank" href="https://www.amazon.es/dp/B09R7SYWZ9?ref_=cm_sw_r_apan_dp_6V7FFNX47CGBFVG8ZDAW&_encoding=UTF8&tag=onededios-21&linkCode=ur2&linkId=cafabe1993cfba16c3a77d67d08e0722&camp=3638&creative=24630">Amazon</a> | 23€/u

### Addressable led strip (WS2812B) 12V
I've decided to use the **WS2812B led strip** because is a type of digitally **addressable LED strip** that allows **individual control over each LED** on the strip. Each LED on the strip has a built-in controller chip that communicates with other LEDs in the strip, enabling the creation of complex patterns and animations. And also because it **only requires a single data line to control all of the LEDs** on the strip.

<img src="https://images.squarespace-cdn.com/content/v1/5d8eb8fa7726ea72f382e973/1571461817586-7GZSKNFZDS85XK1VSBCJ/density.png?format=1000w" alt="WS2812B" width="200"/>

#### Where to buy
[AliExpress](https://es.aliexpress.com/item/1005001278846135.html?spm=a2g0o.order_list.order_list_main.62.78bf194d5pnRWf&gatewayAdapt=glo2esp) | 10.17€/m

### Led Profile
An aluminum profile is specifically designed to house LED strips, providing a stylish and discreet way to install lights.
The aluminum profile for LED needs a cover (which can be transparent or milky diffused), two mounting clips, and two end caps (one with a hole for the cable and one without a hole).

#### Where to buy
[Aliexpress](https://es.aliexpress.com/item/32484961277.html?spm=a2g0o.order_list.order_list_main.638.78bf194d5pnRWf&gatewayAdapt=glo2esp) | 12.93€/m

### Controller (NodeMcu ESP8266)
The NodeMCU ESP8266 is a popular development board that is based on the ESP8266 Wi-Fi module. The ESP8266 module is a low-cost, low-power system-on-a-chip (SoC) that is commonly used in Internet of Things (IoT) applications. The NodeMCU ESP8266 development board features an integrated USB-to-serial converter, which enables the board to be programmed and powered directly from a computer's USB port. The board also includes a built-in Wi-Fi module, which allows it to connect to a wireless network and communicate with other devices.

<img src="https://imgs.search.brave.com/HzGJv5RN5ZTnNSzgv7GbQczeMrAcamxSD925WouVCUo/rs:fit:578:406:1/g:ce/aHR0cDovLzEuYnAu/YmxvZ3Nwb3QuY29t/Ly1mMHBic0VQZG9o/Yy9WbDl2Yk5JNzM3/SS9BQUFBQUFBQUVK/MC9BQ21MNU9XTUdq/RS9zMTYwMC9Ob2Rl/TUNVX0xvTGluLnBu/Zw" width="200"/>

#### Where to buy
[AliExpress](shorturl.at/dgGKZ) | 2.5€/u

<a target="_blank" href="https://www.amazon.es/HiLetgo-Internet-desarrollo-inal%25C3%25A1mbrico-micropython/dp/B0791FJB62/ref=sr_1_1_sspa?keywords=nodemcu+esp8266&amp;sr=8-1-spons&amp;sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&amp;psc=1&_encoding=UTF8&tag=onededios-21&linkCode=ur2&linkId=95900f73eb597d9a4a9721d7cbfec988&camp=3638&creative=24630">Amazon</a> | 7.5€/u

<a target="_blank" href="https://www.amazon.es/dp/B0754LZ73Z?ref_=cm_sw_r_apan_dp_GFT52ZA0G4MJTSDPYTT5&_encoding=UTF8&tag=onededios-21&linkCode=ur2&linkId=0ee9274601a543affd5f34642287dac2&camp=3638&creative=24630">Amazon</a> | 4.6€/u

<a target="_blank" href="https://www.amazon.es/dp/B06Y1ZPNMS?ref_=cm_sw_r_apan_dp_C62SAGW6J84KBE0MAXH4&_encoding=UTF8&tag=onededios-21&linkCode=ur2&linkId=26af80fd2d17c6bd0aa13b1121a90191&camp=3638&creative=24630">Amazon</a> | 10€/u

### Micro USB Cord
NodeMCU comes with a Micro USB port to connect to the power, so we'll need to connect it to the computer and upload the code from the IDE.
**You must ensure that the chosen cord has data-transfering wire.**

#### Where to buy
[Aliexpress](https://es.aliexpress.com/item/1005002389306219.html?spm=a2g0o.order_list.order_list_main.5.78bf194d5pnRWf&gatewayAdapt=glo2esp) | 1€/u

### IDE (Arduino)
The Arduino IDE (Integrated Development Environment) is a software tool used for programming and developing applications for Arduino microcontrollers. It is a simple and user-friendly platform that enables developers to write, compile, and upload code to Arduino boards.

The Arduino IDE includes a text editor, a compiler, and a microcontroller programming environment, making it a one-stop-shop for developers who want to create projects with Arduino. It supports a simplified version of the C++ programming language and provides a range of built-in functions and libraries, making it easy for developers to get started with coding for Arduino.

#### Download
You can go to the download page directly from this [link](https://www.arduino.cc/en/software)
