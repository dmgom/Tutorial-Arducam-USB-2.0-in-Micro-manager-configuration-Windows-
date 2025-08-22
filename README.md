# Tutorial-to-set-up-an-Arducam-USB-2.0-in-Micro-manager-Tutorial
Step by step to set up an Arducam with module USB 2.0 (UVC) in Micro-manager.

## Camera Set up with AMCap
1. Connect the Arducam in the computer.
You have several options to control the camara, in this tutorial AMCap will be used, the idea is to disable automatic options and prevent bugs when Micro-Manager is being used. Also, it is highly recommended to visit Arducam page to understand the camera options, as well as to see the datasheet: https://docs.arducam.com/UVC-Camera/Appilcation-Note/Software-Instruction/UVC-Software-Instructions/. Please, check the SDK of the camera model to comprehense better adjusts in camera.

<img width="900" alt="image" src="https://github.com/user-attachments/assets/f27fb253-0d86-4d58-b423-397775d83a17" />

2. You can download AMCap in this link: https://www.arducam.com/downloads/app/AMCap.exe. Once it is downloaded please open the .exe file.
<img width="155" height="30" alt="image" src="https://github.com/user-attachments/assets/9e62275b-fb89-4949-8dd9-2518c9134e87" />

3. Once the app is opened, select the option 'Devices' and click in 'Arducam USB Camera'.
<img width="900" alt="image" src="https://github.com/user-attachments/assets/fe72891a-dead-417f-a848-93d90b58564d" />


4. Now, press 'Options' and select 'Video Capture Filter'.

<img width="900" alt="image" src="https://github.com/user-attachments/assets/ab479076-88dc-4895-82c8-edc60f869473" />

5. In 'Video Proc Amp' uncheck 'White balance', and in 'Camera Control' uncheck exposure and 'Low Light compensation', click 'Apply' and then 'OK'
<img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/24ca3242-327e-4674-9689-37ca6dd99268" />
<img width="295" height="250" alt="image" src="https://github.com/user-attachments/assets/1a0cf04c-974d-40f4-9b4f-4bb77fa0f1d8" />

## Micro-Manager installation
6. It is neccesary to download Version 2.0 from Micro-Manager web, it is strongly recommended to use a Nightly Build version: https://download.micro-manager.org/nightly/2.0/Windows/. Once it is downloaded, open the .exe file and do the installation tutorial. Note: if you have not ImageJ downloaded it can be installed in the tutorial.
<img src="Images/fileexe.png" width="300">

## Micro-Manager Configuration
7. Once it is installed restart the PC and open Micro-Manager. It should appear in first instance ImageJ and in a few seconds Micro/Manager starting like this:
<img src="Images/startingmicrom.png" width="400">
8. Only click in Hardware Configuration File to choose '(none)' and select 'OK'.

<img src="Images/choosenone.png" width="400">

9. It should appear the following window:
<img width="500" alt="image" src="https://github.com/user-attachments/assets/931bd94e-2936-4378-ac28-38152f41ac7f" />

10. Press the option 'Devices' and select 'Harward configuration wizard'.

<img width="500" height="331" alt="image" src="https://github.com/user-attachments/assets/f37afe57-57ff-4b61-99c5-f9afed4e73a8" />

11. Select 'Create a new configuration' and 'Next'.
<img width="500" height="851" alt="image" src="https://github.com/user-attachments/assets/276125d6-3407-4496-b455-7ae84cd292d2" />

12. Now look for 'OpenCVGrabber' in the 'List by module' and click in 'OpenCVGrabber: OpenCVGrabber video input', next press 'add'.
<img width="500" height="860" alt="image" src="https://github.com/user-attachments/assets/c24d2eef-657d-40fc-b160-78f711ff6e00" />

13. Another window will appear, now press below 'Value', choose 'Arducam USB Camera' and then click 'OK'.
<img width="420" height="345" alt="image" src="https://github.com/user-attachments/assets/f7d0fc0b-5712-4310-90d1-6caf647ba237" />

14. Now, it will appear in the upper table the category 'OpenCVGrabber:...'. Therefore, press 'Next'.
<img width="500" height="850" alt="image" src="https://github.com/user-attachments/assets/93dc2af0-8619-4c83-b7da-e378ce5d006d" />

15. In the following window uncheck 'Use Autoshutter By Default' and press 'Next'.
<img width="500" height="857" alt="image" src="https://github.com/user-attachments/assets/ea2aad08-5e0b-4582-af2b-842355c5961a" />

16. The next window will appear empty, just press 'Next'.
<img width="500" height="850" alt="image" src="https://github.com/user-attachments/assets/a792e096-2463-4d89-836a-a74e507a79d9" />

17. This window will also be empty, just press 'Next'.
<img width="500" height="850" alt="image" src="https://github.com/user-attachments/assets/f2f52bd3-da97-4e65-a2d0-fcca6db50ad2" />

18. Now, choose where do you want to save the configuration file for later use, fill the file name, press 'Save' and therefore press 'Finish'.
<img width="500" height="856" alt="image" src="https://github.com/user-attachments/assets/8734f380-fb2c-4d02-95e9-f98c67da66a5" />

19. Then, configuration was made and the main window will appear, now you can use live or snap to see the camera capturing.
<img width="500" height="317" alt="image" src="https://github.com/user-attachments/assets/0d14e34e-811e-463f-9483-4403b852a219" />

20. If the image seems overexposed, you can try 'Auto Once' in 'Inspect Preview'. This adjust automatically White balance.
  <img width="810" height="737" alt="image" src="https://github.com/user-attachments/assets/7a7b5337-1a0c-4708-9902-f4e1bd267030" />
Now, the image after press 'Auto Once'.
  <img width="810" height="737" alt="image" src="https://github.com/user-attachments/assets/ce9081ab-d4e9-47ee-b0a6-e44e861e67d3" />
  
# NOTE:
Exposure parameters in Micro-Manager must be the same as AMCap, those are -13 to 0, whose respectively ms are in the following table. In other case, it will lead bugs in Micro-Manager. Additionally, the lag in live is proportional to greater exposure times.

<img width="500" height="709" alt="image" src="https://github.com/user-attachments/assets/61cbeeed-6cc8-4fa0-8e22-7b455cbd5a0e" />

Table extracted from: https://docs.arducam.com/UVC-Camera/Appilcation-Note/Software-Instruction/UVC-Software-Instructions/

