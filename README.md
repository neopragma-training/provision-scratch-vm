# provision-scratch-vm

Provision an instance of Ubuntu Linux to support Scratch for a training course or workshop for non-technical people to learn a little about programming and about lightweight software development methods. Once you have a provisioned VM, you can clone git repositories for one or more sample projects designed for use in training classes. These instructions are used by an instructor preparing a VM to be copied and distributed to participants in a training class.

## Steps

The instructions assume you will provision a virtual machine with Ubuntu Linux. This has been tested with the following operating systems:

* Ubuntu Desktop 14.04 LTS 32-bit

### Step 1 - Download Ubuntu iso

Open a browser and navigate to http://www.ubuntu.com. Download the iso for a 32-bit version of Ubuntu Desktop. As this is written, the Scratch 2.0 offline editor does not work with 64-bit Linux.

### Step 2 - Create VM

Using the virtualization product you want your students to use, create a VM and install Ubuntu on it. This procedure has been tested with the following virtualization products:

* VMware Player 6.0.1 Linux 64-bit
* VMware Player 6.0.2 Linux 64-bit
* VMware Player 6.0.1 Windows 8.1 64-bit
* VMware Player 6.0.2 Windows 8.1 64-bit

### Step 3 - Apply system updates

Start the VM and ensure it has a connection to the Internet. Apply any available system updates. Use the Software Updater icon that appears in the Unity launcher or open a Terminal and apply updates using the command line:

```shell
sudo apt-get -y -f update
sudo apt-get -y -f dist-upgrade
```

### Step 4 - Install git

 Install git.

```shell
sudo apt-get -y -f install git
```

### Step 5 - Clone this repo

With git installed, you can load this provisioning project on the new instance:

```shell
cd
git clone https://github.com/neopragma/provision-scratch-vm
```

### Step 6 - Run the setup script

Run the setup script.

```shell
cd ~/provision-scratch-vm
./setup
```

### Step 7 - Verify the setup

The last thing the setup script does is to run a script named verify. Check the output from verify and see if any of the installation steps failed. If so, investigate and resolve the problems. If you discover a problem with the setup script, fix it and make a pull request.

### Step 8 - Install course-specific project(s)

At this point, the VM is ready to support Scratch workshops available from Neo Pragma LLC Github repositories, or any other Scratch activities you care to facilitate.






