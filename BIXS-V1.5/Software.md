# Introduction to BIXS-V1.5: Software
The software ran on the BIXS-V1.5 avionics systems was developed by the avionics team at Space Technology Laboratory. The system was designed to meet a specific mission profile which means that this is not a general purposed flight computer of all scenarios of applications. 

## Source Code
The official source code repsentation of the software is available at the following link:
- [BIXS-V1.5](https://github.com/TKU-STL/BIXS-Arduino-V1)

## Software Design Principles
The software design principles of the BIXS computer are based on the following,

## Software Architecture

### Setup and Initalization
- System Initialization
- Sensors Initialization
    - IMU
    - Altimeter

### Loop and Update
- Alt_Update()
- IMU_Update()

## Directory Structure
- Root
    - .pio //Kernel and Firmware Build
    - .vscode //Environment Configuration in JSON format
    - include // Where you include external header file
    - lib //Where you include external dependencies
    - src //Where you put your source code
    - test //Unit Test
    - platformio.ini //Initalization File

## Development Environments
The development of the software was done in the following environments,
- Platform IO
- Arduino IDE
- GCC
- GitHub
- Git
To find out more about the installation process, please refer to the following link,
- [Environment Setup](../Development-Environment.md)

## API Documentation
The API documentation enables engineers and manager to better understand the sources code in the systems. To better the understanding of the documentation, the software engineer design the API documentation as the following manner.
- Introduction to the API
    - Name
    - Scope
    - Properties
    - Parameters
- Concepts
- Sample Code
### Serial Commmunication and System Functions
##### System Communication Initialization
```C
SysCom_Init(BAUDRATE);
```

The function invoke the Arduino board to begin serial communication. The parameter is the baudrate of the serial communication which is set to 9600 by default and define by the following manner.
```C
#define BAUDRATE 9600
```
### Sensors
#### Sensor Initialization
This function is used to initialize the sensors. The function is invoked by the set-up function. 
```C
Alt_Init();
```
```C
IMU_Init();
```
#### IMU
This function is used to read the IMU data. The function is invoked by the loop function.
```C
IMU_Update();
```

#### Altitude Meter 
```C
Alt_Update();
```
The function is used to read the altitude data from the BMP180 sensor. The function is invoked by the loop function.

### System Utilities
##### System Clock
```C
System_Clock();
```
The function is used to get the system clock. The function is invoked by the main function. The system clock is vital to understand the time sequence of the performance.