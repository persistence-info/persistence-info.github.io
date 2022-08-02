## .NET Startup Hooks <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
`DOTNET_STARTUP_HOOKS` environment variable


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|Admin|
|Security context| User; System[^1] |
|Persistence type| Other |
|Code type|DLL[^2]|
|Launch type|Automatic[^3]; User initiated[^4]|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
> You can set the `DOTNET_STARTUP_HOOKS=path/to/assembly.dll` environment variable and then run a .NET app and the runtime will load your assembly.dll before `Main` and call `StartupHook.Initialize()` in it.

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://github.com/dotnet/runtime/blob/main/docs/design/features/host-startup-hook.md>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->
[@KirillOsenkov](https://twitter.com/KirillOsenkov/status/1553548127956639746)
<!-- [@AdamLangePL](https://twitter.com/AdamLangePL/status/1553751377289138176) -->

### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: To be verified
[^2]: .NET DLL required
[^3]: To be verified
[^4]: .NET app must be launched
