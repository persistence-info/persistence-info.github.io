## LSA Extension <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SYSTEM\CurrentControlSet\Control\LsaExtensionConfig\LsaSrv`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin[^1]|
|Security context| System |
|Persistence type| Registry |
|Code type|DLL|
|Launch type|Automatic|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
The `REG_MULTI_SZ` value named `Extensions` contains filenames of DLLs being automatically loaded by `lsass.exe`. Each DLL has its `InitializeLsaExtension()` method called after loading.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://twitter.com/0gtweet/status/1476286368385019906>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[0gtweet](https://twitter.com/0gtweet)


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: TrustedInstaller required
