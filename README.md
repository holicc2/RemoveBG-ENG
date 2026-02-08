# RemoveBG-ENG
A fork of a great Remove Background AI tool using rembg by JamesH<br>
This is for GIMP 3.0+ Flatpak version<br>
<br><br>
## Instructions
You need rembg on your system to work the plug-in, a remove background tool.<br>
For Ubuntu users you can use pipx to install rembg.<br>
Pipx was the easiest way for me to get it working, you can use pip if you want.<br>
<br><br>
### Installing pipx and preparation
sudo apt update<br>
sudo apt install pipx<br>
pipx ensurepath<br>
<br><br>
### Installing rembg
// This is the most compatible version of rembg, although there are alternatives with CPU and GPU options.<br>
// Highly recommended to just use rembg[cli]<br>
pipx install "rembg[cli]"<br>
<br><br>
// Other option: CPU
// pipx install "rembg[cpu]" # for library<br>
// pipx install "rembg[cpu,cli]" # for library + cli<br>
<br><br>
// Other option: NVIDIA GPU
// pipx install "rembg[gpu]" # for library<br>
// pipx install "rembg[gpu,cli]" # for library + cli<br>
<br><br>
// Other option: AMD GPU
// pipx install "rembg[rocm]" # for library<br>
// pipx install "rembg[rocm,cli]" # for library + cli<br>
<br><br>
### Unzipping RemoveBG.py from .zip
Place your RemoveBG.py in<br>
/home/username/.config/GIMP/3.0/plug-ins/RemoveBG/<br>
<br><br>
To clarify there should be a subdirectory in /plug-ins/ called RemoveBG with the .py in it<br>
<br><br>
Set the .py to executable, right click -> Properties -> Permissions -> Allow this file to run as a program.<br>
Or...<br>
chmod +x /home/username/.config/GIMP/3.0/plug-ins/RemoveBG/RemoveBG.py<br>
<br><br>
### Editing RemoveBG.py
Open RemoveBG.py in a text editor and look for the line that says:<br>
aiExe = "/home/ryan/.local/share/pipx/venvs/rembg/bin/rembg"<br>
This was my path directly to rembg<br>
<br><br>
Change to your rembg path.<br>
<br><br>
Note this line is pointing to the executable rembg not the directory.
