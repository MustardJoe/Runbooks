# setting up a new terminal for regular use? keep those custom prompts on lockdown!



`export PS1='\n \[\e[0;96m\]BigMor\[\e[m\] \[\e[0;97m\]\@ \d\[\e[m\] \[\e[0;91m\w \[\e[m\] \n$ '`


add this line to get your ssh to start up with each terminal session

if [ -z "$SSH_AUTH_SOCK" ] ; then
  eval `ssh-agent -s`
  ssh-add
fi


