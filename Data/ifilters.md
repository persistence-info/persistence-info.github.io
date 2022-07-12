## Filter Handlers for Windows Search <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->

### Location: <!-- where to find it -->
`HKLM\Software\Classes`[^1]


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Securtity context|System|
|Persistence type|Registry|
|Code type|DLL[^2]|
|Launch type|Automatic|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->

> Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index. You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.
 

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
- <https://docs.microsoft.com/en-us/windows/win32/search/-search-ifilter-about>
- [Sample open-sourced implementation](https://github.com/gtworek/PSBits/tree/master/IFilter)


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.html) syntax. Yes, it's .html, to make it work in github pages -->
<https://twitter.com/0gtweet/status/1468548924600459267>

### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: It's more complex. More information can be found at <https://docs.microsoft.com/en-us/windows/win32/search/-search-ifilter-registering-filters>
[^2]: COM
