---
title: run
---

Executes the indicated program. If the process can't be created, the action script is terminated. Run does not wait for the process to terminate before executing the next line of the action script. The command line contains the name of the executable and may optionally contain parameters.

If you wish to wait for one program to finish before starting another one, use the [wait](./wait.html) command.

## Syntax

    run <command-line>

## Examples

These examples show how you might run a script and pass it some arguments. Quotes around the command line are recommended, and necessary if there are spaces in file names.

```actionscript
run "{pathname of regapp "wordpad.exe"}"
run "c:\winnt\ftp.exe" ftp.mycorp.net
run wscript /e:vbs x.vbs arg1 arg2
```

## Notes

On a Windows computer, this command has the same effect as calling the [CreateProcess](https://msdn.microsoft.com/en-us/library/windows/desktop/ms682425%28v=vs.85%29.aspx) function with `<command-line>`. This is also the same as using `<command-line>` in the Windows Run dialog.

See the Windows documentation on [CreateProcess](https://msdn.microsoft.com/en-us/library/windows/desktop/ms682425%28v=vs.85%29.aspx) for a discussion of the method used to locate the executable from a `<command-line>`.
