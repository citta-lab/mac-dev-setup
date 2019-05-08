## Installation Guide


### Homebrew for Mac

Making Mac installation simpler by adding package manager i.e Homebrew,

If the machine has `tcsh` i.e tshell then we need to run `bash` and then install `homebrew` however i had problem executing `nvm` scripts. So start with executing below command to determine the shell.

```
echo $SHELL
```
if it has `tcsh` then change it to `shell` by running
```
chsh -s /bin/sh
```
Now it should echo shell and everything should work fine.

#### I. Basic Installation

1. Install `xcode-select --install`
If this does't get installed then we might need to upgrade the command line which is kind of the problem i had with Mojave. Command line tools is available (here)[https://developer.apple.com/download/more/]

2. Run `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Note:
If this says `Invalid variable` then we might have to run this in `bash`. So run `bash` and then run the above command. This might happen if we are running in `tcsh` shell. 

3. Run `brew tap homebrew/core`
Allows more repos to install packages.

#### II. Homebrew Casks

Homebrew Cask is to help installing Mac applications. This will help avoid going to websites to download, install each software manually.

1. Setup Cask
```
brew tap caskroom/cask
brew tap caskroom/versions
```

#### II. Utilities

1. Tab Completion
```
brew install bash-completion
```
update the `~/.bash_profile` with below snippet so it will work well in the shell
```
if [ -f `brew --prefix`/etc/bash_completion ]; then
  . `brew --prefix`/etc/bash_completion
fi
```

2. Node Installation
2.1 Option
Installing `nvm` i.e node version manager to manage many versions of NodeJS. How ruby does with `RVM`.
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.4/install.sh | bash
```
Installing latest Node
```
nvm install v10.15.3
```

OR
2.2 Option
Install node and npm using brew
```
https://blog.teamtreehouse.com/install-node-js-npm-mac
```

