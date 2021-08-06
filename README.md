# FreeRTOS-ESP32-MPU6050
FreeRTOS ESP32 MPU6050



## Table of Contents

* [Acerca del proyecto](#about-the-project)
  * [Tech Stack](#tech-stack)
  * [File Structure](#file-structure)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
  * [Configuration](#configuration)
* [Usage](#usage)
* [Results and Demo](#results-and-demo)
* [Troubleshooting](#troubleshooting)
* [Contributors](#contributors)
* [Acknowledgements and Resources](#acknowledgements-and-resources)
* [License](#license)

<!-- ABOUT THE PROJECT -->
## About The Project
* The Aim of the Project is to make a Mouse using the data fusion DMP(Digital Motion Processing) of MPU_6050 and ESP32 with Bluetooth support to actually make it    easier for the user to move pointer in any position they want.
* The Support for Right and Left click is also established using Capacitive touch pins of ESP32.
   
   ![](docs/results/Air-Mouse.png)

### Tech Stack
The Technologies used for this project are
* [FreeRTOS](https://www.freertos.org/openrtos.html)
* [ESP-IDF](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/)

### File Structure
   . 
   ├── Components              # Contiene archivos de una biblioteca específica de funciones o hardware utilizado
   │    ├──I2Cdev              # Biblioteca para comunicación I2C
   │    ├──MPU6050             # Biblioteca para sensor MPU6050
   │    ├──CMakeLists.txt      # contiene comandos para incluir el componente dado en un esp-idf
   ├── docs                    # Archivos de documentación
   │   ├── report.pdf          # Reporte de Proyecto
   │   └── results             # Carpeta que contiene capturas de pantalla, imágenes y videos de resultados
   ├── main                    # Archivos de origen (alternativamente, `lib` o` app`)
   │   ├──main.c               # Código fuente principal a ejecutar
   │   ├──kconfig.projbuild    # define las entradas del menú de configuración
   │   ├──CMakeLists.txt       # contiene comandos para incluir la biblioteca bluetooth y main.c en esp-idf
   ├── CmakeLists.txt          # contiene comandos para incluir componentes y carpeta principal mientras se ejecuta
   ├── LICENSE
   └── README.md 

 



## Getting Started

### Pre Requisites
Instalar ESP-IDF : https://github.com/espressif/esp-idf

### Instalación
Clonar el proyecto
```
https://github.com/gautam-dev-maker/Air-Mouse.git

cd FreeRTOS-ESP32-MPU
```
## Usage

Build (Verificar)
```
idf.py build
```
Flash (Cargar el programa y visualizar comunicación con puerto)
```
idf.py -p (PORT) flash monitor

```
### Configuracion

```
idf.py menuconfig
```
  
* `MPU6050 Configuracion
  * `SDA Pin No.` - Set SDA Pin No.
  * `CLK Pin No.` - Set CLK Pin No.
* The default Pin configuration used to connect MPU_6050 with ESP32 in this project is shown ![](docs/results/Esp-32andmpu6050_pin_connection.png)  ![](docs/results/Air-Mouse_diagram.png)
  
## Results and Demo
The use of Right and Left Capacitive touch pins has been demonstrated in the following videos

 [Right/left buttons](https://github.com/gautam-dev-maker/Air-Mouse/blob/master/docs/results/Right-Left%20click.mp4)
 
 ## Troubleshooting
 While Configuring for the first time if Bluetooth is not working then ,go to terminal
 
```
idf.py menuconfig
```
Then go to components/bluetooth and enable bluetooth
Press ctrl+s to save the configuration
then
```
idf.py build
```
## Contributors
* [Aman Chhaparia](https://github.com/amanchhaparia)
* [Gautam Agrawal](https://github.com/gautam-dev-maker)

## Acknowledgements and Resources
* [SRA VJTI](http://sra.vjti.info/) Eklavya 2020 
* Special thanks to [Jhoel RN](https://github.com/JhoelRN)
* https://github.com/nkolban/esp32-snippets
* https://github.com/VedantParanjape/idf-notes-sra
