## MPNotify <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| System |
|Persistence type| Registry |
|Code type|EXE|
|Launch type|Any logon required|
|Impact|Non-destructive[^1]|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
If you put `mpnotify` `REG_SZ` value into the `HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon` registry key, the exe will be loaded by the `winlogon.exe` process, when user logs on. After the timeout (30s) the process and its child processes are terminated.

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://youtu.be/ggY3srD9dYs>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[@0gtweet](https://twitter.com/0gtweet)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Slows the logon process down by 30s, but it works.
