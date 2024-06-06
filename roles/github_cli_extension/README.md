# github_cli_extension
This role will install gh extensions if they are not already installed

### Variables table:

Variable                                | Description
--------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
github_cli_gh_token                     | The GH API token that allows for reading / writing to repos
github_cli_user                         | The user to add the GH_TOKEN as env variable for (will append to .bashrc file)
github_cli_extension                    | The extension to install