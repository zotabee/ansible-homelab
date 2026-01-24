# ansible-homelab
Ansible playbooks for managing my homelab

## Required base project
Companion project of [Pro-Tweaker/SEEDbox](https://github.com/Pro-Tweaker/SEEDbox/)

## Getting Started (Debian distrib)

Install git, python, pip, ansible, ansible-lint and yamllint:

```bash
sudo apt install git python3 pip ansible ansible-lint yamllint
```

Clone the repo:

```bash
git clone https://github.com/zotabee/ansible-homelab.git
cd ansible-homelab/
```

Run Ansible playbook:

```bash
sudo ansible-playbook ansible-homelab.yml
sudo ansible-playbook ansible-homelab.yml --tags=homebox
```

## Testing and linting
All Ansible playbooks and yaml files are checked and fully linted through:

| Command  | Passed |
| ------------- | ------------- |
| yamlint  | ✅  |
| ansible-playbook --syntax-check  | ✅  |
| ansible-lint (production level) | ✅  |
| ansible-playbook --check (against prod)  | ✅  |

Linting commands:

```bash
# yamllint
yamllint --list-files .
yamllint .

# ansible-playbook --syntax-check
ansible-playbook ansible-homelab.yml --syntax-check

# ansible-lint (production level)
ansible-lint

# ansible-playbook --check (against prod)
ansible-playbook ansible-homelab.yml --check
```

## Credits
Project inspired by:

[Dylancyclone/ansible-homelab-orchestration](https://github.com/Dylancyclone/ansible-homelab-orchestration)

[saltyorg/Saltbox](https://github.com/saltyorg/Saltbox)

[Cloudbox/Cloudbox](https://github.com/Cloudbox/Cloudbox)

[Jeff Geerling aka geerlingguy](https://github.com/geerlingguy)

[Ansible for DevOps (Jeff's book)](https://github.com/geerlingguy/ansible-for-devops)