# Asterisk Ansible Playbook

## Description

This is an [Ansible](https://www.ansible.com/) playbook for automatic installation of [Asterisk PBX](https://www.asterisk.org/) on [Ubuntu](https://ubuntu.com/).
I use Asterisk LTS (v20) and Ubuntu Server LTS (v22.04), but I'm pretty sure it's possible to install another version of Asterisk with little to no changes using this playbook.

## Usage

To install Asterisk on your Ubuntu server using this playbook, you need to:

- install Ansible (`brew install ansible` on macOS, `apt install ansible` on Ubuntu. Please check docs if you're using Windows — or just install Ansible into WSL)
- update variables (Asterisk version, number of CPU cores, etc.) in `playbook.yaml` if you need it
- add the IP addresses of your servers to `inventory.yaml`
- install Ansible "community.general" collection: `ansible-galaxy collection install community.general`
- run playbook this way: `ansible-playbook playbook.yaml -i inventory.yaml`

Once it's done, you'll have Asterisk PBX, Fail2Ban and FreePBX installed on your server.
If you don't need Fail2Ban or FreePBX, you can comment out the corresponding roles in `playbook.yaml`.

## Contact

In case of any questions, feel free to contact me by email: [soslanaldatov@gmail.com](mailto:soslanaldatov@gmail.com).
Also, feel free to contribute.
