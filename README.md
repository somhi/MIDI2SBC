# MIDI I2S SBC Pmod Edge Interface v0.1

## **Features**

* MIDI synthesizer: [mt32-pi](https://github.com/dwhinham/mt32-pi) with display, 2 buttons and rotative encoder 
  * Play MIDI sounds from FPGA core through RPi jack output or through I2S DAC
  * Send mt32-pi I2S audio back to FPGA for mixing with other core audio and play it through I2S DAC
* DAC I2S: footprints for UDA 1334A or PCM5102A
  * Play I2S audio sent from your FPGA (connected to Edge or Pmod 3)
  * Play I2S audio from Raspberry mt32-Pi (bypass jumpers)
* SBC (Raspberry Pi connector) or Micro-controller pmod interface 
  * Interface to FPGAs through Edge (see models below) or Pmod 3 connectors
  * Interface signals: SPI and UART  
  * Footprint for Raspberry Pi model B 40 pin connector. Other SBCs or microcontrollers can be interfaced through adapters (e.g. MAix BiT and STM32 are available in [Atlas FPGA project](https://github.com/atlasfpga))
  * SBC or uC can be used as a multicore device for the FPGA
* UART header connected to Raspberry Pi and FPGA (Rx, Tx)
* Power header from raspberry Pi (5 V, 3.3 V)


**Additional features for Edge connector ** (compatible platforms ZXDOS+, GomaDOS+ & NeptUNO)

* PMODs 1 & 2 for double Pmod peripherals like Hyperram, VGA, HDMI, .... 
  * 5V power supply pin between Pmods for compatibility with Colorlight i5 addons
* PMOD 3 can be used also for peripherals (jumper connects power on pins 6,12)



**Additional notes**

* DAC I2S 
  * Only one DAC (either UDA 1334A or PCM5102A) is intended to be used at the same time
  * DAC voltage input selection jumpers (from Edge, other FPGA or Raspberry Pi)

* SPI communication between Raspberry Pi and FPGA
  * SPI 0 or SPI 1 (selection by jumpers)
  * SPI 1 CE2 signal only available if UART Tx is not used (jumper selection)



