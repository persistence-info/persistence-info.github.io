## ServerLevelPluginDll <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SYSTEM\CurrentControlSet\Services\DNS\Parameters`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin[^1]|
|Security context| System |
|Persistence type| Registry |
|Code type|DLL|
|Launch type|Automatic|
|Impact|Non-destructive|
|OS Version|Windows Server|
|Dependencies|Additional components required[^2]|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> ServerLevelPluginDll: An absolute pathname of a dynamic link library that the DNS server can use to resolve unknown names, or an empty string to remove or disable the previously selected DLL.

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
- <https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-dnsp/c9d38538-8827-44e6-aa5e-022a016ed723>
- <https://adsecurity.org/?p=4064>
- [Sample open-source code](https://github.com/gtworek/PSBits/tree/master/ServerLevelPluginDll)


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: DNSAdmins membership required
[^2]: DNS Server role must be installed
