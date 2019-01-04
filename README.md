# Interocitor

ansible role for vfio setup automation


## Installation

In order to use this role, git and ansible need to be installed (this depends on your distribution).


### Debian

```
sudo apt install git ansible
```

### Ubuntu

```
sudo apt install git ansible
```

### Fedora

```
sudo dnf install git ansible python libselinux-python
```

### Arch

```
sudo pacman -S git ansible
```


## Using the Interocitor

1. clone this repository
- ```git clone https://github.com/insanitywholesale/interocitor```
2. go into it
- ```cd interocitor```
3. edit the variables (username and grub_kernel_options) in defaults/main.yml for your distro
- ```vi roles/vfio-arch/defaults/main.yml```
4. run the thing
- ```ansible-playbook -i inventory interocitor.yml -b -K```
5. reboot
- ```sudo reboot```


#### Additional Notes

- if you're running debian, just comment out the rest, the ansible version in the repos is too old. installing ansible using pip might work but it hasn't been tested.
- fedora is a but weird and if you don't install the two additional packages listed above, it doesn't work. in addition, since python isn't there, ansible can't run anything so I can't even added to the required packages list. if you have a fix, feel free to share it.
- arch support is experimental right now (should theoretically work) hasn't been tested like the rest of the distros so until this warning is removed, don't complain about it.
