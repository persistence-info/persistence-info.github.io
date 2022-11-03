## IFilters <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SOFTWARE\Classes`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| System |
|Persistence type| COM |
|Code type| DLL |
|Launch type|Automatic[^1]|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Windows Search may be extended to index new, previously unknown file types. It is done through `IFilter` DLLs. 
If someone registers such DLL, it will be called every time new file with the defined extension appears in the system.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://learn.microsoft.com/en-us/windows/win32/api/filter/nn-filter-ifilter>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: The file must appear in the system, however some files such as .log, .etl. or .tmp appear automatically.
