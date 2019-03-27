# Setup for MAC


## Install

https://brew.sh/

```bash
brew tap caskroom/cask

brew cask install java
brew cask install iterm2

brew install maven
brew install vim
brew install git
brew install bash-completion watch tree

brew cask install atom
brew cask install visual-studio-code
brew cask install google-chrome
brew cask install firefox
brew cask install github-desktop
brew cask install eclipse-java
brew cask install intellij-idea-ce
brew cask install vlc
brew cask install magicprefs

sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

## iTerm2
https://gist.github.com/kevin-smets/8568070

`.zshrc`:
```bash
# Path to your oh-my-zsh installation.
export ZSH=/Users/mgarcez/.oh-my-zsh

# Set name of the theme to load. Optionally, if you set this to "random"
# it'll load a random theme each time that oh-my-zsh is loaded.
# See https://github.com/robbyrussell/oh-my-zsh/wiki/Themes
ZSH_THEME="powerlevel9k/powerlevel9k"
POWERLEVEL9K_DIR_HOME_BACKGROUND="red"
POWERLEVEL9K_DIR_HOME_SUBFOLDER_BACKGROUND="27"
#POWERLEVEL9K_DIR_HOME_SUBFOLDER_BACKGROUND="249"
POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(status command_execution_time)

# Which plugins would you like to load? (plugins can be found in ~/.oh-my-zsh/plugins/*)
# Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
# Add wisely, as too many plugins slow down shell startup.
plugins=(git mvn common-aliases docker zsh-syntax-highlighting zsh-autosuggestions)

export PATH=$PATH:/Users/mgarcez/Documents/git_clones

setopt HIST_IGNORE_DUPS
setopt hist_ignore_all_dups
unsetopt share_history

setopt auto_cd                  # if command is a path, cd into it

source $ZSH/oh-my-zsh.sh

```

## Tips

Sleep: `shift` + `control` + `Power `

Spotlight search: `command`+ `space`

```bash
# Show/hide hidden files
alias hide_hidden_files='defaults delete com.apple.finder AppleShowAllFiles; killall Finder;'
alias show_hidden_files='defaults write com.apple.finder AppleShowAllFiles -boolean true; killall Finder;'

# Make text smaller (by reducing the scale factor)
defaults write NSGlobalDomain AppleDisplayScaleFactor .6
killall Finder
```
