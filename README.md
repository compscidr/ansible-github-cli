# ansible-github-cli
[![Static Badge](https://img.shields.io/badge/Ansible_galaxy-Download-blue)](https://galaxy.ansible.com/ui/repo/published/compscidr/github_cli/)
[![ansible lint](https://github.com/compscidr/ansible-github-cli/actions/workflows/check.yml/badge.svg)](https://github.com/compscidr/ansible-github-cli/actions/workflows/check.yml)
[![ansible lint rules](https://img.shields.io/badge/Ansible--lint-rules%20table-blue.svg)](https://ansible.readthedocs.io/projects/lint/rules/)

A collection of roles to:
- install github cli
- install gh extensions

## Usage
Add the collection to your meta/requirements.yml:
```
collections:
  - name: compscidr.github_cli
    version: "<insert version here>"
```

Install the collection:
```
ansible-galaxy install -r meta/requirements.yml
```

Use in a playbook:
```
- name: Install GH cli and extensions
  hosts: *
  roles:
    - role: compscidr.github_cli.github_cli
      vars:
        github_cli_gh_token: "insert your gh token"
        github_cli_user: "insert your username"
    - role: compscidr.github_cli.github_cli_extension
      vars:
        github_cli_extension: "dlvhdr/gh-dash"
    - role: compscidr.github_cli.github_cli_extension
      vars:
        github_cli_extension: "some other extension"
```

## Variables
Variable                                | Description
--------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
github_cli_gh_token                     | The GH API token that allows for reading / writing to repos
github_cli_user                         | The user to add the GH_TOKEN as env variable for (will append to .bashrc file)
github_cli_extension                    | The extension to install

## Local development and testing
So that you don't need to push and make a release every time:
```
ansible-galaxy collection build --force
ansible-galaxy collection install *tar.gz --force
```

## Testing molecule locally
Inside the ansible directory:
```
python -m venv venv
. venv/bin/activate
pip install molecule molecule-docker passlib
molecule test
```
