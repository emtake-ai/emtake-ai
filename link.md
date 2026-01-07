## build and deploy in PC

### 1. Download EagleBoard Video Repository

##### This repository contains all scripts for dataset preparation, training, conversion, and EagleBoard inference.
```text
git clone https://github.com/emtake-ai/eagleboard-video.git
cd eagleboard-video
```
[download eagleboard-video repo using git clone](https://www.youtube.com/watch?v=ympIrndBtxo)   

### 2. Download Dataset from HuggingFace

##### Download your classification dataset zip file after checking below link

[download dataset zip file from huggingface ](https://www.youtube.com/watch?v=nj-GDC2Z_Ac)  

### 3. Train the Classification Model (PC)

##### Move to training directory and check below link

```text
python3 train_classification_mobilenet.py
```

[train the model for classification](https://www.youtube.com/watch?v=oubfgcZ3uSU)  


### 4. Predict Result on PC

#### Test the trained model on PC webcam:

```text
python3 ./predict_classication.py
```

[predict the result of training in PC](https://www.youtube.com/watch?v=lAREw5jWyGc)  


## Build and deply in Eagleboard

### 1. Build & Train Model for EagleBoard
 
```text
git clone https://github.com/emtake-ai/deep-learning.git
cd deep-learning
```

```text
https://www.huggingface.co/emtake-ai
```
in here you should download the dataset.zip files from huggingface

move the working directory and copy dataset.zip into here.

```text
unzip dataset_classification_mobilenet.zip
```

```text
cp ./model-sample/models/Keras/alexnet.py .
```

```text
python3 ./alexnet.py
```

[eagleboard : build the model and train the model](https://www.youtube.com/watch?v=qabNeS_zZoM)  

### 2. how to train and convert it to the LNE file

```text
sudo docker run -it -v .:synabro -v /home/user/Work/data_synabro:/root/.local/synabro/data synabro:1.3.0 /bin/bash
```

```text
python3 ./alexnet.py
```

```text
cp ./alexnet.keras /root/.local/synabro/data/modelzoo/keras/
```

```text
synabro --net keras/alexnet
```

[eagleboard : how to train and convert it to the LNE file](https://www.youtube.com/watch?v=e6KDznN6WK8)   

