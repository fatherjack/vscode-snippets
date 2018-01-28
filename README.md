# vscode-snippets

Useful snippets for faster, more reliable script editing with VSCode. If you already have custom VSCode snippets then copy all or any of the snippets here and paste them directly into your own Powershell.json.

If you haven't started using VSCode snippets yet then access them via the **File** menu, **Preferences**, **User Snippets** option.

## PowerShell

## Regex shortcuts

### Prefix: _regx

    Description:
    Provides a set of Regex examples for reference of common regex expressions.

    Sample:
    "\\w       - Any word character",
    "\\d       - Any decimal digit",
    "*        - Zero or more{0,}"

## SQL SMO

### prefix: _SQLsmo

    Description:
    Inserts SQL Server SMO line with tab stops to allow Server name values to be added.

    Sample:
    "${1}\\$Servers = get-content ${2}\"C:\\Scripts\\Powershell\\Lookups\\Servers.txt\" ",
    "${3}\\$Server = \"\\$ENV:COMPUTERNAME\\\\${4}sql2016\"",
    "\\$SMOServer = new-object ('Microsoft.SQLServer.Management.Smo.Server') \\$Server$0"

## For each SQL DB

### Prefix: _foreachDB

    Description:
    For each loop for SQL Server database itteration

    Sample:

## SQL Assemblies

### Prefix: _SQLAssemblies

    Description:
    Lines to load SQL Server assemblies

    Sample:

## GetHelp alternative

### prefix: _help

    Description:
    Alternate to Get-Help. Tab stop allows you to type required function name and then press F8. Notepad will open and you can immediately paste into the open window to see the full help content.

    Sample:
    "Get-Help ${1:FunctionName} -Full | clip | notepad.exe$0"

## Hashtable for foreach results

### Prefix: _HashTableForEach

    Description:
    Presents a HashTable variable in place for the results of a foreach iteration that collects data. Tab stops allow for custom variable names to be entered once the intellisense code is onscreen.

    Sample:
    "$${1:VariableName} = @{}",
    "$${1:VariableName} = foreach($${2:ItemName} in $${3:SetName}){",
    "${0:## loop logic in here}",
    "}"
