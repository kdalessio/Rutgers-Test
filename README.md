Anaconda Environment Setup


This guide walks through the installation and configuration process for an Anaconda environment. This guide includes the following:

Download and installation of Anaconda distribution for Python 3

Configuration of Anaconda dev virtual environment

Activation of Anaconda dev environment

Installation of JupyterLab

VERY IMPORTANT: Anaconda downloads the Python 3.8 distribution by default, however - we will create and use a virtual environment that utilizes Python 3.7 instead, as many of our activities are not yet compatible with the new Python 3.8 version. It is imperative that you create the virtual environment as indicated and activate it prior to running your code.

Download and Install Anaconda
Navigate to the Anaconda installation documentation. It will be valuable to have the documentation available in case any issues arise.

LP_Ins_Intro_to_Jupyter_Lab_Installation

Navigate to the Anaconda download site, which can be found here. Click the download button as seen in the below image:

Anaconda_Download_1

This will automatically move your screen to to the download section of the page. Select the appropriate distribution for your system.

Anaconda_Download_2

You will be asked to save the installer. Save it. After the download is complete, run the download file. This will launch an installation wizard that will walk you through the Anaconda install. Continue through the installation process by clicking either "I Agree" or "Next."

Jupyter_Lab_Start.png

You will eventually get to a screen that asks if you would like to set your PATH environment variable using the installation wizard. Do NOT check this box. Make sure that both boxes are unchecked, as displayed in the below screenshot. Click install.

Jupyter_Lab_Path.png

Click Finish once the installation is complete.

Next, open the terminal (Mac) or Git Bash (Windows).

Mac users can find the terminal by opening their Spotlight Search and typing Terminal.

Windows users can open Git Bash by locating it in their Start Menu:

Jupyter_Lab_Launch_Terminal.png
Execute the following commands to ensure the latest Anaconda packages are installed. When prompted, enter "y" to proceed.

conda update conda
conda update anaconda
Jupyter_Lab_Conda_Update.png
Create a dev environment. When prompted, enter "y" to proceed.

conda create -n dev python=3.7 anaconda
Jupyter_Lab_Dev_Env.png

Activate the dev environment.

conda activate dev
Jupyter_Lab_Activate_Dev.png
Verify your your installations by executing the conda list command after activating the environment, then locating the following packages in the populated list:

Numpy
Pandas
Matplotlib
After the installation of Anaconda, we'll want to enable the terminal commands. The instructions differ by your operating system.

Windows. After these instructions, you need to open your terminal and run conda init bash. Then close your terminal, and start a new one before using any jupyter command.
In windows, if you are receiving an error about a "DLL not having an entry point" you most likely have an environmental variable missing. Make sure that you additionally have the \bin subdirectory within your anaconda3 directory added as a path in your environmental variables.

Mac. Versions of MacOS 10.15 and beyond (Catalina) will need to run conda init zsh in the terminal after these steps. Versions below 10.15 will need to run conda init bash instead.
Additionally for Mac, your installation may have been placed in the folder /opt/anaconda3/bin instead of your user directory. You will need to change the instructions from the above video for the .zshrc file to instead be $PATH:/opt/anaconda3/bin rather than the PATH with your user directory.

A few other things to look out for during the post-installation:

Note that the exact location where your Anaconda folder is installed may differ based upon your operating system, version of operating system, and version of Anaconda. It is not uncommon to need to search for the "anaconda3" directory on your machine.

If you're having trouble locating the installation directory for Anaconda, try right-clicking the shortcut for anaconda-navigator and going to Properties (Windows) or Get Info (MacOS). The shourtcut should have a reference to the directory containing Anaconda.

If you're using a Windows machine, and running jupyter-lab . creates an error involving "can't find jupyter module", make sure that you have gone through the steps for conda init bash.

DON'T FORGET: Anaconda downloads the Python 3.8 distribution by default, however - many of our activities are not yet compatible with the new Python 3.8 version. It is therefor imperative that you create the virtual environment as indicated using the python=3.7 parameter and activate it prior to running your code. The command to activate your virtual environment is conda activate dev.
