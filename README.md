# Introduction 
Perform the following steps to install the Linux subsystem and run the Snowflake CSV uploader.

# WSL Installation and Git Configuration
1.	Install Ubuntu from Microsoft Store: https://www.microsoft.com/store/productId/9NBLGGH4MSV6
2.	Install Microsoft Terminal: https://www.microsoft.com/store/productId/9N0DX20HK701
3.  Search Start menu for "Turn Windows features on and off"
4.  Enable "Windows Subsystem for Linux" click OK and reboot when prompted:<br/>
![Enable WSL](readmeImages/EnableLinux.png =400x)
5.  Search for Ubuntu from Start menu and run to begin installation
6.  Enter Username and Password when prompted (won't change with LOL password updates)
7.  Close window after completion
8.  Open Windows Terminal
9.  Change default shell to Ubuntu:<br/>
![Settings Location](readmeImages/EnterSettings.jpg =400x)<br/>
![Default Shell](readmeImages/DefaultShell.jpg =400x)
10.  Open new terminal tab to activate Ubuntu shell
11.  Create SSH key for Git (Right click pastes clipboard to terminal):<br>`ssh-keygen -t rsa -b 4096`
12.  Press Enter for each prompt to use defaults (Do not enter password)
13.  Read public key data:<br>`cat ~/.ssh/id_rsa.pub`
14.  Select and copy all output to clipboard with `CTRL`+`Shift`+`C`
15.  Follow below images to add key to DevOps for repo cloning:<br/>
![Git SSH Settings](readmeImages/gitSSH.jpg =400x)<br/>
![Git Add SSH Key](readmeImages/gitAddKey.jpg =400x)

# CSV Uploader Setup
1.	Clone repo using following command:<br>`cd ~/ && git clone lolinc@vs-ssh.visualstudio.com:v3/lolinc/BusinessAnalytics/WU_Snowflake_Uploader`
2.	Run bash installer script, this will complete setup:<br>`cd ~/WU_Snowflake_Uploader && ./installer.sh`

# Running the Program
To use the program run `snow-csv`
-	To get the path of a CSV file, select it in Windows File Explorer and press `CTRL`+`C`. Paste into terminal when prompted with right click

# Updating to New Releases
Simply run `snow-update` and the newest version of the uploader will be retrieved and placed into `$PATH`
