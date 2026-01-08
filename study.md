## How to study for deep learning classification  
### 1. Classification  
#### 1.1 download github repository called emtake-ai/eagleboard-video.git
```text
git clone https://github.com/emtake-ai/eagleboard-video.git
```
##### after download it, you should mv with cd ./eagleboard-video  
```text
cd ./eagleboard-video
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
python3 ./train_classification.py
```
##### after training is completed, you can get file as "classification.keras"
#### 1.4. you can predict the training model's weight with below command
```text
python3 ./predict_classification.py
```

