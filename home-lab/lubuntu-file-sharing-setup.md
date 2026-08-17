
# Setting up VirtualBox Guest additions in Lubuntu (and some unexpected problems)

## Objective:

To set up VirtualBox Guest Additions , so as to enable:

* Shared Clipboard
* Drag-n-Drop of files from host to guest and vice versa
* Shared Folders (to ensure easy access of files in host machine from guest machine) [status: PLANNED]

  # 🖥️ Lab Environment

| Component           | Version                      |
| ------------------- | ---------------------------- |
| Host OS             | Windows 11                   |
| VirtualBox          | 7.2.8                        |
| Guest OS            | Lubuntu 26.04 LTS (Resolute) |
| Desktop Environment | LXQt                         |
| Graphics Controller | VMSVGA                       |
| Video Memory        | 128 MB                       |


# What I did:
1. Went to settings whilst VM was powered off. Checked if Shared Clipboard and Drag-n-Drop are enabled and set to Bidirectional.
2. Checked if Clipboard daemon is running.

Command:

`VBoxClient --clipboard`

output: command vboxclient not found

To check version , I ran:

`VBoxControl --version`


output: it said VBoxControl not found. 


3. Checked if VirtualBox Guest Additions were installed.

`lsmod | grep vboxguest`

its output indicated that guest additions were installed on Lubuntu.

4.  I later ran :

`sudo apt install virtualbox-guest-utils` 


btw this command appeared on the terminal as Linux was asking "did you mean this command?" after it said that VBoxControl wasn't installed.


5. Post- Installation, it showed a list of suggested packages, which included "virtualbox-guest-x11". So I decided to install it, by running:

`sudo apt install virtualbox-guest-x11`


and then I rebooted the machine, using:

`sudo reboot`.



I thought this would go all normally. But it seems that day was prepared for a sidequest.

I observed that the GUI didn't appear as it normally does after a reboot.

and I thought it was over 😭😭😭😭.


I searched for some way and then I logged in through CLI.

I clicked the shortcut Ctrl + Alt + F4 (in my laptop, this shortcut helps me to move to the text console).

it showed 

chandu login: 

after logging in with username and password, I reached the text console. then, I typed:

`systemctl status display-manager`


this command shows the services or processes which are running.


<img width="1536" height="1152" alt="image" src="https://github.com/user-attachments/assets/4c58662d-276d-4782-8e65-e29230cad1d9" />



this is the image after I ran the systemctl command. It showed that 

sddm.service is running, auth was successful, it did start the x11 session and the Lubuntu Desktop. 

but if the LXQT desktop was started , why is the GUI not appearing?!!!


<img width="1536" height="1152" alt="image" src="https://github.com/user-attachments/assets/4f7983c8-908b-441c-aa2b-692a064abea2" />


"Could not load the Qt platform plugin "xcb"
xcb-cursor0 or libxcb-cursor0 is needed to load the Qt xcb platform plugin."




