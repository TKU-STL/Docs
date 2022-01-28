# Introduction to BIXS-V1.5: Software
The software ran on the BIXS-V1.5 avionics systems was developed by the avionics team at Space Technology Laboratory. The system was designed to meet a specific mission profile which means that this is not a general purposed flight computer of all scenarios of applications. 

## Source Code
The official source code repsentation of the software is available at the following link:
- [BIXS-V1.5](https://github.com/TKU-STL/BIXS-Arduino-V1)

## Software Design Principles
The software design principles of the BIXS computer are based on the following,

## Software Architecture
- Components
    - 

## Directory Structure
- Root
    - .pio //Kernel and Firmware Build
    - .vscode //Environment Configuration in JSON format
    - include // Where you include external header file
    - lib //Where you include external dependencies
    - src //Where you put your source code
    - test //Unit Test
    - platformio.ini //Initalization File

## Development Methodology

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

### Sensors
#### IMU
#### Altitude Meter 