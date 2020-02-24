# rpi_torrent_ansible
Playbook that sets up a raspberry pi with transmission, mullvadvpn, and changes administrator password

### Pre-requisites
Ansible should be installed on your system
Sshpass should be installed on your system if you are planning on using the `ansible_ssh_pass=PASSWORD` field within the `hosts` file
If you are planning on copying over your public ssh key into the `authorized_keys` files for you raspberry pi please place your `id_rsa.pub` in the `templates/` folder
This playbook was developed for my own purposes and assumes you will be using `MullvadVPN` as your vpn provider. You will need to generate your own configuration files from `Mullvadvpn` and place those in a folder called `mullvad/` 
If you wish to use a different vpn provider you will have to find setup instructions from your provider's website and alter the playbook accordingly

### Runing the playbook
`ansible-playbook playbook.yml -i hosts`