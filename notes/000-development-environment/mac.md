# Mac OS X Specific Installation

### Homebrew

Normally you **NEVER** want to run random commands that you get from the internet in your terminal without understanding what they are and exactly what they do. The terminal could give anyone full access to your entire computer. In this case these commands are coming from a trusted source (me) so it's okay.

Run this command in your terminal to install [Homebrew](https://brew.sh/).

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

### git

Type the command `git`. If it is not already installed, it will prompt you with instructions on how to install.

Then run in the terminal: `git config --global credential.helper osxkeychain`