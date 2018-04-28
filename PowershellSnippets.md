# PowerShell

## Regex cheat sheet

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
    "foreach(\\$DB in \\$SMOServer.databases){",
    "    ${0:Your script logic here}",
    "}"

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

## SQL Server Configuration Manager

### Prefix: _SSCM

    Description:
    Pastes the path to the MMC snap-in for SQL Server Configuration Manager for all versions. Press tab until you are on the line for the version that you want to manage and then press F8.

    Sample:
    "<# SQL Server 2017 Configuration Manager#> mmc.exe /32 C:\WINDOWS\SysWOW64\SQLServerManager14.msc"
    "<# SQL Server 2016 Configuration Manager#> mmc.exe /32 C:\WINDOWS\SysWOW64\SQLServerManager13.msc"

## Event Viewer

### Prefix: _eventviewer

    Description:
    Pastes the path to the Event Viewer. Press F8 to open Event Viewer.

    Sample:
    "C:\WINDOWS\system32\eventvwr.msc "

## Slack

### Prefix: _slack

    Description:
    "Sometimes Get-Help doesnt have all the information you need. That's when your friends come in."

    Sample:
    "C:\Users\Jonathan\AppData\Local\slack\slack.exe"
