## Group Policy Client Side Extension
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->

### Location: <!-- where to find it -->
`HKLM\\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon\GPExtensions`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Securtity context| System |
|Persistence type| Registry |
|Code type|DLL|
|Launch type|Automatic|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Group Policy Client Service (`gpsvc`) loads its extension DLLs. The list is easy to be expanded by own DLL creating a persistence mechanism.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
- API - <https://docs.microsoft.com/en-us/previous-versions/windows/desktop/policy/implementing-a-group-policy-client-side-extension>
- List of known extensions, may be outdated - <https://docs.microsoft.com/en-us/archive/blogs/mempson/group-policy-client-side-extension-list>

### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.html) syntax. Yes, it's .html, to make it work in github pages -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
