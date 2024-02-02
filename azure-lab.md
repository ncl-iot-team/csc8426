# Azure lab instructions

## Accessing the remote machine

Login to the azure lab with the following credentials:

Username: student
Password: CSC8426!

## Using the virtual machine within Azure lab


1. Open Hyper-V manager from the desktop
2. Connect to the virtual machine named "Edge", ignore the "Cloud" virtual machine
3. Select settings
4. On the processor tab, change the number of cores to 4. And apply the settings
6. Press start to start the machine
7. For the login screen, use the following credentials:
    * Username: student
    * Password: CSC8112!
    * We recommend you to change the password after the first login. You can do this by opening the terminal and running the command `passwd`

## Additonal software to install

* htop: `sudo apt install htop`
    * htop is a process viewer to monitor your system simliar to the task manager in Windows
    * It's not for monitoring a Docker swarm however
* Java Development Kit: `sudo apt install default-jdk`
    * For running/building Java applications
* IntelliJ IDEA: `sudo snap install intellij-idea-community --classic`
    * An IDE for Java development
