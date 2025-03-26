# Provisioning the Technologies

This directory shows how to provision the NAT network being used for this project, as well as how to provision the virtual machines and adding guest additions.

## Table of Contents

* NAT Network
* Virtual Machines
* Guest Additions
  - Windows
  - Linux

***

# NAT Network
> Check the Project Overview section for more IPv4 details

#### Step 1: File > Tools > Network Manager

[PLACE PHOTO PATH HERE]: #

#### Step 2: NAT Networks > "Create"

[PLACE PHOTO PATH HERE]: #

#### Step 3: Select a name for your network. For this project, it will be called "lab-network", then choose an IPv4 prefix, "Apply"

[PLACE PHOTO PATH HERE]: #

### ***NOTE: Each new virtual machine provisioned should have this network selected***

***

# Virtual Machines
> For each machine's hardware specifications, check out the Project Overview section

#### Step 1: Machine > New

[PLACE PHOTO PATH HERE]: #

#### Step 2: Choose a name for your machine > Select the "Type" (Windows, Ubuntu, etc.) > Select the "Version" (note the version of each of the ISO images)

[PLACE PHOTO PATH HERE]: #

#### Step 3: Add harware specifications (Refer to Project Overview for specifications) > For Windows, Enable EFI

[PLACE PHOTO PATH HERE]: #

#### Step 4: Review specifications > "Finish"

[PLACE PHOTO PATH HERE]: #

#### Step 5: Select the new machine > "Settings"

[PLACE PHOTO PATH HERE]: #

#### Step 6: Storage > Click "Empty" > "Choose a disk file..."

[PLACE PHOTO PATH HERE]: #

#### Step 7: Navigate to where the ISO images are installed > Select the proper ISO > "Open"

[PLACE PHOTO PATH HERE]: #

#### Step 8: Network > Select "NAT Network" in the "Attached to:" dropdown > Choose your NAT network > "OK"

[PLACE PHOTO PATH HERE]: #

#### Step 9: Start the machine

[PLACE PHOTO PATH HERE]: #

#### Step 10: When propmted, hit any key on the keyboard

[PLACE PHOTO PATH HERE]: #

#### Step 11: Take a Snapshot

[PLACE PHOTO PATH HERE]: #

***

# Guest Additions
> Guest additions allow extra functionality and allow the user to interact with VirtualBox instead of the machines. It also allows for the machines to be in full screen instead of the windowed view.

## Windows
#### Step 1: With the machine running, navigate to the menu bar > Devices > "Insert Guest Additions CD image..."

[PLACE PHOTO PATH HERE]: #

#### Step 2: Navigate to "File Explorer" > "This PC" > "VirtualBox Guest Additions" > "VBoxWindowsAdditions" > Follow the default installation > "Reboot Now"

[PLACE PHOTO PATH HERE]: #
[PLACE PHOTO PATH HERE]: #
[PLACE PHOTO PATH HERE]: #

#### Step 3: Allow the virtual machine to restart. Full screen should be enabled now

## Linux
#### Step 1: With the machine running, navigate to the menu bar > Devices > "Insert Guest Additions CD image..."

[PLACE PHOTO PATH HERE]: #

#### Step 2: Select the new CD disk image that appears on the tool bar

[PLACE PHOTO PATH HERE]: #

#### Step 3: Right click the whitespace > "Open in Terminal"

[PLACE PHOTO PATH HERE]: #

#### Step 4: Type the following command:
'sudo ./VboxLinuxAdditions.run'
#### Type the user's password

[PLACE PHOTO PATH HERE]: #


