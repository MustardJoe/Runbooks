# setting up a new terminal for regular use? keep those custom prompts and other handy customizations !


## add these lines to .profile file

Custom Prompt I like:

replaces the Username with BigMor, gives you Current Time and Working Directory, and sets a NewLine both before and after the prompt, just like mom used to make.
```
export PS1='\n \[\e[0;96m\]BigMor\[\e[m\] \[\e[0;97m\]\@ \d\[\e[m\] \[\e[0;91m\w \[\e[m\] \n$ '
```

get ssh-agent to start up with each terminal session
```
if [ -z "$SSH_AUTH_SOCK" ] ; then
  eval `ssh-agent -s`
  ssh-add
fi
```

## add to .bash_loggout

```
# when leaving the console clear the screen to increase privacy

if [ "$SHLVL" = 1 ]; then
    [ -x /usr/bin/clear_console ] && /usr/bin/clear_console -q
fi

# loggout from ssh session when terminal closes/ends
if [ -n "$SSH_AUTH_SOCK" ] ; then
  eval `/usr/bin/ssh-agent -k`
fi
```