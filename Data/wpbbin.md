## Windows Platform Binary Table <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
UEFI


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Other[^1]|
|Security context| System |
|Persistence type| Other |
|Code type|EXE[^2][^3]|
|Launch type|Automatic|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Own toolkit required|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Hardware-based persistence.  
1. During the OS startup, `smss.exe` calls `NtQuerySystemInformation()` function with a `SystemPlatformBinaryInformation` (0x85) as a parameter.  
1. NtQuerySystemInformation() scans UEFI tables stored within hardware memory looking for a piece of data with properly constructed headers.  
1. If the correct pattern ("`WPBT`", length, revision and a checksum) is found, the structure is passed to the `smss.exe`.  
1. `smss.exe` stores the piece of UEFI memory within a file called `%systemroot%\system32\wpbbin.exe`.  
1. `smss.exe` takes execution parameters (command line) from the same UEFI block.  
1. The `wpbbin.exe` is checked for integrity with `IMAGE_DLLCHARACTERISTICS_FORCE_INTEGRITY`.  
1. The `wpbbin.exe` is executed.

The functionality may be disabled with the `DisableWpbtExecution` registry value set to `1` in `HKLM\SYSTEM\CurrentControlSet\Control\Session Manager` (tip by [@Harvesterify](https://twitter.com/Harvesterify))


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
- <http://download.microsoft.com/download/8/a/2/8a2fb72d-9b96-4e2d-a559-4a27cf905a80/windows-platform-binary-table.docx>
- <https://grzegorztworek.medium.com/using-uefi-to-inject-executable-files-into-bitlocker-protected-drives-8ff4ca59c94c>
- https://github.com/tandasat/WPBT-Builder

### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[@Harvesterify](https://twitter.com/Harvesterify)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: File content is stored within UEFI tables.
[^2]: `wpbbin.exe` is created on disk during boot process
[^3]: The code must rely on `ntdll.dll`, without any Win32 API calls.
