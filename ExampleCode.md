## If condition
```powershell
if ($dev -eq "True") 
		{	
			Add-Content -path .\$deviceinfofile -value "$naaid  $enaaid  $sid  $devid  ACLX "
			continue
		}
```


## Logical operators
### -or
```powershell
if ( $age -le 13 -or $age -ge 55 )
```
