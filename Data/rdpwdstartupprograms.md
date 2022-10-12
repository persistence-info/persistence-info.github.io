## RDP WDS Startup Programs <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SYSTEM\CurrentControlSet\Control\Terminal Server\Wds\rdpwd\StartupPrograms`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| User |
|Persistence type| Registry |
|Code type|EXE|
|Launch type|Any logon required[^1]|
|Impact|Non-destructive|
|OS Version|All OS versions[^2]|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Not very widely known. Launches applications (server side) after connecting RDP session. You can specify multiple values separate with comas (,) and **without** spaces.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: RDP logon required
[^2]: Practically it is more server-related, as workstations with RDP are not so common
