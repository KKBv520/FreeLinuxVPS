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
