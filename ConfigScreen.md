## To Install the screen:  
After you log into the Pwnagotchi via SSH you run the following commands.  
```
git clone https://github.com/waveshare/e-Paper.git  
cd e-Paper/RaspberryPi_JetsonNano/python/  
sudo apt-get update  
sudo apt-get install python3-pip  
sudo apt-get install python3-pil  
sudo apt-get install python3-numpy  
sudo pip3 install RPi.GPIO  
sudo pip3 install spidev  
sudo python3 setup.py build  
sudo python3 setup.py install  
python3 examples/epd_2in13_V2_test.py  
```
This should show the screen working.  
![image](https://user-images.githubusercontent.com/71237545/135695943-2609a5c5-4bc2-4069-96c4-0cd026318b93.png)  

