[Table of Contents](/README.md)

# Day 000 - Setting up your Development Environment

Before we can get started on our first day of class, we want to make sure you are set up with a "development environment" on your personal computer. Setting up your development environment just means installing and testing the necessary tools that we will be using over the course of the class.

> You don’t need to understand or know how to use these various tools yet. You will learn more about them throughout your Code Friends journey. 

## Download and Install
* [Chrome](https://www.google.com/chrome/) - Chrome is the web browser used by most web developers because of the good developer tooling that it provides for free.
* [Discord](https://discord.com/download) - Discord is a chat tool that will allow you to communicate with other students, intructor and TA.
* [iTerm2](https://www.iterm2.com/downloads.html) (for OS X) or [Hyper](https://hyper.is) (for Windows 10) - These are terminal applications that allow you to access a text terminal, aka command-line interface (CLI). The command line allows you to navigate your computer and to give it instructions. Our first class will be devoted to learning more about the command line.
* [VS Code](https://code.visualstudio.com/Download) - VS Code (Visual Studio Code) is a code editor. It makes writing code easier and helps you to catch potential errors in your code early.

## Register an account
* Discord (you should have received an invite)
* [GitHub](https://github.com/join)

## For Mac Users Only

[Follow these Mac OS X specific instructions](./mac.md)

## For Windows Users Only

[Follow these Widows 10 specific instructions](./windows.md)

## Install code command

Go to visual studio code and `cmd+shift+p` to open up the command palette and then you can search for "shell" - look for: install "code" command in path.

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

#### For Windows Users Only

To get zsh to run each time you open a new hyperterm window you need to follow a few additional steps:

1. Run this command in hyperterm `chsh -s $(which zsh)`
2. Press `ctrl ,` in hyperterm and edit the lines that start with shell and shellArgs to look like this:

```
shell: 'C:\\Windows\\System32\\wsl.exe',
shellArgs: [],
```

## Customize your shell

In the terminal run the following commands one by one:

```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
```
curl https://gist.githubusercontent.com/alarner/cf808bc1eccaae7198c6/raw/dbla.zsh-theme > ~/.oh-my-zsh/themes/dbla.zsh-theme
```

### For Mac OS X Users Only
```
sed -i '.zshrc_original' 's/robbyrussell/dbla/g' ~/.zshrc
```
```
source ~/.zshrc
```
### For Mac OS X Users Only
```
sed -i 's/robbyrussell/dbla/g' ~/.zshrc
```
```
source ~/.zshrc
```
