# roley-boiz
ansible roles

do the thing:
git clone this repo, cd roley-boiz, edit roles/vfio-ubuntu/defaults/main.yml to change username, edit roles/vfio-ubuntu/files/grub to change gpu IDs, ansible-playbook -i inventory playbook-vfio.yml -b -K, sudo reboot
