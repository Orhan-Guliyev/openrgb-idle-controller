# OpenRGB Idle Controller
**This is my first project on GitHub!🎉**

A Python script for automatically controlling lighting via **OpenRGB**

The main feature is tracking user activity in Windows. The script gently dims the backlight if the PC has been idle for a long time and launches a beautiful “scrolling” animation when the user returns

## ✨ Key Features
* **Smart Sleep Mode:** The script uses the Windows API (`GetLastInputInfo`) to accurately determine the duration of inactivity.
* **Smooth Dimming:** When the timeout is exceeded (15 minutes by default), the backlight gradually fades to zero.
* **Custom “Welcome” Animation:** When the script is first launched or when the PC wakes up, a running-light effect fills the strip with the base color.
* **Dynamic Effect While in Use:** While you’re at the computer, a light pulse smoothly “travels” across your devices.
  
**Welcome Animation & Cycled "In Use" animation showcase**

<img width="400" height="626" alt="IMG_2335" src="https://github.com/user-attachments/assets/409d0c05-d542-4bc5-ab92-26077fc3249f" />

## 🛠 Requirements and Dependencies
1. The [OpenRGB](https://openrgb.org/) server must be installed and running.
2. Python 3.13+
3. Windows 11 OS (i didn't test it on Windows 10 so let me know if it works)
4. Install `openrgb-python pystray pillow` libraries
   
## 📖 How to use
1. Create a folder where it's convenient for you to store the script, and place the script itself in that folder
2. Open the folder in the terminal or run cmd as an administrator and type `cd “path to your folder”`
3. Copy and paste `python -m PyInstaller --noconsole --onefile openrgb-idle-controller.py` inside terminal and press Enter
4. Now find the Task Scheduler and open it
5. In the Task Scheduler interface, on the right, you'll see the “Task Scheduler Library.” From the list there, click “Create a simple task"
6. Name your task whatever you like, then proceed to the next step, where you'll need to select “When Windows starts,” then choose “Run a program” and specify the path to your folder
7. Inside the folder, navigate to the “dist” folder, which contains “openrgb-idle-controller.exe”—the file we need to specify for the Task Scheduler to run. Click ‘Next’ and “Finish.”
8. Open OpenRGB, go to Settings, and select the options shown in my screenshot below. You can specify any other port for the server.
9. Enjoy!
    
<img width="554" height="173" alt="image" src="https://github.com/user-attachments/assets/9e5b4983-bf99-4d81-83d4-5fc7d85672cd" />

# If you have any questions, please ask them [here](https://github.com/Orhan-Guliyev/openrgb-idle-controller/discussions/categories/q-a)
