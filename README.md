# Ansible playbook for setup mariadb using podman on CentOS host

Tested on AWS LightSail instance with CentOS Stream 9 image

### How to run this playbook

1. Make sure you have ansible installed.
2. Clone this repository.
3. `cd` into the directory you just cloned.
4. Create `hosts.ini` file using `hosts.ini.example` file provided.
5. You may run `ansible <machine-name-in-host.ini> -m ping` first to test your connection to your machine.
6. If everything all set run the following command
```bash
ansible-playbook setup.yml
ansible-playbook podman.yml
```
7. Check if mariadb container you just create is running via `ansible <machine-name-in-host.ini> -a "podman ps"`
