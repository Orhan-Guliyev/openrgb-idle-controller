# OpenRGB Idle Controller

A Python script for automatically controlling lighting via **OpenRGB**. 

The main feature is tracking user activity in Windows. The script gently dims the backlight if the PC has been idle for a long time and launches a beautiful “scrolling” animation when the user returns.

## ✨ Key Features
* **Smart Sleep Mode:** The script uses the Windows API (`GetLastInputInfo`) to accurately determine the duration of inactivity.
* **Smooth Dimming:** When the timeout is exceeded (15 minutes by default), the backlight gradually fades to zero.
* **Custom “Welcome” Animation:** When the script is first launched or when the PC wakes up, a running-light effect fills the strip with the base color.
* **Dynamic Effect While in Use:** While you’re at the computer, a light pulse smoothly “travels” across your devices.

## 🛠 Requirements and Dependencies
1. The [OpenRGB](https://openrgb.org/) server must be installed and running.
2. **Windows** operating system (since `ctypes` system calls are used).
3. The `openrgb-python` library.
