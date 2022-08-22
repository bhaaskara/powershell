# General
Usage | command
:-- | :--
List alias commands | `get-alias`
List all the cmdlets | `get-comamnd`
# Files and Directories
Usage | command
:-- | :--
List the files (ls) | `get-childitem`

# Select an object from o/p
`get process |select-object -property cpu`

# Sort
`get-process | select-object -property CPU |sort-object -descending CPU |select-object -first 10`

# Top 10 in the result
`get-process | select-object -property CPU |sort-object -descending CPU |select-object -first 10`