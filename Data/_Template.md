## Image File Execution Options <!-- general "title" of the persistence. Good to be unique -->
<!-- separate sections by two empty lines -->

### Location: <!-- where to find it -->
`HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Securtity context| User; System[^1] |
|Persistence type| Registry |
|Code type|EXE|
|Launch type|Automatic; Any logon required; User initiated[^2]|
|Impact|Destructive[^3]|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Well known key. If there is a subkey with a name matching the exe file name, the `Debugger` REG_SZ value is being read and launched with the original exe passed as parameter.
Effectively it leads to image hijacking, as the configured exe is launched instead of the desired one.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://blog.malwarebytes.com/101/2015/12/an-introduction-to-image-file-execution-options/>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](Data/file.html) syntax. Yes, it's .html, to make it work in github pages -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Depends on the image being hijacked
[^2]: Depends on the image being hijacked
[^3]: The original exe will not start

