# Sonar Plugin for NScaffold
===========

## Conventions

Plugin must be a nupkg format.
Plugin must contain a default.ns.ps1 as a script implementing fake interface of NSCaffold

### folder convention:
<pre><code>
sonar\
functions\*.ns.ps1
tools\sonar-runner
default.ns.ps1 - script block 
</code></pre>

## Inject required configuration

* sonar server
* sonar jdbc connection string
* sonar project properties
* project source dirs - visible from NScaffold
* project test dirs - visible from NScaffold
 
## Add dependencies configurations to project

* Gallio Bundler
* OpenCover
* Report Generate
* FxCop


## Pre-configurated tasks to enable sonar with useful default

* enable-sonar
* new-report
* ....

## Applied for NScaffold

extend codeBaseConfig with new plugin entry.

<pre><code>
plugins = @{
     'name' = 'sonar' 
     'version' = '1.0.0.0'
}
</code></pre>
