**Error**
Script execution is disabled on the system

**Sol**
```
get-executionpolicy -list
Set-ExecutionPolicy Unrestricted -Scope LocalMachine
```
