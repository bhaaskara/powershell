- How powershell relate to Unix ?
- ps conepts
    - scripting
    - functions
    - customization
    - integration
- Daily use case scenarios 
- Desire state and function concept

# Syntax and Structure
Four different types of commands can be run 
- Native Administrative Commands 
    - ifconfig 
- Aliases 
    - cls, Is
    - `get-alias`   
- Scripts 
    - scripts will have `.ps1` extension
    - modules will have `.psm1` extension
- Cmdlets
    - Will follow verb-noun format in general
    - `get-command` lists all the cmdlets

# Pipeline
Used conceptually as an object-based environment 
For example get-process. For each row returned would be a single 
object 
Methods will describe what an object can do 
Allows flexibility and granular manipulation 
Used to string results and also for real-time maintenance of data by 
utilizing variables
Example 
• Get-process —name Mail | stop-process 
• Will result in pulling all process from machine, then find the Mail 
process, then send Mail process as an object to which then Stop—process is applied to  

List all the properties available with in the command
`get-process |get-member`

select the properties you need
`get-process |select-object -property name,CPU`

# Variables
# Modules
Set of related Windows PowerSheII functionalities, grouped together 
as a convenient unit (can be saved in a single directory). 

By defining a set of related script files, assemblies and related 
resources as a module, you can reference, load, persist, and share 
your code much easier than you would otherwise. 

## Modules consist of 
- Code file — either a PS script or a managed cmdlet assembly. 
- Anything else that the above code file may need, such as additional 
assemblies, help files or scripts. 
- A manifest file that describes the above files, as well as stores metadata such 
as author and versioning information. 
- A directory that contains all of the above content, and located where 
PowerShell can find it. 
**NOTE:** None of these are required. You can use script stored in .psm1 file 