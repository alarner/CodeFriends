[Table of Contents](/README.md)

# Day 000 - Setting up your Development Environment

Before we can get started on our first day of class, we want to make sure you are set up with a "development environment" on your personal computer. Setting up your development environment just means installing and testing the necessary tools that we will be using over the course of the class.

## Download and Install
* [Chrome](https://www.google.com/chrome/)
* [Discord](https://discord.com/download)
* [iTerm2](https://www.iterm2.com/downloads.html) (for OS X) or [Hyper](https://hyper.is) (for Windows 10)
* [VS Code](https://code.visualstudio.com/Download)

## Register an account
* Discord (you should have received an invite)
* [GitHub](https://github.com/join)

## For Mac Users Only

[Follow these Mac OS X specific instructions](./mac.md)

## For Windows Users Only

[Follow these Widows 10 specific instructions](./windows.md)

### git settings

Run in the terminal (replace with your name and email address):

```
git config --global user.name "Your Name"
git config --global user.email you@example.com
git config --global push.default matching
git config --global pull.ff only
git config --global core.editor "code --wait"
```

## Install nodejs

Run in the terminal: `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash`

### Install 'oh my zsh'

Run in the terminal: `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

## Customize your shell

In the terminal run the following commands one by one:

```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
```
curl https://gist.githubusercontent.com/alarner/cf808bc1eccaae7198c6/raw/dbla.zsh-theme > ~/.oh-my-zsh/themes/dbla.zsh-theme
```
```
sed -i '.zshrc_original' 's/robbyrussell/dbla/g' ~/.zshrc
```
```
source ~/.zshrc
```
