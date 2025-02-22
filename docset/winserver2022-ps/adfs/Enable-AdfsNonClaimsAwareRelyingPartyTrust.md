---
description: Use this topic to help manage Windows and Windows Server technologies with Windows PowerShell.
external help file: Microsoft.IdentityServer.Management.dll-Help.xml
Module Name: ADFS
ms.date: 12/20/2016
online version: https://docs.microsoft.com/powershell/module/adfs/enable-adfsnonclaimsawarerelyingpartytrust?view=windowsserver2022-ps&wt.mc_id=ps-gethelp
schema: 2.0.0
title: Enable-AdfsNonClaimsAwareRelyingPartyTrust
---

# Enable-AdfsNonClaimsAwareRelyingPartyTrust

## SYNOPSIS
Enables a relying party trust for a non-claims-aware web application or service from the Federation Service.

## SYNTAX

### IdentifierName (Default)
```
Enable-AdfsNonClaimsAwareRelyingPartyTrust [-PassThru] [-TargetName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Identifier
```
Enable-AdfsNonClaimsAwareRelyingPartyTrust [-PassThru] -TargetIdentifier <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### IdentifierObject
```
Enable-AdfsNonClaimsAwareRelyingPartyTrust [-PassThru]
 -TargetNonClaimsAwareRelyingPartyTrust <NonClaimsAwareRelyingPartyTrust> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Enable-AdfsNonClaimsAwareRelyingPartyTrust** cmdlet enables a relying party trust for a non-claims-aware web application or service from the Federation Service.
When you disable a relying party trust, no authentication is allowed.
Non-claims-aware relying party trusts for applications that are published through the Web Application Proxy must be enabled to allow clients outside the network to reach the application through the proxy.

A non-claims aware relying party trust is a relying party trust for web applications or services that do not rely directly on Active Directory Federation Services (AD FS) to issue tokens, but instead rely on a third party that accesses such tokens and transforms them into what applications understand.
A non-claims-aware relying party trust is useful for defining authentication and authorization policies for web applications and services that do not rely on AD FS tokens.
The Web Application Proxy requests such tokens for pre-authentication to web applications or services that have corresponding non-claims-aware relying party trusts for requests that come from outside the network through the proxy.

## EXAMPLES

### Example 1: Enable a non-claims-aware relying party trust by using a name
```
PS C:\> Enable-AdfsNonClaimsAwareRelyingPartyTrust -TargetName "ExpenseReport"
```

This command enables the non-claims-aware relying party trust for the application named ExpenseReport.

### Example 2: Enable a non-claims-aware relying party trust by using an identifier
```
PS C:\> Enable-AdfsNonClaimsAwareRelyingPartyTrust -TargetIdentifier "https://Contosoexpense/"
```

This command enables the non-claims-aware relying party trust for the expense report application that has the identifier https://Contosoexpense.

## PARAMETERS

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### -TargetIdentifier
Specifies the identifier of the non-claims-aware relying party trust to enable.

```yaml
Type: String
Parameter Sets: Identifier
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetName
Specifies the name of the non-claims-aware relying party trust to enable.

```yaml
Type: String
Parameter Sets: IdentifierName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNonClaimsAwareRelyingPartyTrust
Specifies a **NonClaimsAwareRelyingPartyTrust** object.
The cmdlet enables the non-claims-aware relying party trust that you specify.
To obtain a **NonClaimsAwareRelyingPartyTrust**, use the **Get-AdfsNonClaimsAwareRelyingPartyTrust** cmdlet.

```yaml
Type: NonClaimsAwareRelyingPartyTrust
Parameter Sets: IdentifierObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AdfsNonClaimsAwareRelyingPartyTrust](./Add-AdfsNonClaimsAwareRelyingPartyTrust.md)

[Disable-AdfsNonClaimsAwareRelyingPartyTrust](./Disable-AdfsNonClaimsAwareRelyingPartyTrust.md)

[Get-AdfsNonClaimsAwareRelyingPartyTrust](./Get-AdfsNonClaimsAwareRelyingPartyTrust.md)

[Remove-AdfsNonClaimsAwareRelyingPartyTrust](./Remove-AdfsNonClaimsAwareRelyingPartyTrust.md)

[Set-AdfsNonClaimsAwareRelyingPartyTrust](./Set-AdfsNonClaimsAwareRelyingPartyTrust.md)

