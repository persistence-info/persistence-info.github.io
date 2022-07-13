## AeDebug


### Location: <!-- where to find it -->
`HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\AeDebug`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| User; System[^1] |
|Persistence type| Registry |
|Code type|EXE|
|Launch type|Other|
|Impact|Non-destructive[^2]|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:
Well known key. Add or edit the `Debugger` value, using a REG_SZ string that specifies the command line for the debugger.

> If you want the debugger to be invoked without user interaction, add or edit the Auto value, using a REG_SZ string that specifies whether the system should display a dialog box to the user before the debugger is invoked. The string "1" disables the dialog box; the string "0" enables the dialog box.

Starts on application crash, which may be not reliable enough.

Breaks the parent-child chain, making it harder to detect.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://docs.microsoft.com/en-us/windows/win32/debug/configuring-automatic-debugging>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.html) syntax. Yes, it's .html, to make it work in github pages -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Depends on the crashing image
[^2]: The original debugger exe will not start
