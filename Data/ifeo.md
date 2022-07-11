#### Location:
`HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\`

#### Classification:
| Criteria | Value |
| :--- | :--- |
| Permissions | Admin |
| Securtity context | User; System |
| Persistence type | Registry |
| Code type | EXE |
| Launch type | Automatic; Any logon required; User initiaded |
| Impact | Destructive |
| OS Version | All OS versions |
| Dependencies | OS only |
| Toolset | Scriptable |

#### Description: 
Well known key. If there is a subkey with a name matching the exe file name, the `Debugger` REG_SZ value is being read and launched with the original exe passed as parameter.
Effectively it leads to image hijacking, as the configured exe is launched instead of the desired one.

#### References: 
[https://blog.malwarebytes.com/101/2015/12/an-introduction-to-image-file-execution-options/](https://blog.malwarebytes.com/101/2015/12/an-introduction-to-image-file-execution-options/)

#### Credits: 


#### See also: 
