# Github CLI role
This role will:
- install the gpg key to `/usr/share/keyrings` and reference it with `signed-by` from a deb822 source
- add the apt repo to `/etc/apt/sources.d`
- install the gh apt package
- configure gh authentication using native `~/.config/gh/hosts.yml` format


### Variables table:

Variable                                | Description
--------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
github_cli_gh_token                     | The GH API token (PAT) that allows for reading/writing to repos
github_cli_username                     | The GitHub username associated with the token
github_cli_user                         | The system user to configure gh for (defaults to ansible_user)