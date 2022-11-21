## Recycle Bin Open <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SOFTWARE\Classes\CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\shell\open\command`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| User |
|Persistence type| Registry |
|Code type|EXE|
|Launch type| User initiated[^1] |
|Impact|Destructive[^2]|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Executes an exe each time user tries to open the Recycle Bin. Creating the key requires a change of permissions to a registry key. Administrators can do it.

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
- <https://www.hexacorn.com/blog/2018/05/28/beyond-good-ol-run-key-part-78-2/>
- <https://gitlab.com/ORCA000/recyclebinpersistence>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
- [@Hexacorn](https://twitter.com/Hexacorn)
- [@ORCA](https://twitter.com/ORCx41)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Requires opening the Recycle Bin
[^2]: Recycle Bin opening may not work
