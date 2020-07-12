## Enabling WSL for Windows
right click windows icon and go to Windows PowerShell (Admin)
run these commands
````
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
````
Restart your computer

More information about installation can be found here (https://docs.microsoft.com/en-us/windows/wsl/install-win10)[https://docs.microsoft.com/en-us/windows/wsl/install-win10]

## Download Ubunutu
Go to this link (https://aka.ms/wslstore)[https://aka.ms/wslstore]
go to ubuntu and install it

after installation go here and download VcXsrv
(https://sourceforge.net/projects/vcxsrv/)[https://sourceforge.net/projects/vcxsrv/]
Launch XLaunch and setup XLaunch for the first time
Just hit next until it gives an option to save configuration
Save the configuration file to the desktop

To have XLaunch run at startup
Win + r 
type and enter this to get to the startup directory
%AppData%/Microsoft/Windows/Start Menu/Programs/Startup
Move the configuration you just saved on the desktop into this directory
Now on startup XLaunch with start on its own

This is a window server which will allow you to open images/gui 

launch ubuntu and setup and password
The password will be used when ever you run a command with the sudo prefix 

## Download SSH
after setting up ubuntu run these commands
````
sudo apt-get upgrade
sudo apt-get ubuntu-minimal ubuntu-standard
echo export DISPLAY=localhost:0.0 >> ~/.bashrc
source ~/.bashrc
sudo apt-get install x11-apps
````

then you can connect to the hep machines by doing

ssh -XY username@login.hep.wisc.edu