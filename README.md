# RemoveBG-ENG
A fork of a great Remove Background AI tool using rembg by JamesH
This is for GIMP 3.0+ Flatpak version

## Instructions
You need rembg on your system to work the plug-in, a remove background tool.
For Ubuntu users you can use pipx to install rembg.
Pipx was the easiest way for me to get it working, you can use pip if you want.

### Installing pipx and preparation
sudo apt update
sudo apt install pipx
pipx ensurepath

### Installing rembg
// This is the most compatible version of rembg, although there are alternatives with CPU and GPU options.
// Highly recommended to just use rembg[cli]
pipx install "rembg[cli]"

// Other option: CPU
// pipx install "rembg[cpu]" # for library
// pipx install "rembg[cpu,cli]" # for library + cli

// Other option: NVIDIA GPU
// pipx install "rembg[gpu]" # for library
// pipx install "rembg[gpu,cli]" # for library + cli

// Other option: AMD GPU
// pipx install "rembg[rocm]" # for library
// pipx install "rembg[rocm,cli]" # for library + cli

### Unzipping RemoveBG.py from .zip
Place your RemoveBG.py in
/home/username/.config/GIMP/3.0/plug-ins/RemoveBG/

To clarify there should be a subdirectory in /plug-ins/ called RemoveBG with the .py in it

Set the .py to executable, right click -> Properties -> Permissions -> Allow this file to run as a program.
Or...
chmod +x /home/username/.config/GIMP/3.0/plug-ins/RemoveBG/RemoveBG.py

### Editing RemoveBG.py
Open RemoveBG.py in a text editor and look for the line that says:
aiExe = "/home/ryan/.local/share/pipx/venvs/rembg/bin/rembg"
This was my path directly to rembg

Change to your rembg path.

Note this line is pointing to the executable rembg not the directory.
