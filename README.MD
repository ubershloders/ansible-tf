# OpenTTD Ansible Playbook

This repository contains an Ansible playbook for installing and configuring OpenTTD, a popular open-source transport simulation game, on Ubuntu 24.04. This playbook also sets up OpenTTD as a dedicated server with the necessary graphics and sound packs.

## Prerequisites

- **Ansible**: Ensure Ansible is installed on your local machine. You can install Ansible via pip or your operating system's package manager.
- **Target Server**: A running Ubuntu 24.04 server.
- **SSH Access**: SSH access to the target server with a user who has `sudo` privileges.

## Installation Steps

1. **Clone the Repository**

   Clone this repository to your local machine:

   ```sh
   git clone https://github.com/ubershloders/ansible-tf.git
   cd openttd-ansible
Prepare the Inventory File

Create or edit the inventory.ini file to include your server details. Example:
```
[servers]
your_server_ip_or_hostname ansible_ssh_user=your_user
Prepare the Configuration File
```
Place your openttd.cfg file in the same directory as the playbook. This file will be copied to the target server.

## Run the Playbook

Execute the playbook using the following command:

ansible-playbook -i inventory.ini install_openttd.yml
Playbook Overview
The playbook performs the following actions:

### Configuration
openttd.cfg: Customize this file according to your server's requirements. For detailed configuration options, refer to the OpenTTD Configuration Documentation.
### License
This project is licensed under the MIT License. See the LICENSE file for more details.

### Contributing
Feel free to fork the repository, make changes, and submit pull requests. Contributions are welcome!
