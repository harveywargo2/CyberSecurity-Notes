# References
- https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-7.4
- 
# Commands
Set Unrestricted on device
```
Set-ExecutionPolicy Unrestricted
```

See Execution Policy Scopes
```
Get-ExecutionPolicy -List
```

See Current Execution Policy 
```
Get-ExecutionPolicy
```

Set Execution Policy Specific Scope
```
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```