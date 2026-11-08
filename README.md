# MIDI-Instrument
**MIDI Talking Drum Controller**

I'm building a MIDI controller inspired by the traditional talking drum also known as Gángan.
The goal is to detect how hard the drum is struck and use applied pressure to control the pitch.

**Components**
1. Seeed Studio XIAO ESP32-S3 - Reads the sensors and sends MIDI messages to a computer.
2. Piezoelectric sensor - Detect strikes through vibration of the strike pad.
3. Force-sensitive resistor (FSR) - Detects pressure changes to control pitch.
4. 100 kΩ and 10 kΩ resistors - Piezo current limiting ans Forms a voltage divider with the FSR.
5. Schottky diodes - protects the circuit from voltage spikes.

**Bill Of Materials**
## Bill of Materials

| Part | Description | Qty | Unit Price | Total | Vendor |
|------|-------------|----:|-----------:|------:|------|
| XIAO ESP32-S3 | MIDI Controller | 1 | $7.49 | $7.49 | https://www.seeedstudio.com/XIAO-ESP32S3-p-5627.html |
| Connector pin | Connects the sensors to the PCB | 6 | $1.16 | $6.96 | https://www.digikey.com/en/products/detail/phoenix-contact/1715022/260626 |
| 10k Resistor | Voltage divider | 10 | $0.10 | $1.00 | https://www.digikey.com/en/products/detail/stackpole-electronics-inc/RMCF0805FT10K0/1760676 |
| 100k Resistor | Piezoelectric sensor current limiting | 10 | $0.10 | $1.00 | https://www.digikey.com/en/products/detail/yageo/RE0805FRE07100KL/5923482 | 
| Schottky diode | Protects the MCU from voltage spikes | 4 | $0.57 | $2.28 | https://www.mouser.com/en/ProductDetail/Diotec-Semiconductor/SD103AW?qs=OlC7AqGiEDkHDitXxgKEcA%3D%3D |
| PCB | To place electronic components | 1 | $5.00 | $5.00 | https://cart.jlcpcb.com/quote |

![PCB Image](MIDI_Gangan_PCB.png)

**How It Works**
The piezo sensor detects strikes and determines MIDI velocity, the FSR measures pressure to control MIDI pitch bend. The XIAO ESP32-S3 processes the readings of the piezoelectric and FSR sensor and sends MIDI data over USB.

This is a learning project, so I'm figuring things out as I go and improving the design along the way!

![3D View](3D_Viewer.png)
