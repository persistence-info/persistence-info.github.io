## AMSI Providers <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
- `HKLM\SOFTWARE\Microsoft\AMSI\Providers`
- `HKLM\SOFTWARE\Classes\CLSID`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| User; System |
|Persistence type| Registry |
|Code type|DLL[^1]|
|Launch type|Automatic|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> AMSI is designed in particular to combat "fileless malware". Application types that can optimally leverage AMSI technology include script engines, applications that need memory buffers to be scanned before using them, and applications that process files that can contain non-PE executable code (such as Microsoft Word and Excel macros, or PDF documents).
>
> As a creator of antimalware products, you can choose to author and register your own in-process COM server (a DLL) to function as an AMSI provider.

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
- <https://docs.microsoft.com/en-us/windows/win32/amsi/dev-audience>
- <https://twitter.com/0gtweet/status/1452680501249069062>
- [Sample open source DLL](https://github.com/gtworek/PSBits/tree/master/FakeAMSI)


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: COM
