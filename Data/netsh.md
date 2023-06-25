## netsh.exe extensions <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SOFTWARE\Microsoft\NetSh`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| User |
|Persistence type| Registry |
|Code type|DLL|
|Launch type|User initiated[^1]|
|Impact|Non-destructive[^2]|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Netsh.exe can launch different modules. If you add your own module DLL it will be loaded when netsh.exe starts. `DllMain()` and `InitHelperDll()` are called automatically.
Effectively it leads to DLL sideloading.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://twitter.com/0gtweet/status/1672274872163074051>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
Well known key

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: User must launch netsh.exe
[^2]: Lack of `InitHelperDll()' leads to an error message within netsh.exe but the tool and DLL still work.
