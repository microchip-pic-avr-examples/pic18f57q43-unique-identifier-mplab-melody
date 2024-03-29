[![MCHP](images/microchip.png)](https://www.microchip.com)

# Reading the Microchip Unique Identifier (MUI) on the PIC18-Q43 Family of Devices

This code example uses the memory driver generated with the MPLAB® Code Configurator (MCC) Melody library to read the MUI number from the microcontroller's memory. The MUI is a unique number that is encoded individually during final manufacturing on every device. This allows for unique device tracking by the application manufacturer.

## Related Documentation

  - [PIC18F-Q43 Family Product Page](https://www.microchip.com/en-us/products/microcontrollers-and-microprocessors/8-bit-mcus/pic-mcus/pic18-q43?utm_source=GitHub&utm_medium=TextLink&utm_campaign=MCU8_MMTCha_MPAE_Examples&utm_content=pic18f57q43-unique-identifier-mplab-melody-github)
  - [PIC18F57Q43 Data Sheet](https://ww1.microchip.com/downloads/en/DeviceDoc/PIC18F27-47-57Q43-Data-Sheet-40002147F.pdf?utm_source=GitHub&utm_medium=TextLink&utm_campaign=MCU8_MMTCha_MPAE_Examples&utm_content=pic18f57q43-unique-identifier-mplab-melody-github)
  - [PIC18F57Q43 Curiosity Nano User Guide](https://ww1.microchip.com/downloads/en/DeviceDoc/PIC18F57Q43-Curiosity-Nano-HW-UserGuide-DS40002186B.pdf?utm_source=GitHub&utm_medium=TextLink&utm_campaign=MCU8_MMTCha_MPAE_Examples&utm_content=pic18f57q43-unique-identifier-mplab-melody-github)

## Software Used

- [MPLAB® X IDE 6.10.0](https://www.microchip.com/en-us/development-tools-tools-and-software/mplab-x-ide?utm_source=GitHub&utm_medium=TextLink&utm_campaign=MCU8_MMTCha_MPAE_Examples&utm_content=pic18f57q43-unique-identifier-mplab-melody-github) or newer

- [MPLAB® XC8 2.41](https://www.microchip.com/en-us/development-tools-tools-and-software/mplab-xc-compilers?utm_source=GitHub&utm_medium=TextLink&utm_campaign=MCU8_MMTCha_MPAE_Examples&utm_content=pic18f57q43-unique-identifier-mplab-melody-github) or newer compiler

- [PIC18F-Q_DFP V1.17.379](https://packs.download.microchip.com/) or newer

- [MPLAB® Code Configurator (MCC) 5.3.7](https://www.microchip.com/mplab/mplab-code-configurator) or newer

- MPLAB® Melody Library 2.6.1 or newer ([microchip.com/mplab/mplab-code-configurator](https://www.microchip.com/en-us/tools-resources/configure/mplab-code-configurator/melody))

## Hardware Used

- PIC18F57Q43 Curiosity Nano ([DM164150](https://www.microchip.com/en-us/development-tool/DM164150))

## Setup

The PIC18F57Q43 Curiosity Nano Development board is used as the test platform. This board has an onboard programmer/debugger and is equipped with a virtual serial port.

The following configurations must be made for this project:

| Pin | Configuration            |
| :-: | :-----------------------:|
| RF0 | UART TX pin             |
| RF3 | Digital output for LED   |
| RB4 | Digital input for Switch |


## MCC Settings:

This application uses the Memory and the UART drivers. The following screenshots illustrate the settings from MCC.

### Memory Module

<img src="images/mcc_EEPROM__config.png" width = "600"><br>


<img src="images/mcc_NVM_config.png" width = "600"><br>

### UART Module
<img src="images/mcc_UART1_config.png" width = "600"><br>
<img src="images/mcc_UART1PLIB_config.png" width = "600"><br>


## Operation

When the Curiosity Nano board is programmed, the firmware reads the MUI and stores it in an array. Every time the push button (SW0) is pressed, the MUI is printed on the UART which can be observed on the MPLAB Data Visualizer. The LED state toggles every time the push button is pressed for visual confirmation.

<img src="images/Terminal.png" width = "800"><br>


## Summary

This project demonstrates how to read the MUI from the device's memory and display it using the UART module and the MPLAB Data Visualizer. The MUI is helpful with uniquely identifying the device in a given application.
