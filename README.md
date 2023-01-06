# 1. Initial Setting

## 1.1 Install Anaconda on the NUC PC

* Visit the Anaconda Distribution page.
  * https://www.anaconda.com/products/distribution


* Download the recommended version of Anaconda for Linux.
  * Ubuntu 22.04 was used for existing projects.


* Run the downloaded Install File.
  ```
  bash "downloaded Install File name".sh
  ```

* Press Enter, answer 'yes', press Enter again to confirm the location.

* answer 'yes' to initialize Anaconda3 by running conda init.

* Update the bashrc
  ```
  source ~/.bashrc
  ```

* The installation is complete if (base) appears before the command.    
</br>

## 1.2. Install pip on the Linux.

* Update system repository.
  ```
  sudo apt update
  sudo apt upgrade -y
  ```

* Install Python3 pip.
  ```
  sudo apt install python3-pip -y
  ```

* Confirm the Pip Version and Installation
  ```
  pip3 --version
  ```
</br>

## 1.3. Install git on the Linux.

* Update system repository.
  ```
  sudo apt update
  sudo apt upgrade -y
  ```

* Install git.
  ```
  sudo apt install git -y
  ```

* Confirm the Git Version and Installation.
  ```
  git --version
  ```
</br>

## 1.4. Make or Clone "HRI" folder in Home.

* All modules worked and ran from HRI folder within Home path.
</br>

----------
</br>

# 2. Mic Array Module Setting

## 2.1. Download or clone the "seeed-voicecard" module in HRI folder.

* This module is only used when a firmware update is required.
</br>

## 2.2. Set the "MicArray" module.

* Download or clone the "MicArray" module in HRI folder.

* Create virtual environment for the module.
  ```
  conda create -n MicArray python=3.9
  conda activate MicArray
  ```
  
* Install requirements.
  ```
  pip install -r requirements.txt
  ```
  
* If the 'usb' module is not installed correctly, install it manually.
  ```
  sudo pip3 install pyusb
  ```

* Connect the microphone module to the NUC PC using a USB cable.

* run "doa.py' for Direction of Arrival.
  ```
  sudo python3 doa.py
  ```

* run "vad.py' for Voice Activity Detection.
  ```
  sudo python3 vad.py
  ```
  </br>

----------
</br>

# 3. Speaker Diarization Module Setting

## 3.1. Set the "diart" module.

* Download or clone the "diart" module in HRI folder.

* Create virtual environment for the module.
  ```
  conda create -n diart python=3.9
  conda activate diart
  ```

* Install requirements.
```
pip install -r requirements.txt
```

* Install CUDA.
```
sudo apt-get update
sudo apt-get -y install nvidia-cuda-toolkit
```

* Confirm the CUDA Version and Installation.
```
nvcc -V
```

* Install PyTorch for the installed CUDA version.
  * https://pytorch.org/get-started/locally/#start-locally
  
* Install PortAudio and Soundfile.
```
conda install portaudio
pip install PySoundFile
conda install pysoundfile -c conda-forge
```

* Install Pyannote.audio 2.0.
```
pip install pyannote.audio
pip install git+https://github.com/pyannote/pyannote-audio.git@2.0.1#egg=pyannote-audio
```

* Install Diart Module.
```
pip install diart
```

* run microphone stream module.
```
diart.stream microphone
```
