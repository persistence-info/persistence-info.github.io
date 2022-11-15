## TelemetryController <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\AppCompatFlags\TelemetryController`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| System|
|Persistence type| Registry|
|Code type|EXE|
|Launch type|Automatic[^1]|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> The Windows Compatibility Telemetry system makes use of the CompatTelRunner.exe binary to run a variety of telemetry tasks.
> It relies on the registry for instructions on which commands to run.
> The problem is that it will run any arbitrary command without restriction of location or type.

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
- <https://www.trustedsec.com/blog/abusing-windows-telemetry-for-persistence/>
- <https://www.scythe.io/library/windows-telemetry-persistence>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[Christopher Paschen](https://www.trustedsec.com/team/christopher-paschen/)


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Active network connection required
