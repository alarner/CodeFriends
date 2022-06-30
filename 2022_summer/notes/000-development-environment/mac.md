# Mac OS X Specific Installation

### Homebrew

> Homebrew will allow you to use the “brew” command in your terminal (Iterm 2 in your case). The brew command allows you to download other pacakges and applications that you will need

Normally you **NEVER** want to run random commands that you get from the internet in your terminal without understanding what they are and exactly what they do. The terminal could give anyone full access to your entire computer. In this case these commands are coming from a trusted source (me) so it's okay.

Important note: when a command in Iterm2 or Hyper is successful sometimes nothing will happen. Typically if something goes wrong you will get some type of error. Also, when typing a password, it often appears as if you are not typing. Simply put in the password and press enter. 

Run this command in your terminal to install [Homebrew](https://brew.sh/).

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

### git

Type the command `git`. If it is not already installed, it will prompt you with instructions on how to install.

Then run in the terminal: `git config --global credential.helper osxkeychain`