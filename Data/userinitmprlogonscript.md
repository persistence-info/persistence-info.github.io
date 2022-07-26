## User Init Mpr Logon Script <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKCU\Environment`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|User|
|Security context| User |
|Persistence type| Registry |
|Code type|EXE; Other[^1]|
|Launch type|Same logon required|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
To test the UserInitMprLogonScript setting:
- Save the script on the drive,
- Under `HKCU\Environment` set `UserInitMprLogonScript` value to the full path of your script,
- Log on.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://www.hexacorn.com/blog/2014/11/14/beyond-good-ol-run-key-part-18/>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[@Hexacorn](https://twitter.com/Hexacorn)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: `.cmd` scripts etc.
