# roley-boiz
ansible roles

do the thing:
```
git clone https://github.com/insanitywholesale/roley-boiz && cd roley-boiz && vi roles/vfio-<distro>/defaults/main.yml (to change username and add vfio pci IDs) && ansible-playbook -i inventory playbook-vfio.yml -b -K && sudo reboot
```
profit???

PS: if debian, just comment out the other two, ansible version is too old there
