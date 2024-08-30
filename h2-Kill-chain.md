# h2 - Kill chain

## Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains
-
-
-
-
-

# a) Installing VirtualBox and Debian 12-Bookworm Linux on it
## 1) I went to https://www.virtualbox.org/wiki/Downloads and clicked and installed "Windows hosts"

## 2) I opened the setup and clicked on "Next >" in order to start the setup procedure
![image](https://github.com/user-attachments/assets/1f5f2101-59b4-4cf1-b20a-668f3245ed01)

## 3) Again on "Next >" (if you don't want to change Location where its going to be downloaded, otherwise just continue)
![image](https://github.com/user-attachments/assets/f35daf8a-01b8-48b0-91be-00407512ec90)

## 4) Now on "Yes", this could temporarily disconnect you from the internet but don't worry :)
![image](https://github.com/user-attachments/assets/7e8de1f2-7f5c-401e-94c1-d9d2ec32783b)

## 5) Now I clicked on "Yes" because in order the VM to function some packages needed to be installed
![image](https://github.com/user-attachments/assets/14adab79-00c6-4e88-9c26-4d5a7a6f0ea6)

## 6) Here I unchecked the creation of an start menu, shortcut on desktop and in the quick launch bar and clicked on "Next >" because I don't like polluting my system with icons. I rather search things in the taskbar :)
![image](https://github.com/user-attachments/assets/a381f953-f5cc-48d8-b568-497361e49821)

## 7) Last but not least I clicked on "Install" to complete the setup
![image](https://github.com/user-attachments/assets/7b13bb7a-82de-4e78-bc1e-6d841a7169ea)

## 8) Finally I unchecked the option to start it right away and clicked on "Finish" because I wanted to install the ISO first and the open the VM
![image](https://github.com/user-attachments/assets/29650fba-a4ff-420e-a0fb-e1dc9335a45c)


## 9) Now I went to https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/ and searched for "debian-live-12.6.0-amd64-xfce.iso" and downloaded it (this is the ISO File aka Debian)

## 10) Now I opened VirtualBox and clicked on "New" 
![image](https://github.com/user-attachments/assets/e9f27f7e-494e-4ee4-bad8-292a0fc6c26a)

## 11) On the new window, below I clicked on "Expert Mode" in order to have more options
![image](https://github.com/user-attachments/assets/6927f9d7-2962-493a-8f5c-13c3de7a5113)

## 12) Then I entered the name "DebianTeroKarvinenCom", chose the ISO File and checked the box with "Skip Unattended Installation"
![image](https://github.com/user-attachments/assets/b9bd67b1-34c4-4db2-9f99-0f4848bb30a3)

## 13) On the same window, I opened the "Hardware" section and gave 4096MB (=4GB) of RAM and 2 CPU working Processors out of my 16
![image](https://github.com/user-attachments/assets/85168417-418d-42bd-b9ff-4f3627638563)

## 14) Still on this window I opened "Hard disk" and augmented the Hard disk Size to 60GB to give it more breathing room and finally clicked on "Finish"
![image](https://github.com/user-attachments/assets/d6ba20c1-af8b-42e9-a96f-dc3cb7e73d07)

## 15) Now the setup is finished and started it

## 16) This is what showed on first boot. Then selected "Live system (amd64)"
![image](https://github.com/user-attachments/assets/1e7a704b-db26-4e6d-80bf-3d0c695aff0c)

## 17) After a few minutes the desktop showed up and looked like this
![image](https://github.com/user-attachments/assets/d2ff77cf-4bbf-4dba-85b6-26c9555acd81)

# b) Voluntary Bonus: Update all software using "apt-get"
## 1) I opened the terminal terminator
![image](https://github.com/user-attachments/assets/fb0bcad9-00bd-4525-bba4-2b31eb356718)

## 2) I entered the following "sudo apt-get -y dist-upgrade" in the command line in order to update everything
![image](https://github.com/user-attachments/assets/4d801a0b-e968-490d-8279-281fa1072590)

## 3) After its done it looked like this:
![image](https://github.com/user-attachments/assets/51e623a0-d314-4208-8ec5-8200cbd44fc5)
