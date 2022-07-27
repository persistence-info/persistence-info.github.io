## Autodial DLL <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SYSTEM\CurrentControlSet\Services\WinSock2\Parameters\AutodialDLL`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| System[^1] |
|Persistence type| Registry |
|Code type|DLL|
|Launch type|Automatic[^2]|
|Impact|Non-destructive[^3]|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> When Winsock library connects to the internet it 'talks' to various service providers and probes them for connectivity services. [...] 
> At some stage it attempts to load a DLL as specified by the following Registry key:
> `HKLM\SYSTEM\CurrentControlSet\Services\WinSock2\Parameters\AutodialDLL`
> This key is quite obscure and Microsoft only describes it in a context of a very old vulnerability MS06-041.
> Turns out that the AutodialDLL entry points to a DLL that WinSock will load anytime it connects to the internet.
> The DLL needs to export 3 functions:
> - WSAttemptAutodialAddr
> - WSAttemptAutodialName
> - WSNoteSuccessfulHostentLookup


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://www.hexacorn.com/blog/2015/01/13/beyond-good-ol-run-key-part-24/>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[@Hexacorn](https://twitter.com/Hexacorn)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Requires confirmation but it should be possible
[^2]: Requires confirmation
[^3]: Requires confirmation

