## Usages
To name the module classes add custom parameter to `generamba gen` command. Creates a MVP module without flow controller, this should be used for additional modules within a specific flow.

```
generamba gen MODULE-NAME FlowMVP --module_path MODULE-PATH
```

`MODULE-PATH` can contain slashes to make sub-folders, like `App/Modules/Gallery`

## Dependencies
A FlowMVP module needs the FlowController protocol and extensions to be available in the project. To install the FlowController protocol + extensions execute the following generamba command.  

```
generamba gen Common FlowController
```
