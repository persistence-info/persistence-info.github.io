## Print Monitor <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SYSTEM\CurrentControlSet\Control\Print\Monitors`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| System |
|Persistence type| Registry |
|Code type|DLL|
|Launch type|Automatic|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> Print monitors are responsible for directing a print data stream from the print spooler to an appropriate port driver. Two types of print monitors are defined -- language monitors and port monitors.

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
- <https://docs.microsoft.com/en-us/windows-hardware/drivers/print/writing-a-print-monitor>
- <https://docs.microsoft.com/en-us/windows-hardware/drivers/print/installing-a-print-monitor>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
