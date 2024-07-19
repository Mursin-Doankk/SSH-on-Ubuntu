# SSH-on-Ubuntu
Enable SSH on Ubuntu


# 1. To install SSH, first update the package repository cache with:
```
sudo apt-get update
```
# 2. Now install the OpenSSH software package by entering:
```
sudo apt-get install openssh-server
```
sudo apt-get install openssh-server terminal output
If prompted, type in your password and press y (yes) to permit the installation.

# 3. To verify the installation was successful and SSH is running use the command:
```
sudo service ssh status
```
sudo service ssh status terminal output
The confirmation message that you are looking for is: Active: active (running).

This means you have installed and enabled SSH on your remote machine, which can now accept commands from your SSH client.

6. To return to the command line prompt enter q.

Log Into Remote Server With SSH
Once you have gone through the process of enabling SSH on Ubuntu, you are ready to log into your remote machine.

1. Open the terminal (CTRL+ALT+T) and type the following command:

ssh username@public_IP -p22

ssh port 22 local terminal output
Change the username and IP address to the username and IP address of the Ubuntu computer on which you have installed SSH.

2. If you do not know the IP address, you can quickly identify it through the terminal by typing the command:

ip a

ip a terminal output
This displays the public IP address of the machine where SSH was installed.

Once you have identified and typed in all the information, you are officially logged into the server. You are free to manage it from the comfort of your workstation safely.

Note: Read more about secure remote access to implement and enforce the best practices for employees.

SSH Configuration Options
The default SSH configuration options can be adjusted. You can change the default port (generally a good idea, as a precautionary security measure), disable the root user, or make other configuration adjustments.

Edit Configuration File
After successfully installing OpenSSH on Ubuntu, you can edit its configuration file.

1. Open the SSH configuration file with the command:

sudo nano /etc/ssh/sshd_config

2. Now that you have opened the file using nano (or with any Linux text editor) find and make any necessary changes.

For example, to change the port number to listen on TCP port 2222 instead of the default TCP port 22, find the line in which Port 22 is specified by default, uncomment the line, and change it to Port 2222.

port 2222 sshd_config file contents
