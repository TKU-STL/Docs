# Introduction to the Development Environment at Avionics Team, STL

## Software Development Toolchain and IDEs
#### Required Tools
- [gcc](https://gcc.gnu.org/)
- [Mingw](https://sourceforge.net/projects/mingw-w64/)
- [Cygwin](https://cygwin.com/install.html)
- [Git](https://git-scm.com/)
- [GitHub](https://github.com/)
- [Visual Studio Code](https://code.visualstudio.com/)
  - [GitHub for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-github)
  - [PlatformIO](https://platformio.org/)
- [Arduino IDE](https://www.arduino.cc/)
- [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)

## Hardware Development Tools
- [Fusion 360](https://www.fusion360.com/)

#### Optional Tools
- [Matlab](https://www.mathworks.com/)

## Environment Setup
#### Preliminary Check:
1. Open the command prompt in Windows or terminal in Linux and Mac OS
2. Check if the version information is identical with the information below
##### Version Check:
###### GCC
```
gcc --version
```
###### Corrected Version Information: GCC
```
gcc (GCC) 11.2.0
Copyright (C) 2021 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

###### Git
```
git --version
```
###### Corrected Version Information: Git
```
git version 2.34.1
```

###### Open OCD
```
openocd --version
```
###### Corrected Version Information: OpenOCD
```
xPack OpenOCD x86_64 Open On-Chip Debugger 0.11.0+dev (2021-12-07-17:33)
Licensed under GNU GPL v2
For bug reports, read
        http://openocd.org/doc/doxygen/bugs.html
```
The you can have a clear and correct version information by typing the commands above. Your environment set-up should be compatible with our development setting.

### IDE Installation and Configuration
#### Visual Studio Code
Visual Studio Code is a powerful IDE which is used to develop software. It is a free software which is open source and can be used by anyone. It is recommended to use Visual Studio Code to develop software. The software development in the lab massively invovlves the use of both Visual Studo Code and PlatformIO. Therefore, please ensure that you have installed the software before you start the development by the end of Novmeber 2021.

#### Arduino IDE Installation
Please use the link above to download and install the latest version of the Arduino IDE which will be the foundation of our software development process. 

#### STM32CubeIDE
The main purpose of installing STM32CubeIDE is to include the ST Link driver which is essential to the development process with ARM Cortex development board.

### Fusion 360 Installation
Please use the link above to download and install the latest version of the Fusion 360 which will be the foundation of our software development process. Also, you will be required to login into the Fusion 360 with the Autodesk account you have created.