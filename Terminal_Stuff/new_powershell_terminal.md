# Stuff to remember for new PowerShell terminal:

### lists all the locations a powershell profile might reside:
`$PROFILE | Format-List -Force`

### gets the current prompt as a code block
`(Get-Command Prompt).ScriptBlock` 

which should return something like the following (on terminal that hasn't been set up yet):
```
PS C:\Users\jforney> (Get-Command Prompt).ScriptBlock                                                                                 
"PS $($executionContext.SessionState.Path.CurrentLocation)$('>' * ($nestedPromptLevel + 1)) ";
# .Link
# https://go.microsoft.com/fwlink/?LinkID=225750
# .ExternalHelp System.Management.Automation.dll-help.xml
```

# command to set new temporary session-only prompt
function prompt { }

# command to set temporary prompt that i like:
```
function prompt {"`n $(Get-Date) $($executionContext.SessionState.Path.CurrentLocation)$('>' * ($nestedPromptLevel + 1)) `n> ";}
```

# command to create a new profile file if one doesn't exist already
New-Item -Type File -Force $PROFILE

# good way to learn the powershell commands while in powershell
Get-Command -verb [a verb]
Get-Command -noun [a noun]

# command to allow runing scripts in powershell (this includes even basic shit like having a profile with a custom prompt)
Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser