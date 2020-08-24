![TensorFlow-AI-Simple-Object-Detection-Webcam](./img/artificial-intelligence-3382507_640.jpg)

TensorFlow-AI-Simple-Object-Detection-Webcam
---
TensorFlow Simple Object Detection with Webcam on a Mac.

---

#### Setup Anaconda
  - Download/Install Anaconda
    
    [https://www.anaconda.com](https://www.anaconda.com)
  - Clone Repo
  
    `git clone https://github.com/stea4lth/TensorFlow-AI-Simple-Object-Detection-Webcam.git`
    
    > *Change into the directory*

    `cd TensorFlow-AI-Simple-Object-Detection-Webcam`                                                                                                          
                                                                                                                    
  - Setup Virtual Environment
    > *Choose your environment name - **myenv***

    `conda create -n myenv python`
  - Activate Environment
  
    `conda activate myenv`
    
  - Install TensorFlow
  
    `pip install tensorflow`
    
  - Install other needed libraries
      ```
    pip install Cython
    pip install contextlib2
    pip install pillow
    pip install lxml
    pip install jupyter
    pip install matplotlib
      ```
    
  - Install protoc
    > Download the latest release
    
    [https://github.com/protocolbuffers/protobuf/releases/latest](https://github.com/protocolbuffers/protobuf/releases/latest)
    
     1. Copy *protoc* binary into environment bin directory
     
        `cp ~/Downloads/protoc-3.12.4-osx-x86_64/bin/protoc /opt/anaconda3/envs/myenv/bin/`
     2. Copy *includes* contents into environment includes directory
        
        `cp ~/Downloads/protoc-3.12.4-osx-x86_64/include/* /opt/anaconda3/envs/myenv/include/`
        
        > You might need to allow *protoc* in **System Preferences > Security & Privacy**
        
  - Clone TensorFlow Models
    1. Change into environment directory
    
       `cd /opt/anaconda3/envs/myenv`
       
    2. Clone TensorFlow Models
    
       `git clone https://github.com/tensorflow/models.git`
              
    3. Compile *protos*
     
       `cd models/research` - *Must run from this directory*
       
       `protoc object_detection/protos/*.proto --python_out=.`
       
    4. Install TensorFlow Object Detection API
    
       `cp object_detection/packages/tf2/setup.py .`

       `python -m pip install .`
       
    5. Test API
        
       `python object_detection/builders/model_builder_tf2_test.py`

#### Run Program
  - Change into *TensorFlow-AI-Simple-Object-Detection-Webcam* directory
  
    `cd ~/TensorFlow-AI-Simple-Object-Detection-Webcam`
  
  - Run Program
    
      `python index.py`
