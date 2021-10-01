# Burning and setting our Pwnagotchi:  

After we download and install the image on the MicroSD card we unplug the new Card (unmount safe) and mount it again.  
we create a file called ssh with nothing inside, and also a file called config.toml  

Content of config.toml  
``` 
main.name = "THE NAME OF YOUR PWNAGOTCHI"
main.lang = "en"
main.whitelist = [
  'YOUR NETWORK','YOUR OTHER NETWORK'
]

main.plugins.grid.enabled = true
main.plugins.grid.report = true
main.plugins.grid.exclude = [
  'YOUR NETWORK','YOUR OTHER NETWORK'
]

ui.display.enabled = true
ui.display.type = "waveshare_2"
ui.display.color = "black" 
```  
Connect your Pwnagotchi on the second port to your computer.  
Connect on the Second port (DATA PORT)  
![image](https://user-images.githubusercontent.com/71237545/135692216-cf38076a-aae6-4c1e-9a8a-5904739eec9f.png)  
Once is connected you configure your usb interface with static ip address just like the Pre-Face says https://pwnagotchi.ai/configuration/#pre-face  
![image](https://user-images.githubusercontent.com/71237545/135693395-9601404b-4526-4190-bd0c-0a352f5c6e7c.png)  
After configuring the interface we check the connection with putty to the Pwnagotchi.  
![image](https://user-images.githubusercontent.com/71237545/135693419-5c3a9099-9098-46b5-baeb-210093f3e044.png)  
And we set the PowerShell to be able for the Pwnagotchi to navigate 

# Giving Internet access to the Pwnagotchi

First we have to download this script if is for windows. https://raw.githubusercontent.com/evilsocket/pwnagotchi/master/scripts/win_connection_share.ps1  
For others Operating Systems check
We Open a PowerShell as administrator and we execute the following  
```
powershell -ep bypass 
./win_connection_share.ps1 -SetPwnagotchiSubnet  
./win_connection_share.ps1 -EnableInternetConnectionSharing  
```
![image](https://user-images.githubusercontent.com/71237545/135694870-027b5b61-7042-4ad5-92fe-336dbec0ea55.png)  
This will show Which connection you want to share and to which connection is given the access.  
Once we do this, we should have internet on our pwnagotchi  
![image](https://user-images.githubusercontent.com/71237545/135695284-66476633-cad1-428c-8e9c-62445716ca8b.png)  
# Note:  
Remember to change the nameserver under resolv.conf to 8.8.8.8 otherwise it won't resolve names.  
![image](https://user-images.githubusercontent.com/71237545/135695113-494bc5b3-1e0f-48ee-b06d-349bbdf4f627.png)  

