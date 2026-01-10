## How to study for deep learning classification in eagleboard

<p align="center">
  <img src="https://raw.githubusercontent.com/emtake-ai/emtake-ai/main/eagleboard-case.png" width="50%">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/emtake-ai/emtake-ai/main/eagleboard-case-explain.png" width="50%">
</p>

### 0. Eagleboard unboxing  
#### You should open the box and connect with below contents of youtube  
[unboxing for eagleboard on how to communicate with minicom in ubuntu](https://youtu.be/hFXY7798rrM)

[how to wire usb2ethernet with eagleboard](https://youtu.be/HwZ2ReAg7Y4)  

### 1. Classification  
#### 1.1 download github repository called emtake-ai/eagleboard-video.git
```text
git clone https://github.com/emtake-ai/deep-learning.git
```
##### after download it, you should mv with cd ./deep-learning  
```text
cd ./deep-learning
```
#### 1.2 download huggingface.co/emtake-ai website with one click away  
```text
www.huggingface.co/emtake-ai
```
##### you put copy above, and paste it into the web browser.
##### from there, you should follow below link from youtube
[download dataset.zip file from huggingface : youtube ](https://www.youtube.com/watch?v=nj-GDC2Z_Ac)  
##### after downloading, you mv dataset.zip into the current working directory
```text
cp ~/Downloads/dataset.zip .
```
##### you should unzip after above
```text
unzip dataset.zip
```
#### 1.3 train the model with downloaded files
```text
cp ./model-sample/models/Keras/mobilenet.py .
```
#### 1.4 using docker, you should train
```text
sudo docker run -it --gpus all --rm -v .:/synabro -v directory_for_synabro_data:/root/.local/synabro/data
```  
```text
python3 mobilenet.py
```
##### after training is completed, you can get file as "mobilenet.keras"
#### 1.5 you should copy mobilenet.keras to /root/.local/synabro/data/modelzoo/keras
```text
cp ./mobilenet.keras /root/.local/synabro/data/modelzoo/keras
```
##### you should run below command with file modification  
```text
vi /root/.local/synabro/share/models.json
```
##### you should put below into the below into the models.json
```text
,"keras/mobilenet": {
"name": "mobilenet"
,"framework": "keras"
,"path": "keras/mobilenet"
}
```
##### after above, you should run below command
```text
synabro --net keras/mobilenet
```
##### after it, you can find out mobilenet.lne
#### 1.6 you prepare the eagleboard to boot with login root/root
##### you can see the /root as a current directory

#### 1.6. you should copy mobilenet with sftp with below command
```text
sftp root@192.168.x.x
password : root
```
```text
cd ./aimf_demo
put deploy_classification.py
```
```text
cd ./LNE/Detection/
```
```text
put mobilenet.lne 
```

#### 1.7. you should run below command in eagleboard
```text
cd 
cd ./aimf_demo
python3 ./deploy_classification.py
```

#### You can check with all with youtube 
[check all-1](https://youtu.be/iKezqnlwjhE)  
[check all-2](https://youtu.be/T_cGhqvI1ZA)