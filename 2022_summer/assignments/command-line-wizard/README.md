# Command Line Wizard

Your goal is to complete all of the following tasks by **only using the command line and your code editor**. At the end of the assignment you'll submit a history of all of the commands you typed into your terminal.

## First some practice...

1. In your home directory create a new directory called `codefriends`. This is where we will keep all of the notes and projects that we work on together. Each lesson will have it's own directory inside of `codefriends`.
2. Inside of the newly created `codefriends` directory create a new directory called `001-command-line`.
3. Inside of `001-command-line` create a new file called `notes.md` and a new directory called `projects`.
4. Using the command line open `notes.md` in your code editor. Write down at least three things you learned in class and save the file.
5. Go back to your `codefriends` directory and run the `tree` command. If you do not have the tree command, you can type `brew install tree` on Mac or `sudo apt install tree` on Windows to get it. The output should look like this:
    ```
    ~/codefriends: tree
    .
    └── 001-command-line
        ├── notes.md
        └── projects
    ```
6. If your tree looks different then use `mv`, `rm`, and / or `rmdir` to restructure it to match above.
7. Inside of the `~/codefriends/001-command-line/projects` directory create a new directory called `command-line-wizard`.
7. Copy the output of the `tree` command you ran above and put it inside of `~/codefriends/001-command-line/projects/command-line-wizard/tree.out`.

## Let's make this easier for next time...

Notice the directory structure that you have created inside of `codefriends`. Each day we meet we will replicate this directory structure with a slightly different name, but it will always have `notes.md` and a `projects` directory. Create a bash script called `newday.sh` that will perform the necessary commands to replicate this directory structure. The bash script should take one argument that is the name of the day (eg. `./newday.sh 001-command-line`) and create that directory with a `notes.md` file and a `projects` directory.

## Bonus #1

> Not required but a good challenge if you have extra time

You may have noticed that you need to be inside of the directory where `newday.sh` exists in order to run it. It would be nice if we could run that command from anywhere. The `PATH` variable is a special variable on the command line that specifies where to find executable files.

1. Run `echo $PATH` to see what your current `PATH` variable looks like. You should see a series of command line paths separated by a `:`.
2. Run `pwd` in the directory where your `newday.sh` file is to get the path to that directory. Save the path that is displayed somewhere. We will need it in a few steps.
3. Run `code ~/.zshrc` to open up a special configuration file that allows you to update the `PATH` variable.
4. At the end of the file add `export PATH=$PATH:`. Then add the path that you found with the `pwd` command in step 2 to the end of that new line. You should end up with something like `export PATH=$PATH:/Users/username/codefriends/001-command-line/projects/command-line-wizard`

> If you want to see another example of the power of the command line, the following command will do all of those steps you just did in one line: `echo "export PATH=\$PATH:$(pwd)" >> ~/.zshrc`. If you're curious you can try to figure out what this command means.

[Read this article on PATH variables](https://janelbrandon.medium.com/understanding-the-path-variable-6eae0936e976) to learn more about what they are and how they work.

## Bonus #2

> Not required but a good challenge if you have extra time

Wouldn't it be cool to automatically increment the number at the beginning of the day rather than having to remember if it's day 5 or 6 or 7? Update your bash script to automatically prefix the directory with the next day number. For example `./newday.sh html-css` should automatically create a directory called `002-html-css` if there is already a directory that starts with 001 or `003-html-css` if there are already directories that start with 001 and 002.
