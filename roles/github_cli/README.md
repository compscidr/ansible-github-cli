# Github CLI role
This role will:
- import to the gpg key to `/etc/apt/trusted.d` and verify the signature
- add the apt repo to `/etc/apt/sources.d`
- install the gh apt package


### Variables table:

Variable                                | Description
--------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
github_cli_gh_token                     | The GH API token that allows for reading / writing to repos