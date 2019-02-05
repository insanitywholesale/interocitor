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

1. clone this repository anywhere you want
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

- if you're running debian stretch or older, just comment out the rest, the ansible version in the repos is too old. installing ansible using pip does work but you're introducing a package that is being handled by pip and not the actual package manager. this is a solution that does work but it's up to you to decide if you want to comment out a few lines or install using pip.
- fedora is a but weird and if you don't install the two additional packages listed above, it doesn't work. in addition, since python isn't there, ansible can't run anything so I can't even added to the required packages list. if you have a fix, feel free to share it.
- the case of identical gpus is not supported at the moment. same goes for vbios dumping and patching.
