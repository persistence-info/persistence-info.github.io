## Authentication Packages <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SYSTEM\CurrentControlSet\Control\Lsa`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| System |
|Persistence type| Registry |
|Code type|DLL|
|Launch type|Automatic|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> Authentication packages are contained in dynamic-link libraries. The Local Security Authority (LSA) loads authentication packages by using configuration information stored in the registry. 

`lsass.exe` loads all DLLs specified by the `Authentication Packages` `REG_MULTI_SZ` value. The DLL should be placed into `%WINDIR%\System32` and referred in the registry without its extension - to load `%WINDIR%\System32\msv1_0.dll`, `msv1_0` only should be entered.

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://docs.microsoft.com/en-us/windows/win32/secauthn/authentication-packages>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->

