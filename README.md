# customLocker
This project is an electrically locked box. You can safely store things that you are addicted to inside it and unlock it by reaching a particular goal. I'm going to put sweets in it and unlock the box once I've reached my daily calorie target on my smartwatch. Inside the box is a load cell that can roughly detect the amount of sweets taken out. In addition to that, there is a wireless charger, that will charge e.g. your phone while beeing busy. 
## Why I made this project
I often find myself looking at my phone a lot when I'm busy, which slows me down. Furthermore, I also want to do more sport. With the box, I can combine these things and create my first PCB, build a large 3D model, and learn many other skills.
## Pictures
### 3D-Model
<img width="549" height="395" alt="image" src="https://github.com/user-attachments/assets/8979d5e2-66a8-4a0c-b769-1451c18ad818" />

### PCB-Front
<img width="910" height="484" alt="image" src="https://github.com/user-attachments/assets/9ac14178-8ec9-47a9-bdc7-4208faa3de56" />

### PCB-Back
<img width="910" height="484" alt="image" src="https://github.com/user-attachments/assets/afbfb105-6f67-456d-b9e5-47312a5be8ed" />

## Wiring
servo motor: connect the red cable to +5v
hall effect sensor: when facing the smaller side the left once is +5v, the middle one GND and the right one signal
HX711: this board is solderd directly on the PCB in the only possible direction
power: connect the 5V of the USB-C connector with the +5V on the board and the +5V on the wireless charger, same for GND
## BOM
### Aliexpress
| Description                                                                     | Link                                                                                                                                                                                                                                                       | price in USD |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| ESP32-32D to control everything                                                 | https://de.aliexpress.com/item/4000093185394.html?spm=a2g0o.cart.0.0.b1964ae4QiPiLO&mp=1&gatewayAdapt=glo2deu                                                                                                                                              |         3,56 |
| load cell (5KG AND HX711) to detect the amount of removed items                 | https://de.aliexpress.com/item/4001274733879.html?spm=a2g0o.cart.0.0.b1964ae4QiPiLO&mp=1&gatewayAdapt=glo2deu                                                                                                                                              |          1,9 |
| 0.96 inch display (white) to display information such as left time, calorien... | https://de.aliexpress.com/item/1005006141235306.html?spm=a2g0o.cart.0.0.b1964ae4QiPiLO&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |         1,97 |
| servo motor (360°) to lock/open the box                                         | https://de.aliexpress.com/item/1005007173214082.html?spm=a2g0o.cart.0.0.b1964ae4QiPiLO&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |          1,8 |
| passive buzzer to notify the user                                               | https://de.aliexpress.com/item/1005008825917787.html?spm=a2g0o.cart.0.0.b1964ae4QiPiLO&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |         1,86 |
| keys (blue) for user inputs                                                     | https://de.aliexpress.com/item/1005004341695529.html?spm=a2g0o.cart.0.0.b1964ae4QiPiLO&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |         1,62 |
| key caps (red) for the keys                                                     | https://de.aliexpress.com/item/1005007209930123.html?spm=a2g0o.cart.0.0.64164ae4YkwdOF&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |         7,26 |
| wireless charger (b) if the smartphone or simular is in the box                 | https://de.aliexpress.com/item/1005006386722006.html?spm=a2g0o.cart.0.0.64164ae4YkwdOF&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |         5,76 |
| hall effect sensor (47E) to check if the box is open or closed                  | https://de.aliexpress.com/item/1005008647103022.html?spm=a2g0o.cart.0.0.64164ae4YkwdOF&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |          1,8 |
| magnetic tape (10mmx1mm, 1 Meter) for the hall effect sensor                    | https://de.aliexpress.com/item/1005006757451588.html?spm=a2g0o.cart.0.0.64164ae4YkwdOF&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |         2,39 |
| USB-C PCB for power                                                             | https://de.aliexpress.com/item/1005009193894473.html?spm=a2g0o.cart.0.0.64164ae4YkwdOF&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |         1,15 |
| connector pins (each color) to connect the components to the PCB                | https://de.aliexpress.com/item/1005007324368709.html?spm=a2g0o.cart.0.0.64164ae4YkwdOF&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |         1,36 |
| some cables (M-F-20pin) to connect the components as well                       | https://de.aliexpress.com/item/1005007805542492.html?spm=a2g0o.cart.0.0.64164ae4YkwdOF&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |         1,24 |
| M4x16mm screws to mount most of the components                                  | https://de.aliexpress.com/item/1005006674812661.html?spm=a2g0o.cart.0.0.64164ae4YkwdOF&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |         1,77 |
| m4 threaded inserts (OD 6mm, lenght 6mm) for the screws                         | https://de.aliexpress.com/item/1005003582355741.html?spm=a2g0o.cart.0.0.64164ae4YkwdOF&mp=1&gatewayAdapt=glo2deu                                                                                                                                           |         2,59 |
| M5x30 screws to mount the load cell and the opening mechanism of the box        | https://de.aliexpress.com/item/1005006051322108.html?spm=a2g0o.productlist.main.35.1d807847E9uYf0&algo_pvid=ca520a57-ad42-44bf-a79a-73b8be690855&pdp_ext_f=%7B%22order%22%3A%22272%22%2C%22eval%22%3A%221%22%7D&utparam-url=scene%3Asearch%7Cquery_from%3A |         3,26 |
| shipping cost to Germany                                                        |                                                                                                                                                                                                                                                            |         6,27 |
| total price for ALIEXPRESS                                                      |                                                                                                                                                                                                                                                            |        47,56 |
### local building center
| Description                                                                                                                             | price in €  |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|
| 2 pices M4 DIN9021 to spread the pressure over the box                                                                                  | 2X0,24=0,48 |
| 2 pices M5 DIN9021 to spread the pressure over the box                                                                                  | 2x0,29=0,58 |
| 2 pieces M5 domed cap nut                                                                                                               | 2x0,49=0,98 |
| total price in €                                                                                                                        | 2,04€       |
| total price in $ (7/17/2025 at 4:44pm under: https://www.visa.de/support/verbraucher/visa-reiseservices/exchange-rate-calculator.html)  | 2,39$       |

### PCB from jlcpcp
| Description                                            | price in $ |
|--------------------------------------------------------|------------|
| 2 pices M4 DIN9021 to spread the pressure over the box |          4 |
| shipping cost                                          |        3,3 |
| total                                                  |        7,3 |

### total cost
| Description           | price in $                                                                 |
|-----------------------|----------------------------------------------------------------------------|
| aliexpress            |                                                                      47,56 |
| local building center |                                                                       2,39 |
| PCB                   |                                                                        7,3 |
| 3D-Filament           | nothing - I have to use Printing Legion because I have no 3D-Printer yet 😥 |
| total                 |                                                                      **57,25** |
