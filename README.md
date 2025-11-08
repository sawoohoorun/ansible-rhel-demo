# Ansible RHEL Demo Project

This is an Ansible project for managing RHEL (Red Hat Enterprise Linux) servers.

## Project Structure

```
.
├── ansible.cfg          # Ansible configuration file
├── inventory/           # Inventory files
│   ├── hosts.yml        # Main inventory file
│   ├── group_vars/      # Group variables (alternative location)
│   └── host_vars/       # Host variables (alternative location)
├── group_vars/          # Group variables
│   ├── all.yml          # Variables for all hosts
│   └── rhel_servers.yml # Variables for RHEL servers
├── host_vars/           # Host-specific variables
├── roles/               # Ansible roles
├── playbooks/           # Playbook files
│   └── site.yml        # Main playbook
├── files/               # Static files to be copied
├── templates/           # Jinja2 templates
├── vars/                # Variable files
└── tasks/               # Standalone task files
```

## Usage

1. Update the inventory file (`inventory/hosts.yml`) with your actual hosts
2. Configure variables in `group_vars/` and `host_vars/` as needed
3. Create or modify playbooks in `playbooks/`
4. Run playbooks:
   ```bash
   ansible-playbook playbooks/site.yml
   ```

## Inventory

The inventory file is located at `inventory/hosts.yml`. Update it with your actual server information.

## Variables

- Group variables: `group_vars/`
- Host variables: `host_vars/`
- Variables can also be placed in `inventory/group_vars/` and `inventory/host_vars/`

## Roles

Create reusable roles in the `roles/` directory. Each role should follow the standard Ansible role structure:
- `tasks/main.yml`
- `handlers/main.yml`
- `templates/`
- `files/`
- `vars/main.yml`
- `defaults/main.yml`
- `meta/main.yml`

