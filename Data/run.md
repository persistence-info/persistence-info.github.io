## "Run" registry key


### Location:
`HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Run`


### Classification:

| Criteria | Value |
|:--- |:---|
| Permissions | User |
| Securtity context | User |
| Persistence type | Registry |
| Code type | EXE; Other; Fileless |
| Launch type | Same logon required |
| Impact | Non-destructive |
| OS Version | All OS versions |
| Dependencies | OS only |
| Toolset | Scriptable |


### Description:
Well known key, used by many apps. Any file path specified in a Registry value will be used to `ShellExecute()` the specified file by explorer.exe when user logs on. Multiple values can exist.


### References:
- <https://docs.microsoft.com/en-us/windows/win32/setupapi/run-and-runonce-registry-keys>
- <http://windowsir.blogspot.com/2022/07/does-autostart-really-mean-autostart.html>


### Credits:
N/A


### See also:
- [HKCU `RunOnce` key](runonce.html)
- [HKLM `Run` key](hklmrun.html)
- [HKLM `RunOnce` key](hklmrunonce.html) 


### Remarks:
