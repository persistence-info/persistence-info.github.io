## Monitoring Silent Process Exit

<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\SilentProcessExit\<ProcessName>`

`HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\<ProcessName>\`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| User; System[^1] |
|Persistence type| Registry |
|Code type|EXE|
|Launch type|User initiated|
|Impact|None|
|OS Version|Windows 7 and newer|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:
*Monitoring Silent Process Exit* mechanism allows executing an application or script (monitor application), when a process terminates after result of **ExitProcess** call or **TerminateProcess** called by another process. 
To achieve that, few conditions have to by met:
- `GlobalFlag` for monitored process should have `FLG_MONITOR_SILENT_PROCESS_EXIT` flag enabled (512 decimal),
- `ReportingMode` for monitored process should have `LAUNCH_MONITORPROCESS` flag enabled (1 decimal),
- `MonitorProcess` for a monitored process have to be set.

For example, to execute Powershell script that runs calculator after Notepad exit, we could use Powershell itself like this:
```powershell
$monitoredApp = "notepad.exe"
$monitor = "powershell -c calc.exe #"

New-Item -Force -Path "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\$monitoredApp" | Out-Null
Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\$monitoredApp" -Name GlobalFlag -Value 512

New-Item -Force -Path "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\SilentProcessExit\$monitoredApp" | Out-Null
Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\SilentProcessExit\$monitoredApp" -Name ReportingMode -Value 1
Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\SilentProcessExit\$monitoredApp" -Name MonitorProcess -Value $monitor
```

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://learn.microsoft.com/en-us/windows-hardware/drivers/debugger/registry-entries-for-silent-process-exit/>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
- Entry added by [@pawelmaziarz](https://twitter.com/pawelmaziarz)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Depends on the image being hijacked
