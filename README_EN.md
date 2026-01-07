# AgentDevice - Smart Terminal Open Source Project

[English](README_EN.md) | [中文](README.md)

## Project Introduction

AgentDevice is a complete smart terminal project that integrates hardware and software design with cloud-edge computing to achieve various intelligent application scenarios. It can serve as a low-cost voice assistant, an affordable educational robot, a home monitoring device that recognizes actions locally and alerts only in case of anomalies, and an industrial equipment maintenance assistant.

The project covers the complete chain from hardware design to software implementation, including custom integrated circuits, PCB layout, 3D printed enclosures, and embedded software development based on ESP-IDF.

## Key Features

### Hardware Design
- **Custom Integrated Circuits**: Independently designed circuit boards supporting multiple sensors and interfaces
- **PCB Design**: Complete Gerber files ready for PCB manufacturing
- **3D Printed Enclosure**: Modular enclosure design including buttons, screen covers, and other components

### Software Functions
- **Button Camera**: Supports button-triggered camera functionality
- **Expression Settings**: Supports custom emoticon display with multiple expression switching
- **Battery Display**: Real-time monitoring and display of battery level
- **Volume Control**: Volume up/down button control
- **IoT Device Control**: Integrated IoT functionality supporting sensors like temperature and humidity
- **MCP Device Control**: Control external devices via MCP protocol

## Project Structure

```
AgentDevice/
├── LICENSE                 # Apache 2.0 License
├── README.md              # Project Documentation (Chinese)
├── README_EN.md           # Project Documentation (English)
└── docs/               # docs Smart Terminal Files
    ├── 3D外壳文件/        # 3D Printed STL Files
    ├── 原理图及PCB文件/   # Schematic and PCB Gerber Files
    ├── 小e-按键拍照/     # Button Camera Implementation
    ├── 小e-表情设置/     # Expression Settings Implementation
    ├── 小e-电量显示/     # Battery Display Implementation
    ├── 小e-音量加减/     # Volume Control Implementation
    ├── 小e-iot控制设备/  # IoT Device Control Implementation
    └── 小e-mcp控制设备/  # MCP Device Control Implementation
```

## Hardware Design Details

### Circuit Schematic
The project includes complete circuit schematic PDF files located at `docs/原理图及PCB文件/原理图.pdf`.

**Schematic Preview:**
[View Full Schematic](docs/原理图及PCB文件/原理图.pdf)

### PCB Design
PCB Gerber files are located in the `docs/原理图及PCB文件/Gerber_PCB/` directory, including:
- Top and bottom copper layers
- Silkscreen layers
- Solder mask layers
- Drill files
- Other manufacturing files

**PCB Ordering Notes:**
[PCB Ordering Instructions](docs/原理图及PCB文件/Gerber_PCB/PCB下单必读.txt)

### 3D Enclosure
3D printing files are located in the `docs/3D外壳文件/` directory, including:
- Main enclosure (外壳1.STL)
- Button components (按键.STL, 按键2.STL, 按键3.STL, 按键4.STL)
- Screen cover (装配体2 - 屏幕盖-1.STL)
- Cover plate (装配体2 - 盖-1.STL)

**3D Enclosure Renderings:**
![Main Enclosure](docs/3D外壳文件/外壳1.jpg)
![Button Components](docs/3D外壳文件/按键.jpg)
![Screen Cover](docs/3D外壳文件/装配体2%20-%20屏幕盖-1.jpg)
![Cover Plate](docs/3D外壳文件/装配体2%20-%20盖-1.jpg)

## Software Function Implementation

### Button Camera Function
Supports button-triggered camera with integrated camera module. Implementation steps include:
1. Configure camera pins
2. Add camera header files
3. Initialize button camera monitor
4. Implement camera method

**Demo Video:**
<video width="600" controls>
  <source src="docs/小e-按键拍照/video/video1.mp4" type="video/mp4">
  Your browser does not support the video tag
</video>

**Configuration Screenshots:**
![Camera Pin Configuration](docs/小e-按键拍照/img/image1.png)
![Camera Header File](docs/小e-按键拍照/img/image2.png)
![Initialize Monitor](docs/小e-按键拍照/img/image3.png)
![Camera Method](docs/小e-按键拍照/img/image4.png)

### Expression Settings Function
Supports custom emoticon display:
1. Generate or download emoticon images
2. Convert images to C array format
3. Add emoticon data to code
4. Configure display parameters

**Emoticon Examples:**
![Emoticon Generation](docs/小e-表情设置/img/image1.png)
![Image Conversion Tool](docs/小e-表情设置/img/image2.png)
![Add Emoticon Data](docs/小e-表情设置/img/image3.png)
![64-bit Data](docs/小e-表情设置/img/image4.png)
![32-bit Data](docs/小e-表情设置/img/image5.png)
![Filename Correspondence](docs/小e-表情设置/img/image6.png)
![File Location](docs/小e-表情设置/img/image7.png)

### Battery Display Function
Real-time battery level monitoring:
1. Configure ADC pins
2. Add battery monitoring header files
3. Initialize ADC monitor
4. Implement battery level function

**Configuration Screenshots:**
![Battery Pin Configuration](docs/小e-电量显示/img/image1.png)
![Battery Header File](docs/小e-电量显示/img/image2.png)
![Battery Variables](docs/小e-电量显示/img/image3.png)
![ADC Initialization](docs/小e-电量显示/img/image4.png)
![Monitor Initialization](docs/小e-电量显示/img/image5.png)
![GetBatteryLevel Function](docs/小e-电量显示/img/image6.png)

### Volume Control Function
Volume up/down button control:
1. Define volume control pins
2. Initialize button functions
3. Modify constructor
4. Add related header files

**Demo Video:**
<video width="600" controls>
  <source src="docs/小e-音量加减/video/video1.mp4" type="video/mp4">
  Your browser does not support the video tag
</video>

**Configuration Screenshots:**
![Volume Pin Definition](docs/小e-音量加减/img/image1.png)
![Variable Definition](docs/小e-音量加减/img/image2.png)
![Button Initialization](docs/小e-音量加减/img/image3.png)
![Constructor Modification](docs/小e-音量加减/img/image4.png)
![Header File Addition](docs/小e-音量加减/img/image5.png)

### IoT Device Control
Integrated IoT functionality supporting various sensors:
- Temperature and humidity sensor example
- Custom device class implementation
- Property definition and callback functions

**Implementation Screenshots:**
![IoT Tool Class Creation](docs/小e-iot控制设备/img/image1.png)
![Device Initialization](docs/小e-iot控制设备/img/image2.png)

### MCP Device Control
Control external devices via MCP protocol:
- Device initialization
- Communication protocol implementation
- Data transmission and control

**Implementation Screenshots:**
![MCP Code Implementation](docs/小e-mcp控制设备/img/image1.png)
![MCP Initialization](docs/小e-mcp控制设备/img/image2.png)

## Quick Start

### Hardware Preparation
1. Download and print 3D enclosure files
2. Manufacture PCB using Gerber files
3. Purchase required electronic components
4. Solder and assemble hardware

### Software Setup
1. Install ESP-IDF development environment
2. Clone the project: `git clone https://github.com/your-repo/AgentDevice.git`
3. Enter project directory: `cd AgentDevice`
4. Configure project: `idf.py menuconfig`
5. Build and flash: `idf.py build flash`

### Function Testing
Follow the README in each function module for step-by-step implementation and testing.

## Installation and Usage

### Environment Requirements
- ESP-IDF development environment
- 3D printer (for enclosure manufacturing)
- PCB manufacturing service (for circuit boards)

### Compilation and Flashing
1. Install ESP-IDF
2. Clone the project repository
3. Configure project parameters
4. Compile firmware
5. Flash to device

### Hardware Assembly
1. Manufacture PCB using Gerber files
2. Print enclosure using 3D printer
3. Solder components
4. Complete assembly

## Contribution Guidelines

Community contributions are welcome! Please follow these steps:
1. Fork the project
2. Create a feature branch
3. Submit changes
4. Initiate Pull Request

## License

This project uses the Apache License 2.0. See [LICENSE](LICENSE) file for details.

## Contact Us

For questions or suggestions, please contact us through:

- **GitHub Issues**: [Submit Issues](https://github.com/your-repo/AgentDevice/issues)
- **Official Website**: [https://agentdevice.com](https://agentdevice.com)
- **Personal WeChat QR Code**:
  ![Personal WeChat QR Code](docs/contact/wechat_personal_qr.png)
- **Corporate WeChat QR Code**:
  ![Corporate WeChat QR Code](docs/contact/wechat_work_qr.png)

### Sponsorship Support
If you like this project, give it a 🌟, you can unlock more content and open source code

[GitHub Star](https://github.com/EvMatrix/AgentDevice/stargazers)

---

**AgentDevice** - Making smart terminals accessible to everyone!