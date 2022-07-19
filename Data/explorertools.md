## Explorer tools <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\MyComputer`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| User |
|Persistence type| Registry |
|Code type|EXE|
|Launch type|User initiated[^1]|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> Looking at the following location: `HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\MyComputer` we can quickly guess that the keys listed underneath refer to a couple of utility tools that Windows occasionally runs.
> Exploring them we can find out that the settings are mapped to the following locations:
> - `BackupPath` = `%SystemRoot%\system32\sdclt.exe`
> - `cleanuppath` = `%SystemRoot%\System32\cleanmgr.exe /D %c`
> - `DefragPath` = `%systemroot%\system32\dfrgui.exe`
> Obviously, replacing these settings with your own (read: malware) will end up with the replacement programs being executed at the time OS will decide to kick off the respective activity (or, the user triggers it).


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://www.hexacorn.com/blog/2017/01/18/beyond-good-ol-run-key-part-55/>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[@Hexacorn](https://twitter.com/Hexacorn)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Requires launching a tool like "Disk Cleanup" etc.
