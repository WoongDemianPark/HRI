# ReSpeaker USB 4 Mic Array

>Available at [Seeed](https://www.seeedstudio.com/ReSpeaker-Mic-Array-v2.0-p-3053.html)

![](http://respeaker.io/assets/images/usb_4_mic_array.png)

The ReSpeaker USB 4 Mic Array is the successor of the ReSpeaker USB 6+1 Mic Array. It has better built-in audio processing algorithms than the 6+1 Mic Array, so it has better audio recording quality, although it only has 4 microphones.

## Features
+ 4 microphones
+ 12 RGB LEDs
+ USB
+ built-in AEC, VAD, DOA, Beamforming and NS
+ 16000 sample rate

## Install Drivers
[Follow the drivers installation guide](https://github.com/WoongDemianPark/HRI/tree/main/MicArray/driver)

## Device Firmware Update
The Microphone Array supports USB DFU. We have [a python script - dfu.py](https://github.com/WoongDemianPark/HRI/blob/main/MicArray/dfu.py) to do that.

```
pip install pyusb
python dfu.py --download 6_channels_firmware.bin        # with sudo if usb permission error
```

| firmware | channels | note |
|---------------------------------|----------|-----------------------------------------------------------------------------------------------|
| 1_channel_firmware.bin | 1 | processed audio for ASR |
| 6_channels_firmware.bin | 6 | channel 0: processed audio for ASR, channel 1-4: 4 microphones' raw data, channel 5: playback |

</br>

----------
</br>

# Usage

## Create virtual environment for the module.
```
conda create -n MicArray python=3.9
conda activate MicArray
```
  
## Install requirements.
```
pip install -r requirements.txt
```
  
## If the 'usb' module is not installed correctly, install it manually.
```
sudo pip3 install pyusb
```

## Connect the ReSpeaker USB 4 Mic Array to the NUC PC using a USB cable.

run "doa.py' for Direction of Arrival.
```
sudo python3 doa.py
```

run "vad.py' for Voice Activity Detection.
```
sudo python3 vad.py
```
