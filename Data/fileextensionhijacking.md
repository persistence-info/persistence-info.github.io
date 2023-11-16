## File Extension Hijacking
<!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKCU\txtfile\shell\open\command`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|User|
|Security context| User|
|Persistence type| Registry |
|Code type|EXE|
|Launch type| User initiated|
|Impact|Destructive[^1] |
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Replacing the default application for opening txt files can be used as a persistence mechanism.
The stored payload will be triggered when the user opens a txt file.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://attack.mitre.org/techniques/T1546/001>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: In order to still be able to open txt files with an editor, a corresponding process call must be implemented within the payload.




