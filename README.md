# Tutorial-to-set-up-an-Arducam-USB-2.0-in-Micro-manager-Tutorial
Step by step to set up an Arducam with module USB 2.0 (UVC) in Micro-manager

## Camera Set up
1. Connect the Arducam in the computer.
You have several options to control the camara, in this tutorial AMCap will be used, the idea is to disable automatic options and prevent bugs when Micro-Manager is being used.
2. Download AMCap and open the .exe file
3. 
## Micro-Manager installation
1. It is neccesary to download Version 2.0 from Micro-Manager web, it is strongly recommended to use a Nightly Build version: https://download.micro-manager.org/nightly/2.0/Windows/. Once it is downloaded, open the .exe file and do the installation tutorial. Note: if you have not ImageJ downloaded it can be installed in the tutorial.
<img src="Images/fileexe.png" width="300">

## Micro-Manager SetUp
2. Once it is installed restart the PC and open Micro-Manager. It should appear in first instance ImageJ and in a few seconds Micro/Manager starting like this:
<img src="Images/startingmicrom.png" width="400">
3. Only click in Hardware Configuration File to choose '(none)' and select 'OK'.
<img src="Images/choosenone.png" width="400">
4. It should appear the following window:
<img width="777" height="311" alt="image" src="https://github.com/user-attachments/assets/931bd94e-2936-4378-ac28-38152f41ac7f" />
5. Press the option 'Devices' and select 'Harward configuration wizard'.
<img width="782" height="331" alt="image" src="https://github.com/user-attachments/assets/f37afe57-57ff-4b61-99c5-f9afed4e73a8" />
6. Select 'Create a new configuration' and 'Next'.
<img width="876" height="851" alt="image" src="https://github.com/user-attachments/assets/276125d6-3407-4496-b455-7ae84cd292d2" />
7. Now look for 'OpenCVGrabber' in the 'List by module' and click in 'OpenCVGrabber: OpenCVGrabber video input', next press 'add'.
<img width="880" height="860" alt="image" src="https://github.com/user-attachments/assets/c24d2eef-657d-40fc-b160-78f711ff6e00" />
8. Another window will appear, now press below 'Value' and choose 'Arducam USB'
<img width="562" height="345" alt="image" src="https://github.com/user-attachments/assets/f7d0fc0b-5712-4310-90d1-6caf647ba237" />
