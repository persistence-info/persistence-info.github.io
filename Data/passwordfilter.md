## Password Filter <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`HKLM\SYSTEM\CurrentControlSet\Control\Lsa`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Securtity context| System|
|Persistence type| Registry |
|Code type|DLL|
|Launch type|User initiated[^1]|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> When a password change request is made, the Local Security Authority (LSA) calls the password filters registered on the system.

The DLL not only provides some persistence, but also obtains a cleartext password from LSASS.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
- <https://docs.microsoft.com/en-us/windows/win32/secmgmt/password-filters>
- [Sample code](https://github.com/gtworek/PSBits/tree/master/PasswordStealing)


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Password change must happen. Possibly machine password change will work as well making this automatic, but it happens quite rarely.
