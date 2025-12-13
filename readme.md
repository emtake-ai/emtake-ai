<h1 align="center">Welcome to Emtake-AI's GitHub</h1>

## EagleBoard from emtake

<p align="center">
  <img src="https://raw.githubusercontent.com/emtake-ai/emtake-ai/main/eagleboard.png" width="100%">
</p>

## SoC LG8111 from LGE

LG8111 is the first Artificail Intelligence SoC for Various on-device AI Applications such as Home Appliance, Robotics and
Autonomous Vehicles

<p align="center">
  <img src="https://raw.githubusercontent.com/emtake-ai/emtake-ai/main/overview.png" width="100%">
</p>

## Synabro SDK from AiM Future

Synabro SDK is a software platform that provides users with a set of tools for deploying
machine learning/deep learning models for inference on NPU hardware (GAIA and NMP supported).
With Synabro, users can compile the models from deep learning frameworks to binary files
targeting the NMP hardware platform and FPGA. Synabro can be used via a Command-line interface
or Python environment

<p align="center">
  <img src="https://raw.githubusercontent.com/emtake-ai/emtake-ai/main/application.png" width="100%">
</p>

### Eagleboard Key Features

Eagleboard is an **AI SoC module with an integrated NPU**, designed to support  
**real-time video and audio AI solutions** on Linux-based edge systems.

#### 🔌 Peripheral & Communication Interfaces

Eagleboard provides a rich set of standard peripheral interfaces for seamless
integration with external devices and sensors.

- **UART** – Debugging, control, and device communication  
- **I²C** – Sensor and peripheral control  
- **SPI** – High-speed peripheral communication  
- **USB** – Camera, audio, storage, and general peripherals  
- **Ethernet** – Network connectivity for streaming and remote control  

#### 🎥 Video Input Capabilities

Eagleboard supports multiple video input paths, enabling flexible camera configurations:

- **MIPI CSI-2** – High-performance image sensors  
- **DVP (Digital Video Port)** – Parallel camera interfaces  
- **USB Camera (UVC)** – Plug-and-play USB cameras  

All video inputs are accessible through **Linux V4L2 (Video4Linux2)**,  
allowing standard camera frameworks and pipelines to be used without modification.

#### 🎤 Audio Input & Output Capabilities

Eagleboard supports multiple audio interfaces for both **capture and playback**:

- **Analog Mono Microphone** – Simple and low-power audio input  
- **PDM Digital Microphone** – High-quality digital microphone interface  
- **USB Audio (UAC)** – Standard **USB microphones and speakers** via USB Audio Class  

All audio devices are exposed through **Linux ALSA**, ensuring compatibility with
standard Linux audio frameworks and tools.

#### 🐧 Linux-Friendly Multimedia Stack

Eagleboard runs on **Linux**, providing native access to multimedia devices:

- **V4L2** for video capture and processing  
- **ALSA** for audio capture and playback  

This allows seamless integration with widely used frameworks such as
**OpenCV**, **GStreamer**, and **FFmpeg**.

#### 🚀 Application Enablement

By combining rich I/O, multimedia interfaces, and an integrated NPU,
Eagleboard enables a wide range of GPU-free edge AI applications:

- AI-powered **video analytics**
- **Audio analysis** and voice-based solutions
- **Multimodal AI pipelines** combining video and audio
- Real-time **edge inference** on an AI SoC with an integrated NPU

> **Eagleboard enables flexible, GPU-free edge AI solutions with standard Linux  
> video and audio interfaces on an AI SoC with an integrated NPU.**


#### Video Solution
It use the MIPI, DVP, UVC through USB for Video application
<p align="center">
  <img src="https://raw.githubusercontent.com/emtake-ai/emtake-ai/main/videosolution.png" width="100%">
</p>


#### Audio solution 1
It use the the analog MIC and digital MIC as MIC meanwhile it use the speaker with I2S Amplifier in Audio Application

<p align="center">
  <img src="https://raw.githubusercontent.com/emtake-ai/emtake-ai/main/audiosolution_1.png" width="100%">
</p>


#### Audio solution 2
It use the USB as MIC and Speaker for Audio Application
<p align="center">
  <img src="https://raw.githubusercontent.com/emtake-ai/emtake-ai/main/audiosolution_2.png" width="100%">
</p>