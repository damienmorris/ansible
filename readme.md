# Prerequisites

1. Install `pipx`:
```bash
sudo apt update
sudo apt install pipx
pipx ensurepath
sudo pipx ensurepath --global # optional to allow pipx actions with --global argument
```

2. Install Ansible:
```bash
pipx install --include-deps ansible
```

# Playbook: `ubuntu-local`

1. Install dependencies:
```bash
pipx inject ansible python-debian
```

2. Run playbook
```
ansible-playbook -u <username> --ask-become-pass ubuntu-local.yaml
```
