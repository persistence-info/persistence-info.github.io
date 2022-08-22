## PowerShell Profile <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
- `$PSHOME\Profile.ps1`
- `$PSHOME\Microsoft.PowerShell_profile.ps1`
- `$Home\[My ]Documents\PowerShell\Profile.ps1`
- `$Home\[My ]Documents\PowerShell\Microsoft.PowerShell_profile.ps1`

Where `$PSHOME` variable = installation directory for PowerShell, `$Home` variable = current user's home directory.

### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin; User|
|Security context|User|
|Persistence type|Files only|
|Code type|Other|
|Launch type|User initiated[^1]|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
PowerShell profile - a script, running automatically each time PowerShell is started.  
To start PowerShell without profiles, use the `-NoProfile` parameter of PowerShell.exe

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_profiles>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: PowerShell must be launched
