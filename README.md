# CrowPi3


### Description
CrowPi3

![crowpi_3_1_1](https://github.com/user-attachments/assets/37643e4a-080d-4c32-a5e9-77dc2055f275)


CrowPi 3 is constructed around the newly released Raspberry Pi 5 development board by the Raspberry Pi Foundation. It serves as a powerful tool that integrates learning, design, and programming, offering a new learning platform for coding enthusiasts and developers. CrowPi 3 is compatible with various development boards including Pi 5, Arduino Nano, micro:bit, and Pico series. It integrates a variety of sensors and is equipped with a display, camera, and microphone, facilitating the construction of an AI smart hardware platform. Additionally, it offers abundant course resources, making CrowPi 3 an ideal choice for learning programming.

### Website
https://www.elecrow.com/crowpi-3-al-learning-and-development-station.html

### Forums
https://forum.elecrow.com/categories/hardware

<br>

# Official CrowPi3 system image
The CrowPi3 system image is available [HERE](https://drive.google.com/drive/folders/1CkRyCbM1ektOu4h1XP0nV6II2hTAw1Fl?usp=sharing).  

# Initial Setup
1. ***Note:** For more details on the Raspberry Pi Setup Wizard, see [HERE](https://www.raspberrypi.org/blog/raspbian-update-june-2018/).*  

# Frequently Asked Questions
Solutions to common problems encountered with CrowPi3 can be found [HERE](./faq/TOC-FAQ.md#frequently-asked-questions).  





# Caution
Please strictly use 5V5A adapter that supports PD protocol for power supply, otherwise the device will not be driven or burned out.

<br>

# Helpful resources that could aid with your programming
- [Raspberry Pi offical website](https://www.raspberrypi.org/help/)  
- [Pinout! - The Raspberry Pi GPIO pinout guide.](https://pinout.xyz/)  
***Note:** You may easily display the hardware features of your particular Raspberry Pi board using the command `pinout` in a terminal.*  

<br>

# Information of CrowPi3 on-board modules

| Function               | connector       | quantities | reference voltage | raspberry pi(3.3V)（Function name for IO） | Arduino Nano v3(5V)          | micro:bit(3.3V)     | PICO(3.3V)          |
| ---------------------- | --------------- | ---------- | ----------------- | ------------------------------------------ | ---------------------------- | ------------------- | ------------------- |
| Accelerometer&Gyro     | I2C             | 1          | 3.3V              | SCL1,SDA1                                  | A5,SCL;A4,SDA                | P19,SCL;P20,SDA     | P17,SCL;P16,SDA     |
| 1602 LCD               | I2C             | 1          | 5V                |                                            |                              |                     |                     |
| Digital display        | I2C             | 1          | 5V                |                                            |                              |                     |                     |
| LIGHT SENSOR           | I2C             | 1          | 3.3V              |                                            |                              |                     |                     |
| EEPROM                 | I2C             | 1          | 5V                |                                            |                              |                     |                     |
| Temperature & Humidity | I2C             | 1          | 3.3V              |                                            |                              |                     |                     |
| IIC                    | I2C             | 1          | 5V                |                                            |                              |                     |                     |
| Encoder                | I2C             | 2          | 5V                |                                            |                              |                     |                     |
| HALL SENSOR            | I2C/GPIO        | 1          | 5V                | IO26                                       | P21                          |                     |                     |
| STEP MOTOR             | I2C/GPIO        | 4          | 5V                | IO21,IO22,IO23,IO06(STEP1,2,3,4)           | P22,P26,P27,P28(STEP1,2,3,4) |                     |                     |
| Vibration sensor       | I2C/GPIO        | 1          | 5V                | IO02                                       | P10                          |                     |                     |
| LED*6                  | IIC-PR2040,IO10 | 6          | 5V                | SCL1,SDA1                                  | P1                           | P17,SCL;P16,SDA     |                     |
| 8*8RGB(RGB_LED)        | IIC-PR2040,IO6  | 1          | 5V                | P12                                        |                              |                     |                     |
| ROCKER                 | SPI-ADC         | 2          | 3.3V              | CE1,SCLK,MISO,MOSI                         | A6,A7                        | P13,P14,P15,P16(CS) | P14,P12,P15,P13(CS) |
| custom_key*4           | SPI-ADC         | 1          | 3.3V              | D13,D12,D11,D10(CS)                        |                              |                     |                     |
| Voltage Sensor         | SPI-ADC         | 1          | 3.3V              |                                            |                              |                     |                     |
| RFID                   | SPI             | 1          | 3.3V              | CE0,SCLK,MISO,MOSI                         | D13,D12,D11,D9(CS)           | P13,P14,P15,P4(CS)  | P14,P12,P15,P11(CS) |
| SERVO                  | GPIO            | 1          | 5V                | IO24                                       | D3                           | P10                 | P8                  |
| Touch Sensor           | GPIO            | 1          | 3.3V              | IO0                                        | A0                           | P3                  | P20                 |
| Ultrasonic Sensor      | GPIO            | 2          | 3.3V              | IO25(EHCO),IO27(TRIG)                      | A1(TRIG),D5(EHCO)            | P6(TRIG),P11(EHCO)  | P3(TRIG),P9(EHCO)   |
| Flame                  | GPIO            | 1          | 3.3V              | IO07                                       | A2                           | P9                  | P7                  |
| Relay                  | GPIO            | 1          | 5V                | IO29                                       | A3                           | P2                  | P18                 |
| Tilt sensor            | GPIO            | 1          | 3.3V              | IO03                                       | D7                           | P7                  | P4                  |
| Motion sensor          | GPIO            | 1          | 3.3V              | IO04                                       | D4                           | P5                  | P6                  |
| SOUND_SENSOR           | GPIO            | 1          | 3.3V              | IO05                                       | D8                           | NC                  | P5                  |
| BUZZER                 | GPIO            | 1          | 5V                | IO01                                       | D6                           | P0                  | P19                 |
| IR Remote Sensor       | GPIO            | 1          | 3.3V              | IO28                                       | D2                           | P8                  | P2                  |
| uart                   | uart            | 1          | 3.3V              | TXD, RXD                                   | D1,TX D0,RX                  | NC                  | P0,TX;P1;RX         |
| burn-in port           | USB-UART        | 1          | 5V                | TXD, RXD                                   | D1,TX D0,RX                  | NC                  |                     |


