## How to study for deep learning classification in eagleboard
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
##### you should unzip after above
```text
unzip dataset.zip
```
#### 1.3 train the model with downloaded files
```text
cp ./model-sample/models/Keras/alexnet.py .
```
#### 1.4 using docker, you should train
```text
sudo docker run -it --gpus all --rm -v .:/synabro -v directory_for_synabro_data:/root/.local/synabro/data
```  
```text
python3 alexnet.py
```
##### after training is completed, you can get file as "alexnet.keras"
#### 1.5 you should copy alexnet.keras to /root/.local/synabro/data/modelzoo/keras
```text
cp ./alexnet.keras /root/.local/synabro/data/modelzoo/keras
```
##### you should run below command with file modification  
```text
vi /root/.local/synabro/share/models.json
```
##### you should put below into the below into the models.json
```text
,"keras/alexnet": {
"name": "alexnet"
,"framework": "keras"
,"path": "keras/alexnet"
}
```
##### after above, you should run below command
```text
synabro --net keras/alexnet
```
##### after it, you can find out alexnet.lne
#### 1.6 you prepare the eagleboard to boot with login root/root
##### you can see the /root as a current directory

#### 1.6. you should copy alexnet with sftp with below command
```text
sftp user@IP
```
```text
cd ./.../.../...
```
```text
put alexnet.lne 
```

#### 1.7. you should run below command in eagleboard
```text
python3 ./deploy_classification.py
```

