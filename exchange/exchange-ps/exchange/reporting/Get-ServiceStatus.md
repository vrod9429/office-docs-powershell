---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019, Exchange Online
schema: 2.0.0
---

# Get-ServiceStatus

## SYNOPSIS
!!! Exchange Server 2010

{{ Fill in the Synopsis }}

!!! Exchange Server 2013, Exchange Server 2016, Exchange Server 2019, Exchange Online



## SYNTAX

```
Get-ServiceStatus [[-Identity] <OrganizationIdParameter>] [-DomainController <Fqdn>]
 [-MaintenanceWindowDays <UInt32>] [-ReportingDatabase <String>] [-ReportingServer <Fqdn>] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -DomainController
{{ Fill DomainController Description }}

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
{{ Fill Identity Description }}

```yaml
Type: OrganizationIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -MaintenanceWindowDays
{{ Fill MaintenanceWindowDays Description }}

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportingDatabase
{{ Fill ReportingDatabase Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportingServer
{{ Fill ReportingServer Description }}

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Exchange.Configuration.Tasks.OrganizationIdParameter

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
