# Introduction 
Perform the following steps to install the Linux subsystem and Miniconda. Also set up your first conda environment with JupyterLab.

# WSL and Miniconda Installation
1.	Install Ubuntu from Microsoft Store: https://www.microsoft.com/store/productId/9NBLGGH4MSV6
2.	Install Microsoft Terminal: https://www.microsoft.com/store/productId/9N0DX20HK701
3.  Search Start menu for "Turn Windows features on and off"
4.  Enable "Windows Subsystem for Linux" click OK and reboot when prompted:<br/>
<img src="readmeImages/EnableLinux.png" width="400"><br/>
5.  Search for Ubuntu from Start menu and run to begin installation
6.  Enter Username and Password when prompted (won't change with LOL password updates)
7.  Close window after completion
8.  Open Windows Terminal
9.  Change default shell to Ubuntu:<br/>
<img src="readmeImages/EnterSettings.jpg" width="400"><br/>
<img src="readmeImages/DefaultShell.jpg" width="400"><br/>
10.  Open new terminal tab to activate Ubuntu shell.
11.  Run following command to download Miniconda installer:<br/>`wget https://repo.anaconda.com/miniconda/Miniconda3-py39_4.11.0-Linux-x86_64.sh -O install-miniconda.sh`
12.  Follow prompts and select defaults except for when the installer asks whether you'd like to initialize at the end. Select `Y`.
13.  Open a new terminal window to activate the base conda environment.
14.  Run the following command to install JupyterLab to your base environment:<br/>`conda install -c conda-forge jupyterlab nb_conda_kernels ipykernel`
15.  Create a new development environemt:<br/>`conda create -n YourEnvName ipykernel`
16.  Install development packages to your environment:<br/>`conda install -n YourEnvName pandas matplotlib`
17.  Launch JupyterLab server:<br/>`jupyter-lab`
18.  Navigate to http://localhost:8888/lab.
19.  Create a new notebook with an appropriate kernel from your environments.
