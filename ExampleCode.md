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

# File and Folders
## Copy a folder, subfolder and its contents
`Copy-Item "C:\users\badiveni\test1" -Destination "\\Atsstg1amgts302\data\VMAX_Weekly_Cap_Reports\" -Recurse -Force`

## Zip the folder
`Compress-Archive -Path "C:\SCRIPTS\DATA\MonthlySRDFRepo\*" -DestinationPath ".\Allscripts_VMAX_Weekly_SRDF_Reports.zip" -update`

# Email
```sh
$EmailSettings=@{
    SMTPServer="10.67.21.14"
    From="noreply@allscripts.com"
    #To= "allscriptsstorage@atos.net"
    To= "bhaskar.adiveni@atos.net"
    Subject="Allscripts Storage Weekly SRDH Reports"
    Body= "Please refer to the attached zip file"
    Attachments= ".\Allscripts_VMAX_Weekly_SRDF_Reports.zip"
    BodyAsHtml=$true
}
Send-MailMessage @EmailSettings 
```
