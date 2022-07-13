## cmd.exe AutoRun <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKCU\Software\Microsoft\Command Processor\AutoRun`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|User|
|Security context| User|
|Persistence type| Registry |
|Code type|EXE; Other; Fileless|
|Launch type|User initiated[^1]|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
`cmd.exe /?` says:
> when CMD.EXE starts, it looks for the following REG_SZ/REG_EXPAND_SZ registry variables, and [...], they are executed first.
> `HKEY_CURRENT_USER\Software\Microsoft\Command Processor\AutoRun`

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://devblogs.microsoft.com/oldnewthing/20071121-00/?p=24433>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: User must launch cmd.exe
