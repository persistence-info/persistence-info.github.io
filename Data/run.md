LOCATION: `HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run`

| Criteria | Value |
| :--- | :--- |
| Permissions | user |
| Securtity context | user |
| Persistence type | registry |
| Code type | EXE |
| Launch type | same logon required |
| Impact | non-destructive |
| OS Version | all OS versions |
| Dependencies | OS only |
| Toolset | OS only, scriptable |

Description: well known key, used by many apps. Any file path specified in a Registry value will be used to launch a file by explorer.exe when user logs on.

References: [https://docs.microsoft.com/en-us/windows/win32/setupapi/run-and-runonce-registry-keys](https://docs.microsoft.com/en-us/windows/win32/setupapi/run-and-runonce-registry-keys)
