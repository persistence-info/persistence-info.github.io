## Screen Saver <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKCU\Control Panel\Desktop`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|User|
|Security context| User; System[^1] |
|Persistence type| Registry |
|Code type|EXE[^2]|
|Launch type|Automatic; Any logon required; User initiated[^3]|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Well known key. If you provide a link to your .exe (can be renamed for .scr) in the registry, it will be launched as a screensaver.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://support.microsoft.com/en-us/topic/how-to-change-the-logon-screen-saver-in-windows-ab28d230-ffb9-65f8-74a9-c26c5e00ec73>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
Well known, but [@Alh4zr3d](https://twitter.com/Alh4zr3d) made me aware I did not mention it yet: <https://twitter.com/Alh4zr3d/status/1622980055650410497>

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: If the default screen saver is changed. Admin required though.
[^2]: Can be renamed to .scr
[^3]: Screensaver executable must start due to inactivity, or when user changes its properties.
