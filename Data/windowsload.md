## HKCU `Load`  <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKCU\Software\Microsoft\Windows NT\CurrentVersion\Windows`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|User|
|Security context| User|
|Persistence type| Registry |
|Code type|EXE|
|Launch type|Same logon required|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Explorer tries to start an application specified as a value of `Load` within `HKCU\Software\Microsoft\Windows NT\CurrentVersion\Windows`  
As [@rpargman](https://twitter.com/rpargman) writes in his [tweet](https://twitter.com/rpargman/status/1548378142825295872):
> Load is a great regkey to look for in IR because in the usual case it doesn’t exist at all on modern Windows versions. It’s an old leftover that’s still supported for some backward reason.

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://twitter.com/rpargman/status/1548337378816774145>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
 [@rpargman](https://twitter.com/rpargman)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
