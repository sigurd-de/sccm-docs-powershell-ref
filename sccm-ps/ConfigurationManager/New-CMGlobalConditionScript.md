---
title: New-CMGlobalConditionScript
titleSuffix: Configuration Manager
description: Creates a Script type global condition in Configuration Manager.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# New-CMGlobalConditionScript

## SYNOPSIS

Creates a Script type global condition in Configuration Manager.

## SYNTAX

### NewScriptFromFile (Default)

```powershell
New-CMGlobalConditionScript -DataType <GlobalConditionDataType> -FilePath <String>
 -ScriptLanguage <ScriptingLanguage> [-UseLoggedOnUserCredential <Boolean>] [-Use32BitHost <Boolean>]
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
```

### NewScriptFromText

```powershell
New-CMGlobalConditionScript -DataType <GlobalConditionDataType> -ScriptText <String>
 -ScriptLanguage <ScriptingLanguage> [-UseLoggedOnUserCredential <Boolean>] [-Use32BitHost <Boolean>]
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
```

## DESCRIPTION

The **New-CMGlobalConditionScript** cmdlet creates a Script type global condition in Microsoft System Center Configuration Manager.

A global condition is a setting or expression in System Center Configuration Manager that you can use to specify how System Center Configuration Manager provides and deploys an application to clients.

## EXAMPLES

### Example 1

```powershell
$GlobalScript = New-CMGlobalConditionScript -DataType String -ScriptText $string -ScriptLanguage JScript -Name GC5
```

This command creates a Script type global condition in Configuration Manager.

## PARAMETERS

### -DataType

Specifies a data type.

```yaml
Type: GlobalConditionDataType
Parameter Sets: (All)
Aliases:
Accepted values: String, DateTime, Integer, FloatingPoint, Version, Boolean

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specifies a description.

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

### -DisableWildcardHandling

DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -FilePath

Specifies a file path of the script.  You can use Windows PowerShell, VBScript, or JScript scripts.

```yaml
Type: String
Parameter Sets: NewScriptFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -Name

Specifies a name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptLanguage

Specifies a script language.

```yaml
Type: ScriptingLanguage
Parameter Sets: (All)
Aliases:
Accepted values: JScript, PowerShell, VBScript

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptText

Specifies a script string.

```yaml
Type: String
Parameter Sets: NewScriptFromText
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Use32BitHost

Indicate whether to use 32-bit host.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseLoggedOnUserCredential

If you enable this option, the script will run on client computers by using the credentials of the user who is signed in.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: UseLoggedOnUserCredentials

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## OUTPUTS

### System.Object

## RELATED LINKS

- [Set-CMGlobalConditionScript](./Set-CMGlobalConditionScript.md)
- [New-CMGlobalCondition](./New-CMGlobalCondition.md)
- [New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)
- [New-CMGlobalConditionAssembly](./New-CMGlobalConditionAssembly.md)
- [New-CMGlobalConditionFile](./New-CMGlobalConditionFile.md)
- [New-CMGlobalConditionIisMetabase](./New-CMGlobalConditionIisMetabase.md)
- [New-CMGlobalConditionOmaUri](./New-CMGlobalConditionOmaUri.md)
- [New-CMGlobalConditionRegistryKey](./New-CMGlobalConditionRegistryKey.md)
- [New-CMGlobalConditionRegistryValue](./New-CMGlobalConditionRegistryValue.md)
- [New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)
- [New-CMGlobalConditionWqlQuery](./New-CMGlobalConditionWqlQuery.md)
- [New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXPathQuery.md)