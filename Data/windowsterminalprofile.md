## Windows Terminal Profile <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|User|
|Security context| User |
|Persistence type| File |
|Code type|EXE|
|Launch type|User initiated[^1]|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|Additional software required[^2]|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> 1. Modify the `settings.json` located in `%localappdata%` and add a custom profile that contains your payload
> 1. Change the `defaultProfile` value and put your GUID 
> 1. Add the value `"startOnUserLogin": true`

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
- <https://twitter.com/nas_bench/status/1550836225652686848>
- <https://nasbench.medium.com/persistence-using-windows-terminal-profiles-5035d3fc86fe>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[@nas_bench](https://twitter.com/nas_bench)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Windows Terminal must be run
[^2]: Windows Terminal required

