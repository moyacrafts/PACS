# PACS (Plug And Create Shield)
![PACS header image](https://raw.githubusercontent.com/moyacrafts/PACS/main/readme_images/PACS_header_image.jpg)

These are the building instructions for a low-cost extension module designed for ESP32 development boards. The module simplifies the process of connecting inputs and outputs to a board, while also enabling user interaction through push buttons and displaying information via low-power OLED display.

## Overview and parts list
![PACS components overview](https://raw.githubusercontent.com/moyacrafts/PACS/main/readme_images/PACS_parts_overview.jpg)

| # | Name |  Description |
| ------------ | ------------ | ------------ |
| 1+2 | Tactile switch (SMD) | RACON 12 S, THT, 12x12 mm |
| 3 | OLED-Display SSD1306 | I²C OLED Display 0,96”, 128x64 px, SSD1306 controller, I²C  connection, 5V |
| 4+5 | Socket strip | 30 pins, double rows, pin length 3.5mm, max. 5A |
| 6 | Stripboard 70x50 mm | Epoxyd FR4 PCB with double-sided dot matrix and solder resist, grid spacing: 2.54 mm |
| 7 | Jumper wire | Wire for connections (ø 0,5 mm) |

## Schematics and instructions
![PACS component placement on the front side](https://raw.githubusercontent.com/moyacrafts/PACS/main/readme_images/PACS_front_components.png)
![PACS component placement on the back side](https://raw.githubusercontent.com/moyacrafts/PACS/main/readme_images/PACS_back_connections.png)

| Name | Soldering connections |  Wire connections |
| ------------ | ------------ | ------------ |
| Tactile switch 1 | **B2** (OUT)	**D2** (GND)<br>**B6** (OUT)	**D6** (GND) | **B6** -> **L9**<br>**D6** -> **I6** |
| Tactile switch 2 | **G2** (OUT)	**I2** (GND)<br>**G6** (OUT)	**I6** (GND) | **G6** -> **L10**<br>**I2** -> **W4** |
| OLED display | **D17** (OUT)	**E17** (VCC)<br>**F17** (SCL)	**G17** (SDA) | **D17** -> **I2**<br>**E17** -> **L3**<br>**F17** -> **W16**<br>**G17** -> **W13** |
| Socket strip 1 | **L3** to **L17**<br>**M3** to **M17** | see above |
| Socket strip 2 | **W3** to **W17**<br>**X3** to **X17** | see above |

## Supported hardware
The module works with 30-pin variants of development boards that are based on the popular [ESP32-DevKitC](https://www.espressif.com/en/products/devkits/esp32-devkitc/overview) platform.

## Give your PACS a cover
![PACS case parts overview](https://raw.githubusercontent.com/moyacrafts/PACS/main/readme_images/PACS_case_parts.jpg)
Vector images for laser cutting a protective case out of 3 mm High-Density-Fiberboard (HDF) can be found inside the [case images folder](https://github.com/moyacrafts/PACS/tree/main/case_images_vector).

## Helpful resources
HACKADAY  
*Resources for hardware hacking*  
https://hackaday.io/discover

WOKWI  
*Simulate IOT projects in your browser (/w ESP32 support)*  
https://www.wokwi.com

The ESP Journal  
*Best Practices, Articles, and Notes from Espressif*  
https://blog.espressif.com

How To Solder – For DIY Guitar Pedals, Synth, and Other Hobby Electronics  
*Mark A. Stratman (MAS Effects)*  
https://masfx.io/how-to-solder.pdf

Soldering Electronic Connections  
*NASA Technical Standards Coordinator, Washington DC*  
https://nepp.nasa.gov/docuploads/06AA01BA-FC7E-4094-AE829CE371A7B05D/NASA-STD-8739.3.pdf

