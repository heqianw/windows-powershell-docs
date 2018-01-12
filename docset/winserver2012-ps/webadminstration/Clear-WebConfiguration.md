---
external help file: Microsoft.IIS.PowerShell.Provider.dll-Help.xml
ms.assetid: 00539C2C-98C6-4E16-A1D9-4DB348332895
online version: 
schema: 2.0.0
---

# Clear-WebConfiguration

## SYNOPSIS
Removes configuration settings from the specified configuration location.

## SYNTAX

```
Clear-WebConfiguration [-Clr <String>] [-Force] [-Location <String[]>] [-Filter] <String[]>
 [[-PSPath] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Removes configuration settings from the specified configuration location.

## EXAMPLES

### -------------- EXAMPLE 1: Removing ASP configuration on the root node --------------
```
C:\PS>Clear-WebConfiguration -Filter /system.webServer/asp -PSPath 'IIS:\'
```

This command removes the \<asp\> section from the root node.

### -------------- EXAMPLE 2: Remove a configuration property from the root node --------------
```
C:\PS>Clear-WebConfiguration -Filter /system.webServer/asp/@lcid -PSPath 'IIS:\'
```

This example removes the lcid property from the IIS configuration root node.

### -------------- EXAMPLE 3: Removing configuration from the site node --------------
```
IIS:\>Clear-WebConfiguration -Filter /system.webServer/asp -PSPath 'IIS:\sites\Default Web Site'
```

Remove the \<asp\> section from the IIS configuration node for the Default Web Site.

## PARAMETERS

### -Clr
Version of the .NET framework in the form vn.n, such as v4.0 or v2.0.
The default is v4.0.
This parameter is used only when PSPath is set to either Machine or Machine/Webroot.
If PSPath is not set to one of these values and the Clr parameter is set, PowerShell ignores the value of Clr and returns a warning.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Specifies the IIS configuration section or an XPath query that returns a configuration element.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Forces the specified configuration to be cleared.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
The location of the configuration setting to clear.
Location tags are frequently used for configuration settings that must be set more precisely than per application or per virtual directory.
For example, a setting for a particular file or directory could use a location tag.
Location tags are also used if a particular section is locked.
In such an instance, the configuration system would have to use a location tag in one of the parent configuration files.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PSPath
Specifies the configuration path.
This can be either an IIS configuration path in the formatcomputer name/webroot/apphost, or the IIS module path in this format IIS:\sites\Default Web Site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-WebConfiguration](./Get-WebConfiguration.md)

[Set-WebConfiguration](./Set-WebConfiguration.md)
