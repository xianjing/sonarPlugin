# Sonar Plugin for NScaffold
===========

## conventions

Plugin must be a nupkg format.
Plugin must contain a default.ns.ps1 as a script implementing fake interface of NSCaffold

folder convention:

sonar\
functions\*.ns.ps1
tools\sonar-runner
default.ns.ps1 - script block 

## inject required configuration

* sonar server
* sonar jdbc connection string
* sonar project properties

* project source dirs - visible from NScaffold
* project test dirs - visible from NScaffold
 

##applied for NScaffold

extend codeBaseConfig with new plugin entry.

plugins = @{
     'name' = 'sonar' 
     'version' = '1.0.0.0'
}
