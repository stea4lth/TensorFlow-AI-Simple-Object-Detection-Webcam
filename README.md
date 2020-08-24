TensorFlow-AI-Simple-Object-Detection-Webcam
---
TensorFlow Simple Object Detection with Webcam on a Mac.

---

#### Setup Anaconda
  - Download/Install Anaconda
    
    [https://www.anaconda.com](https://www.anaconda.com)
  - Clone Repo
  
    `git clone https://github.com/stea4lth/TensorFlow-AI-Simple-Object-Detection-Webcam.git`
    
    > *Change into the dir*

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
        
  - Clone TensorFlow Models
    1. Change into environment directory
    
       `cd /opt/anaconda3/envs/myenv`
    2. Compile *protos*
       
          `cd models/research/`
   
   
