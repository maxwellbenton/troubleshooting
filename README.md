## Fixing NVM and RVM Dotfile Issues for MacOS

If you are having trouble getting RVM, Ruby, Nvm, or Node to work, you may have an issue with your `.zshrc` file. To fix, we need to run two commands.

The first command makes a backup of your current `.zshrc` file:

mv ~/.zshrc{,.bak}

The second command replaces the contents of your `.zshrc` file with a default dot file:

curl -sSL https://raw.githubusercontent.com/flatiron-school/dotfiles/master/.zshrc > ~/.zshrc

Close and reopen your terminal. With a new `.zshrc` file, we can now test out each tool.

### Verify RVM is Installed

To confirm that RVM is working, run:

```
rvm
```

If you see a long message ending in “For additional documentation please visit https://rvm.io”, RVM is installed. If the command `rvm` is not recognized, revisit the Installing Ruby on macOS instructions and run the commands listed, starting from the top of the page.

### Verify Ruby is Installed

To confirm Ruby is installed, run:

```
rvm list
```

If you see `=* ruby-2.6.1`, Ruby is installed and 2.6.1 set as the default version and you are all set for Ruby.

If you do not see `ruby-2.6.1` at all, install it with the following command:

```
rvm install ruby-2.6.12.6.1
```

If `ruby-2.6.1` is listed, but is not preceded by `=*`, make it the default version by running:

```
rvm use 2.6.1 --default
```

### Verify NVM is installed

To confirm NVM is installed, run:

```
nvm
```

If you see a message ending with “Note: to remove, delete, or uninstall nvm…”, nvm is installed. If the `nvm` command is not recognized, install NVM with the following command:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.36.0/install.sh | zsh
```

### Verify Node is Installed

To confirm Node is installed, run:

```
nvm list
```

If you see a message starting with “-> v14.13.0” (or any number higher than this), a version of Node is installed that will work for this course.
