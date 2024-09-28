# Reference
- https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.management/set-location?view=powershell-7.4
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/cd

# Commands
list directory
```
dir
Get-ChildItem
```

change directory
```
cd
Set-Location
```

return to root
```
cd \
Set-location \
```

move to home (~) 
```
cd ~
Set-Location -Path ~
Set-Location ~
```

move up one parent
```
cd ..
Set-Location ..
```

move up two parents
```
cd ..\..
Set-Location ..\..
```

move to folder with spaces (dot is Current Working Directory)
```
cd '.\Saved Games'
```

all the same 
```
cd Desktop
cd .\Desktop
cd .\Desktop\
cd desktop
Set-Location Desktop
Set-Location .\Desktop
Set-Location .\Desktop\
Set-Location desktop
Set-Location -Path Dekstop
```




