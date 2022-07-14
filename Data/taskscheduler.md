## Task Scheduler <!-- general "title" of the persistence. Good to be unique. -->
<!-- separate sections by two empty lines -->
<!-- do not remove empty sections  -->


### Location: <!-- where to find it -->
N/A[^1]


### Classification: <!-- see "how it works" document. Empty lime must go next. -->

|Criteria|Value|
|:---|:---|
|Permissions|User; Admin|
|Security context| User; System |
|Persistence type| Other |
|Code type|EXE; DLL; Fileless; Other|
|Launch type|Automatic; Other|
|Impact|Non-destructive|
|OS Version|All OS versions|
|Dependencies|OS only|
|Toolset|Scriptable|


### Description:<!-- add two EOLs or two spaces at the end of line to create a line break -->
Scheduled tasks may be used to run custom tasks in many different scenarios. Generally, end-users can create tasks executing within their security context, administrators can create tasks running as System.

### References: <!-- use <...> or [abc](https://...) syntax. Prepend with "- " when more than one -->
<https://docs.microsoft.com/en-us/windows/win32/taskschd/task-scheduler-start-page>


### Credits: <!-- use [abc](https://...) syntax. Prepend with "- " when more than one. -->


### See also: <!-- if refering to the same repo, use [Name](file.md) syntax. -->
<!-- prepend with "- " if more than one -->


### Remarks: <!-- see the usage in the "classification" section. Use only 1:1 references i.e. not refering to the same footnote from two different places -->
[^1]: Task data is stored within the registry, but API access seems to be more reasonable in all cases.
