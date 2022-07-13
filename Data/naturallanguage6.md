## Natural Language 6 DLLs <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->

### Location: <!-- where to find it -->
`HKLM\System\CurrentControlSet\Control\ContentIndex\Language`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| System |
|Persistence type| Registry |
|Code type|DLL|
|Launch type|Automatic|
|Impact|Non-destructive[^1]|
|OS Version|All OS versions[^2]|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->

> C:\WINDOWS\system32\SearchIndexer.exe process looks for the `DLLOverridePath` entries under the following locations (language may vary on non-English OS versions):  
> `HKLM\System\CurrentControlSet\Control\ContentIndex\Language\English_UK`
> `HKLM\System\CurrentControlSet\Control\ContentIndex\Language\English_US`
> `HKLM\System\CurrentControlSet\Control\ContentIndex\Language\Neutral`

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://www.hexacorn.com/blog/2018/12/30/beyond-good-ol-run-key-part-98/>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[@Hexacorn](https://twitter.com/Hexacorn)

### See also: <!-- if refering to the same repo, use [Name](file.html) syntax. Yes, it's .html, to make it work in github pages -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: To be verified
[^2]: To be verified
