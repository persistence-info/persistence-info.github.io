## Code Signing DLL <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
- `HKLM\SOFTWARE\Microsoft\Cryptography\Providers`
- `HKLM\SOFTWARE\Microsoft\Cryptography\OID`


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| User|
|Persistence type| Registry |
|Code type|DLL|
|Launch type| User initiated[^1]|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> Hijack attacks [...] permit persistent code execution in the context of any application that performs code signing or signature validation. By implementing a SIP or trust provider, code execution is possible.


### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
- <https://specterops.io/assets/resources/SpecterOps_Subverting_Trust_in_Windows.pdf>
- [Open-source implementation](https://github.com/gtworek/PSBits/tree/master/SIP)


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[Matt Graeber](https://twitter.com/mattifestation)

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: All cases of signature verification, including  UAC prompts and displaying file properties.

