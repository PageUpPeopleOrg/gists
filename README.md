# gists - WARNING: PUBLIC REPO
...because org based gists isn't a thing on github :(

Please don't add any sensitive data in here.

Great centralized place to put in tidbits of scripts that can be ran from anywhere:

* **Bash** using `source <(curl -s https://raw.githubusercontent.com/PageUpPeopleOrg/gists/master/YOUR-SCRIPT-HERE.sh)`
* **Powershell** using `iex ((New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/PageUpPeopleOrg/gists/master/YOUR-SCRIPT-HERE.ps1'))`

### install-hashicorp

Installs the specified hashicorp product unto your local computer, uses the latest version if none are specified.

`./install-hashicorp <consul|nomad|otto|packer|serf|terraform|vagrant|vault> [version]`

### get-temporary-token

Configures profiles for the various accounts/roles to be assumed.  
First, configure a profile by doing `./get-temporary-token configure [profile-name] [some-user] [some-role] [role-account-number] [access-key] [secret-key]`, then get the token based on the profile created by running `./get-temporary-token get [profile-name] [mfa-token]`.
You can check the status of your session by running `./get-temporary-token expired`.

For easier environment variable setting, run the script with `source ./get-temporary-token get [profile-name] [mfa-token]`.
All information is stored in the [default AWS config/credential location](https://docs.aws.amazon.com/cli/latest/userguide/cli-config-files.html) for better security.