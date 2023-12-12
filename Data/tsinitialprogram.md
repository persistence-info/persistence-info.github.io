## TS Initial Program <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
- `HKLM\SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services`
- `HKCU\SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services`
- `HKLM\SYSTEM\CurrentControlSet\Control\Terminal Server\WinStations\RDP-Tcp`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin; User[^1]|
|Security context| User |
|Persistence type| Registry |
|Code type|EXE|
|Launch type| User initiated[^2]|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
If the `fInheritInitialProgram` value is set to 1, the exe indicated in the `InitialProgram` value is automatically started on RDP connection.

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://twitter.com/JacqBens/status/1560380971777662983>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[@JacqBens](https://twitter.com/JacqBens)


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: For HKCU
[^2]: Terminal Services connection must be established

