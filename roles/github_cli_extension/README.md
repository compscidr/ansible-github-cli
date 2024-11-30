# github_cli_extension
This role will install gh extensions if they are not already installed.
To install mupltiple extensions, just invoke the role multiple times
with different variable values.

### Variables table:

Variable                                | Description
--------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
github_cli_extension                    | The extension to install

Note, this will fail if GH_TOKEN env variable is not defined.