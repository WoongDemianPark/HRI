# 1. Initial Setting

## 1.1 Install Anaconda on the NUC PC

* Visit the Anaconda Distribution page.
  * https://www.anaconda.com/products/distribution


* Download the recommended version of Anaconda for Linux.
  * Ubuntu 22.04 was used for existing projects.


* Run the downloaded Install File.
  ```
  $ bash "downloaded Install File name".sh
  ```

* Press Enter, answer 'yes', press Enter again to confirm the location.

* answer 'yes' to initialize Anaconda3 by running conda init.

* Update the bashrc
  ```
  $ source ~/.bashrc
  ```

* The installation is complete if (base) appears before the command.    
</br>

## 1.2. Install pip on the Linux.

* Update system repository.
  ```
  $ sudo apt update
  $ sudo apt upgrade -y
  ```

* Install Python3 pip.
  ```
  $ sudo apt install python3-pip -y
  ```

* Confirm the Version and Installation
  ```
  $ pip3 --version
  ```
</br>

## 1.3. Install git on the Linux.

* Update system repository.
  ```
  $ sudo apt update
  $ sudo apt upgrade -y
  ```

* Install git.
  ```
  $ sudo apt install git
  ```

* Confirm the Version and Installation.
  ```
  $ git --version
  ```
</br>

## 1.4. Make or pull "HRI" folder in Home.

* All modules worked and ran from HRI folder within Home path.
</br>

----------
</br>

# 2. Mic Array Module Setting

## 2.1. Download the "seeed-voicecard" module in HRI folder.

* This module is only used when a firmware update is required.
</br>

## 2.2. Set the "MicArray" module.

* Download the "MicArray" module in workspace folder.

* Create virtual environment for the module.
  ```
  $ conda create -n MicArray python=3.9
  $ conda activate MicArray
  ```
  
* Install requirements
  ```
  $ pip install -r requirements.txt
  ```
  
* If the 'usb' module is not installed correctly, install it manually.
  ```
  $ sudo pip3 install pyusb
  ```

* Connect the microphone module to the NUC PC using a USB cable.

* run "doa.py' for Direction of Arrival.
  ```
  $ sudo python3 doa.py
  ```

* run "vad.py' for Voice Activity Detection.
  ```
  $ sudo python3 vad.py
  ```
