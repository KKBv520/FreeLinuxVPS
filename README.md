# FreeLinuxVPS
Get Free Linux VPS With GPU + 12 GB Ram ! With Colab! This Server will working 12 hours If you have Colab Pro Its will Working More Times !

**INFO**

RAM : 12 GB
GPU : YES
GAME AND DEVELOPING: YES
UNLIMITED TIME : NO
DURATION: 12 HOURS (IF YOU HAVE COLAB PRO IS MORE)
Always Access ? : YES

**THIS COLAB MADE BY KKBv520**

Good Luck 👍 

**Please Follow me On Github AND Give Star To This repository Thanks!**

**IF OUR VERSION IS NOT WORKING READ THIS**

**SETP 1** - Copy This Into Colab
` ` `!sudo apt update
!sudo apt install libcairo2-dev ffmpeg texlive texlive-latex-extra texlive-fonts-extra texlive-latex-recommended texlive-science tipa libpango1.0-dev
!pip install manim
!pip install IPython --upgrade` ` `
**SETP 2** - After Copying this make new 
Not book In colab Then Make New code Also
Change Runtime TO GPU 
**SETP 2** - Copy This Into Colab
` ` `from manim import *` ` `
**SETP 3**  - Copy this into Colab ( If You want GPU Also You Need Change Runtime To GPU)
` ` `#@title **GPU T4 INSTALLING**
gpu_info = ! nvidia-smi
gpu_info = '\n'.join(gpu_info)
if gpu_info.find('V100-PCIE...') >=0:
  print(gpu_info)
  exit()
else :
  print(gpu_info)` ` `
**SETP 4** - Copy This Into Colab
` ` `#@title **STEP 4 CREATE USER**
 
import os
 
username = "user" #@param {type:"string"}
password = "root" #@param {type:"string"}
 
print("Creating User and Setting it up")
 
# Creation of user
os.system(f"useradd -m {username}")
 
# Add user to sudo group
os.system(f"adduser {username} sudo")
    
# Set password of user to 'root'
os.system(f"echo '{username}:{password}' | sudo chpasswd")
 
# Change default shell from sh to bash
os.system("sed -i 's/\/bin\/sh/\/bin\/bash/g' /etc/passwd")
 
print("User Created and Configured")` ` `
**SETP 5** - Copy into colab
` ` `#@title **INSTALL YOUR VPS BY KKB**
#@markdown  It takes 4-5 minutes for installation
 
import os
import subprocess
 
#@markdown  Visit http://remotedesktop.google.com/headless and Copy the command after authentication
 
CRP = "" #@param {type:"string"}
 
#@markdown Enter a pin more or equal to 6 digits
Pin = 123456 #@param {type: "integer"}
 
 
class CRD:
    def __init__(self):
        os.system("apt update")
        self.installCRD()
        self.installDesktopEnvironment()
        self.installGoogleChorme()
        self.finish()
 
    @staticmethod
    def installCRD():
        print("Installing Chrome Remote Desktop")
        subprocess.run(['wget', 'https://dl.google.com/linux/direct/chrome-remote-desktop_current_amd64.deb'], stdout=subprocess.PIPE)
        subprocess.run(['dpkg', '--install', 'chrome-remote-desktop_current_amd64.deb'], stdout=subprocess.PIPE)
        subprocess.run(['apt', 'install', '--assume-yes', '--fix-broken'], stdout=subprocess.PIPE)
 
    @staticmethod
    def installDesktopEnvironment():
        print("Installing Desktop Environment")
        os.system("export DEBIAN_FRONTEND=noninteractive")
        os.system("apt install --assume-yes xfce4 desktop-base xfce4-terminal")
        os.system("bash -c 'echo \"exec /etc/X11/Xsession /usr/bin/xfce4-session\" > /etc/chrome-remote-desktop-session'")
        os.system("apt remove --assume-yes gnome-terminal")
        os.system("apt install --assume-yes xscreensaver")
        os.system("systemctl disable lightdm.service")
 
    @staticmethod
    def installGoogleChorme():
        print("Installing Google Chrome")
        subprocess.run(["wget", "https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb"], stdout=subprocess.PIPE)
        subprocess.run(["dpkg", "--install", "google-chrome-stable_current_amd64.deb"], stdout=subprocess.PIPE)
        subprocess.run(['apt', 'install', '--assume-yes', '--fix-broken'], stdout=subprocess.PIPE)
 
    @staticmethod
    def finish():
        print("Finalizing")
        os.system(f"adduser {username} chrome-remote-desktop")
        command = f"{CRP} --pin={Pin}"
        os.system(f"su - {username} -c '{command}'")
        os.system("service chrome-remote-desktop start")
        print("Finished Succesfully")
 
 
try:
    if username:
        if CRP == "":
            print("Please enter authcode from the given link")
        elif len(str(Pin)) < 6:
            print("Enter a pin more or equal to 6 digits")
        else:
            CRD()
except NameError as e:
    print("username variable not found")
    print("Create a User First")` ` `
SETP 6 - AUTO ALIVE
#@title **MAKE ALIVE VPS 24 HOURS** 
 
alive = False #@param {type:'boolean'}
 
! sleep 999999



**YOU CAN DOWNLOAD OUR CODE IN GITHUB**
