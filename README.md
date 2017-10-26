# i3
i3 WM config


## Map Capslock to Esc

```
setxkbmap -option caps:escape
```

## Set key delay and rate

```
xset r rate 200 25
```

## Open new terminal from here

Add to .bashrc

```
# Commands to be executed before the prompt is displayed
# Save current working dir
PROMPT_COMMAND='pwd > "${HOME}/.cwd"'

# Change to saved working dir
[[ -f "${HOME}/.cwd" ]] && cd "$(< ${HOME}/.cwd)"
```

No need to find the pid of the most recent shell, the only requirement is a shell which supports running a command either when the prompt is displayed or each time a command is entered at the prompt.

The saved directory even persists across logout/login, if you don't want that, simply delete ${HOME}/.cwd on logout.

Note: If you have multiple terminals open at different directories, switch to the terminal whose directory you want to 'clone', type <enter> or run some other command at the prompt to save that directory, then open a new terminal.
  
Ref https://faq.i3wm.org/question/150/how-to-launch-a-terminal-from-here/

## Launching .desktop files

```
i3-dmenu-desktop
```

Ref https://build.i3wm.org/docs/i3-dmenu-desktop.html
