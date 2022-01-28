# Introduction to BIXS-V1.5: Software
The software ran on the BIXS-V1.5 avionics systems was developed by the avionics team at Space Technology Laboratory. The system was designed to meet a specific mission profile which means that this is not a general purposed flight computer of all scenarios of applications. 

## Source Code
The official source code repsentation of the software is available at the following link:
- [BIXS-V1.5](https://github.com/TKU-STL/BIXS-Arduino-V1)

## Software Design Principles
The software design principles of the BIXS computer are based on the following,
- Modular
- Reusable
- Configurable

## Software Architecture
#### Setup and Initalization
- System Initialization
- Sensors Initialization
    - IMU
    - Altimeter
#### Loop function
- Main Loop
    - Update Sensors

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
- API
- Sample Code
--------------------------
### Serial Commmunication and System Functions
#### System Communication Initialization
- Name: System Communication Initialization
- Scope: Initalization Function
- Properties: None
- Parameters: Baud Rate
- Concept: The function invoke the Arduino board to begin serial communication. The parameter is the baudrate of the serial communication which is set to 9600 by default and define by the following manner.
##### API
```C
SysCom_Init(BAUDRATE);
```
#### Sample Code
```C
#include <Arduino>

#define BAUDRATE 9600

void setup()
{
    Serial.begin(BAUDRATE);
}
```
--------------------------------
## Sensors
### Sensor Initialization 
Name: Sensor Initialization
Scope: Initalization Function
Properties: None
Parameters: None
Concept: The function is used to initialize the sensors. The function is invoked by the set-up function.

##### API
```C
Alt_Init(); //Altimeter initialization
```
```C
IMU_Init(); //IMU initialization
```
----------
### IMU
Name: IMU
Scope: Loop function
Properties: None
Parameters: None
Concept: The function is used to update the IMU data. The function is invoked by the loop function.
#### API
```C
IMU_Update();
```
#### Sample Code
```C
void loop(){
    IMU_Update();
}
```
----------
### Altitude Meter 
Name: Altitude Meter
Scope: Loop function
Properties: None
Parameters: None
Concept: The function is used to update the altitude data. The function is invoked by the loop function.
#### API
```C
Alt_Update();
```
#### Sample Code
```C
void loop(){
    Alt_Update();
}
```
----------------
### System Utilities
#### System Clock
Name: System Clock
Scope: Loop function
Properties: None
Parameters: None
Concept: The function is used to read the system clock data from the microprocessor. The function is invoked by the loop function.
#### API
```C
System_Clock();
```
#### Sample Code
```C
void loop(){
    System_Clock();
}
```