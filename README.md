# ansible-github-cli
A collection of roles to:
- install github cli
- install gh extensions (todo)

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

Use in a role:
```
- name: Ensure gh cli is installed
  tags: github_cli
  become: true
  ansible.builtin.import_role:
    name: compscidr.github_cli.github_cli
```