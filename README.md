# Find The Malicious User

Download the following [virtual machine with Ubuntu Server](https://storage.googleapis.com/breathecode/virtualbox/Ubuntu-Server-Find-Malicious-User.ova) and run the computer in Virtual Box on your computer.

You have just joined the cybersecurity team at 4Geeks Academy. The team is currently setting up a web server with Ubuntu for the E-Learning platform. This team consists of:

1. Alejandro
2. Daniela
3. Vanessa
4. Chema
5. Analista (You)

Your username and password are:

```bash
username: analista
password: analista
```

Each user has their own directories and files, as well as some shared ones, with different permissions on the shared files. One of these users has permissions they shouldn't have and seems to be up to something. Can you discover who it is?

1. Identify the malicious user
2. Analyze their actions and explain what they were attempting to do
3. Determine what permissions they had and on which directories that allowed them to execute this action
4. Propose a solution to this problem

> ⚠️ The Sticky bit permission (rwx-t) is often used to grant selective access to files and directories.


## 💡 HELP

- The Ubuntu machine we've designed for you doesn't have a graphical interface because, in addition to testing your hacking skills, we also want to test your command-line skills.
- The main directory system where you'll be actively investigating is as follows:

```bash
|- home
    |-alejandro
    |-analista
    |-chema
    |-daniela
    |-vanessa
    |-vboxuser
```
> ⚠️ Upon logging in, you will be positioned in the ./analista directory.

- The first instructions can be found in the ./home directory.
