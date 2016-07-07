# Usage

* `z foo`     # cd to most frecent dir matching foo
* `z foo bar` # cd to most frecent dir matching foo and bar
* `z -r foo`  # cd to highest ranked dir matching foo
* `z -t foo`  # cd to most recently accessed dir matching foo
* `z -l foo`  # list matches instead of cd
* `z -c foo`  # restrict matches to subdirs of $PWD

## Optional Settings:

* set `$_Z_CMD` in .bashrc/.zshrc to change the command (default z).
* set `$_Z_DATA` in .bashrc/.zshrc to change the datafile (default ~/.z).
* set `$_Z_NO_RESOLVE_SYMLINKS` to prevent symlink resolution.
* set `$_Z_NO_PROMPT_COMMAND` if you're handling PROMPT_COMMAND yourself.
* set `$_Z_EXCLUDE_DIRS` to an array of directories to exclude.
* set `$_Z_OWNER` to your username if you want use z while sudo with $HOME kept

# Installation

## Bash / ZSH (without using a framework)

1. Clone Z into your account with `git clone git@github.com:rupa/z.git`
2. Put something like this in your .bashrc/.zshrc: `. /path/to/z.sh`
3. cd around for a while to build up the db
4. Profit!!!

## ZSH Framework Instructions

### [Antigen](https://github.com/zsh-users/antigen)

Add `antigen bundle rupa/z` to your `.zshrc` with your other bundle commands.

Antigen will handle cloning the plugin for you automatically the next time you start zsh. You can also add the plugin to a running zsh by running `antigen bundle rupa/z` on the command line for testing before adding it to your `.zshrc`.

### [Oh-My-Zsh](http://ohmyz.sh/)

1. `cd ~/.oh-my-zsh/custom/plugins`
2. `git clone git@github.com:rupa/z.git`
3. Add z to your plugin list - edit `~.zshrc` and change `plugins=(...)` to `plugins=(... z)`

### [Zgen](https://github.com/tarjoilija/zgen)

Add `zgen load rupa/z` to your .zshrc file in the same function you're doing your other `zgen load` calls in.
