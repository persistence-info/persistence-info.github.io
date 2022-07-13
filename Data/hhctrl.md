## hhctrl.ocx <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKCR\CLSID\{52A2AAAE-085D-4187-97EA-8C30DB990436}\InprocServer32`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| User|
|Persistence type| Registry |
|Code type|Other[^1]|
|Launch type|User initiated[^2]|
|Impact|Destructive[^3]|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> When hh.exe is started it tries to find the hhctrl.ocx library by checking the following Registry value: `HKCR\CLSID\{52A2AAAE-085D-4187-97EA-8C30DB990436}\InprocServer32'
> The library that the value points to is then loaded.
> If the library doesn’t exist, or the loading didn’t succeed the hh.exe gives it another go and attempts to load the library using the hard-coded name hhctrl.ocx and relying on the LoadLibrary function (and as a result is a subject to side-loading attacks).
> As such, there seem to be at least 2 opportunities here:
> 1. Drop c:\WINDOWS\hhctrl.ocx and delete the HKCR\CLSID\{52A2AAAE... value so running hh.exe will sideload the c:\WINDOWS\hhctrl.ocx
> 2. Replace the value of the HKCR\CLSID\{52A2AAAE… to point to your own lib and run hh.exe – this will load the lib of choice

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://www.hexacorn.com/blog/2018/04/23/beyond-good-ol-run-key-part-77/>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[@Hexacorn](https://twitter.com/Hexacorn)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
[.chm helper DLL](htmlhelpauthor.md)

### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: .ocx
[^2]: 'hh.exe' must be run. Manually, or via associated .chm file
[^3]: To be verified
