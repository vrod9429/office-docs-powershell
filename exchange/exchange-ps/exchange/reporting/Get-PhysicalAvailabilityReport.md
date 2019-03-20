---
external help file: Microsoft.Exchange.ServerStatus-Help.xml
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019
title: Get-PhysicalAvailabilityReport
schema: 2.0.0
author: chrisda
ms.author: chrisda
ms.reviewer:
monikerRange: "exchserver-ps-2010 || exchserver-ps-2013 || exchserver-ps-2016 || exchserver-ps-2019"
---


# Get-PhysicalAvailabilityReport

## SYNOPSIS
This cmdlet is available only in on-premises Exchange.

The Get-PhysicalAvailabilityReport cmdlet is used with Microsoft System Center Operations Manager. If you don't have System Center Operations Manager in your organization, this cmdlet serves no useful purpose.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

### StartEndDateSet
```
Get-PhysicalAvailabilityReport -EndDate <DateTime> -StartDate <DateTime>
 [[-Database] <DatabaseIdParameter>]
 [[-ExchangeServer] <ServerIdParameter>]
 [-DailyStatistics]
 [-DomainController <Fqdn>]
 [-ReportingDatabase <String>]
 [-ReportingServer <Fqdn>]
 [<CommonParameters>]
```

### ReportingPeriodSet
```
Get-PhysicalAvailabilityReport [-ReportingPeriod <Today | Yesterday| LastWeek | LastMonth | Last3Months | Last6Months | Last12Months>]
 [[-Database] <DatabaseIdParameter>]
 [[-ExchangeServer] <ServerIdParameter>]
 [-DailyStatistics]
 [-DomainController <Fqdn>]
 [-ReportingDatabase <String>]
 [-ReportingServer <Fqdn>]
 [<CommonParameters>]
```

## DESCRIPTION
You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1
```
Get-PhysicalAvailabilityReport -StartDate "3/3/2015 8:00 AM" -EndDate "3/10/2015 5:00 PM" -ReportingServer scom01.contoso.com -ReportingDatabase
```

{{ Add example description here }}

## PARAMETERS

### -EndDate
The EndDate parameter specifies the end date of the date range.

Use the short date format that's defined in the Regional Options settings on the computer where you're running the command. For example, if the computer is configured to use the short date format mm/dd/yyyy, enter 09/01/2018 to specify September 1, 2018. You can enter the date only, or you can enter the date and time of day. If you enter the date and time of day, enclose the value in quotation marks ("), for example, "09/01/2018 5:00 PM".

You use this parameter with the StartDate parameter. You can't use this parameter with the ReportingPeriod parameter.

```yaml
Type: DateTime
Parameter Sets: StartEndDateSet
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDate
The StartDate parameter specifies the start date of the date range.

Use the short date format that's defined in the Regional Options settings on the computer where you're running the command. For example, if the computer is configured to use the short date format mm/dd/yyyy, enter 09/01/2018 to specify September 1, 2018. You can enter the date only, or you can enter the date and time of day. If you enter the date and time of day, enclose the value in quotation marks ("), for example, "09/01/2018 5:00 PM".

You use this parameter with the EndDate parameter. You can't use this parameter with the ReportingPeriod parameter.

```yaml
Type: DateTime
Parameter Sets: StartEndDateSet
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DailyStatistics
The DailyStatistics switch specifies whether to return daily statistics data. You don't need to specify a value with this switch.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
The Database parameter filters the results by the specified Exchange mailbox database. You can use any value that uniquely identifies the database. For example:

- Name

- Distinguished name (DN)

- GUID

```yaml
Type: DatabaseIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019
Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainController
The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

The DomainController parameter isn't supported on Edge Transport servers. An Edge Transport server uses the local instance of Active Directory Lightweight Directory Services (AD LDS) to read and write data.

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

### -ExchangeServer
The ExchangeServer parameter filters the results by the specified Exchange server. You can use any value that uniquely identifies the server. For example:

- Name

- FQDN

- Distinguished name (DN)

- ExchangeLegacyDN

```yaml
Type: ServerIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019
Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReportingDatabase
The ReportingDatabase parameter specifies the URL of the System Center Operations Manager SQL database.

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

### -ReportingPeriod
The ReportingPeriod parameter specifies the date range. Valid values are:

- Today

- Yesterday

- LastWeek

- LastMonth

- Last3Months

- Last6Months

- Last12Months

You can't use this parameter with the StartDate or EndDate parameters.

```yaml
Type: Today | Yesterday | LastWeek | LastMonth | Last3Months | Last6Months | Last12Months
Parameter Sets: ReportingPeriodSet
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Server 2019
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportingServer
The ReportingServer parameter specifies the FQDN of the System Center Operations Manager reporting server (for example, scom01.contoso.com).

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://docs.microsoft.com/powershell/module/exchange/reporting/get-physicalavailabilityreport)
