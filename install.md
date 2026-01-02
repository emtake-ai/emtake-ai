## EagleBoard AI SDK – Installation & Workflow Guide

This document explains the full workflow from GPU Training PC setup to deployment on EagleBoard NPU.

### 1. Prepare Ubuntu 22.04 Training PC (NVIDIA GPU)  

Use Ubuntu 22.04 and Python ≥ 3.10.  

#### 1.1 Install NVIDIA Driver  
sudo apt update  
sudo apt install -y nvidia-driver-550 : you should check your nvidia GPU driver's version  
sudo reboot   
nvidia-smi  

#### 1.2 Install CUDA Toolkit  

Download CUDA Toolkit (runfile installer) from NVIDIA and install it.  

sudo sh cuda_12.1.1_535.86.10_linux.run --toolkit : you should check the version of CUDA  

#### 1.3 Install cuDNN  

Download cuDNN for CUDA 12 and install it.  

tar -xf cudnn-linux-x86_64-8.x.x_cuda12-archive.tar.xz  
sudo cp cudnn-*/include/* /usr/local/cuda/include/   
sudo cp cudnn-*/lib/* /usr/local/cuda/lib64/   
sudo ldconfig  

#### 1.4 Install Media & Vision Libraries  

sudo apt install -y \  
gstreamer1.0-tools gstreamer1.0-libav gstreamer1.0-plugins-* \  
ffmpeg v4l-utils \   
libopencv-dev python3-opencv \   
alsa-utils libasound2-dev  

#### 1.5 Install Python, Git, Docker  
sudo apt install -y python3.10 python3.10-venv git docker.io  
sudo usermod -aG docker $USER  
newgrp docker  

### 2. Training on GPU PC  
#### 2.1 Install LabelImg  
git clone https://github.com/tzutalin/labelImg  
cd labelImg   
pip install pyqt5 lxml  
python labelImg.py  


[how to use V4L2 Device with gstreamer](install_2.md)
[how to use ALSA Device with gstreamer](install_1.md)



