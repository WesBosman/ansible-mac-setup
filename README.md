# ansible-mac-setup

I had to install an ext pack for Virtual Box because the VM had usb 3.0.

I ran `VBoxManage --version` in the terminal and found out I had version `6.18` so I downloaded the extension pack for that version of Virtual Box.

https://www.virtualbox.org/wiki/Download_Old_Builds_6_1


## Installation

Install the required Ansible roles.
```
ansible-galaxy install -r requirements.yml
```


## Testing
I included a vagrant file that builds a Mac OSX Mojave image for testing
to run it you have to run
```
vagrant up
```

If the machine is already running and you make changes to the machine and want to see the effects run
```
vagrant provision
```