# Ansible role: eriklotin.docker
This role installs Docker and does some post-install tasks to prepare hosts for running Docker containers.

# Install
```
ansible-galaxy install eriklotin.docker
```
or install locally:
```yaml
ansible-galaxy install eriklotin.docker -p ./roles/
```

# Variables

List of system users which will be added to docker system group.
```yaml
docker_users: []
```

# Example playbook

```yaml
- hosts: all

  vars:
    - docker_users: ["ubuntu"]

  roles:
    - role: eriklotin.docker
      become: true
```

# Dependencies

This role uses [geerlingguy.docker](https://github.com/geerlingguy/ansible-role-docker) role to install Docker.


# License
MIT. See `LICENSE` file.

# Author
Created in 2019-02 by [Erik Lotin](https://github.com/eriklotin).