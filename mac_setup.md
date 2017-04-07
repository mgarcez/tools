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
brew install bash-completion

brew cask install atom
brew cask install visual-studio-code
brew cask install google-chrome
brew cask install firefox
brew cask install github-desktop
brew cask install eclipse-java
brew cask install vlc
```

## iTerm2
https://gist.github.com/kevin-smets/8568070

`.zshrc`:
```bash
ZSH_THEME="powerlevel9k/powerlevel9k"
POWERLEVEL9K_DIR_HOME_BACKGROUND="red"
POWERLEVEL9K_DIR_HOME_SUBFOLDER_BACKGROUND="27"
#POWERLEVEL9K_DIR_HOME_SUBFOLDER_BACKGROUND="249"
POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(status command_execution_time)

plugins=(git mvn common-aliases docker web-search)
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
