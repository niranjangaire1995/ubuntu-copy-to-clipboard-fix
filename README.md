# ubuntu-copy-to-clipboard-fix
Fix for Ubuntu copy to clipboard not working

No Bs straight to the point. Install Guest Edition CD that will fix the issue.
1. sudo apt update               //this command gives the list of upgradables.
2. <img width="849" height="358" alt="Screenshot 2026-04-08 214520" src="https://github.com/user-attachments/assets/10039752-2632-488c-93d2-2810a2a02a4c" />

3. sudo apt install build-essential dkms linux-headers-$(uname -r)     #This installs required files
4. VM Top Bar -> Devies -> Insert Guest additions CD Image -> You will see the CD icon 
5. <img width="209" height="547" alt="image" src="https://github.com/user-attachments/assets/aa14d206-72a8-4435-ae45-1016cb755cf0" />
Make sure this is also enabled -> bidirectional.
<img width="667" height="420" alt="image" src="https://github.com/user-attachments/assets/ed1c278f-2798-4a0a-a57e-af6300eed33b" />

also do the command lsmod | grep vbox the result should show vboxguest, vboxvideo, vboxsf. if sf is not there, the clipboard is not activated or the guest edition is not propelry installed.
VBoxClient --clipboard or VBoxClient --draganddrop will fix it. But I will install the guest edition.
<img width="807" height="513" alt="image" src="https://github.com/user-attachments/assets/af0b2284-4662-4641-8626-988e86f0dfe3" />

6. Move to CD directory -> cd /media and open one of the files (VBox_GAs_7.2.6  VBox_GAs_7.2.61  VBox_GAs_7.2.62). Its usually the last one VBox_GAs_7.2.62 one.
7. do this -> sudo sh VBoxLinuxAdditions.run
8. It will take forever to install and restart the system
9. The copy paste will now.
