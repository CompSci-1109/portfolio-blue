
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
