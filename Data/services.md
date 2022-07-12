## Windows Services <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->

### Location: <!-- where to find it -->
`HKLM\SYSTEM\CurrentControlSet\Services`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Securtity context|System|
|Persistence type| Registry |
|Code type|EXE, DLL, Other|
|Launch type|Automatic|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable[^1]|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Windows Services are one of the best known and widely used persistence mechanisms. EXE-based approach is best known, but DLLs loaded by `svchost.exe` are used (also by malicious actors) as well.  
Oficially, the DLL must be indicated within the `Parameters` subkey, but in practice it is not required, making the detection a bit harder.[^2]


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
[Persistence with Windows Services](https://gtworek.github.io/PSBits/services.html)
[PowerShell script for service DLL analysis](https://github.com/gtworek/PSBits/blob/master/Services/Get-ServiceDlls.ps1)


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.html) syntax. Yes, it's .html, to make it work in github pages -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Also remotely
[^2]: <https://twitter.com/0gtweet/status/1535156885179047936>
