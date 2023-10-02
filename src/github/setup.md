# Setup

Once you have a GitHub account setup, it is a good idea to link it with your local Git configuration for your system. Open a new shell and run the following commands, filling in your details.

```sh
# Set the name that is identifiable for credit when reviewing version history
git config --global user.name "github-username"

# Set an Email address that will be associated with each history marker
git config --global user.email "github-email"

# Set automatic command line coloring for Git for easy reviewing
git config --global color.ui auto
```

## GitHub Personal Access Tokens

To access private repos from GitHub you will need to either set up SSH ([below](#ssh--git)) or generate a personal access token to use as a password for HTTP login. Follow [this](https://github.com/settings/tokens) link and click the 'Generate new token' (select the 'classic' token option). Tick every box and name the token something like 'Full Access Token'. This will act as a universal password for accessing your GitHub recourses. Make sure to also set it to have no expiration date so it never becomes invalid. Once you generate the token make sure to copy and store it in a secure location as you will never be able to after this.

> Note: It should be noted that this is not a best practice as losing this token or leaking it will completely expose your account. This is a method for convenience not safety. You should read the options and tick only what's necessary for a token to control in future.

## SSH + Git

Typically you can just use the HTTP protocol to clone or upload repos, however, this is not as secure as using SSH and cloning private repos requires a Personal Access Token. Using SSH is generally far more secure and far more convenient. To do this, we must first install OpenSSH, the process of which can be different for every platform.

### Install OpenSSH

#### Windows

Open PowerShell as Administrator and run the following commands.

```powershell
# Check if OpenSSH Client and Server packages are already installed
Get-WindowsCapability -Online | Where-Object Name -like 'OpenSSH*'

# Install the OpenSSH Client
Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

# Install the OpenSSH Server
Add-WindowsCapability -Online -Name OpenSSH.Server~~~~0.0.1.0
```

#### Linux (Ubuntu)

```sh
sudo apt install openssh-client openssh-server
```

#### macOS

```sh
# Install OpenSSH with Homebrew
brew install openssh
```

### SSH Keygen and Setup w/ GitHub

Next we generate a key using the `ssh-keygen`. Running the command below will begin the process for generating an SSH key. It will then prompt you to enter a file location. Just press enter to use the default location. It will then ask you to enter a passphrase. This is optional, but recommended.

```sh
ssh-keygen -t ed25519 -C "your_email@example.com"
```

> Note: It is best to you the ed255519 algorithm however, on legacy systems this may not be available so the RSA-4096 algorithm should be used instead.
>
> ```sh
> ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
> ```

Once you have generated your key, you need to start an SSH agent and add the key.

```sh
# Start new SSH agent
eval "$(ssh-agent -s)"

# Point agent to key location key
ssh-add ~/.ssh/id_ed25519
```

You will then need to copy the public key to your clipboard. You can print the key using the `cat` command.

```sh
cat ~/.ssh/id_ed25519.pub
```

Then, go to your GitHub account, go to settings, and click on the SSH and GPG keys tab (or click [this](https://github.com/settings/keys) link). Click on "New SSH key", and paste the key into the box. Give it a name, and click "Add SSH key". You should now be able to clone repos using SSH. To do this, go to the repo you want to clone, but instead of copying the HTTP link, copy the SSH link, and then its regular Git cloning.
