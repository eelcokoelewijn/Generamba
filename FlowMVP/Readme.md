## Usages
To name the module classes add custom parameter to `generamba gen` command.

```
generamba gen MODULE-NAME FlowMVP --module_path MODULE-PATH
```

`MODULE-PATH` can contain slashes to make sub-folders, like `App/Modules/Gallery`

## Dependencies
A FlowMVP module needs the FlowController protocol and extensions to be available in the project. To install the FlowController protocol + extensions execute the following generamba command.  

```
generamba gen Common FlowController
```

## Rambafile spec
```
### Headers settings
company: COMPANY-NAME

### Xcode project settings
project_name: PROJECT-NAME
xcodeproj_path: XCODE-PROJ-FILE

### Code generation settings section
# The main project target name
project_target: PROJECT-TARGET-NAME
project_file_path: ""
project_group_path: ""

### Catalogs
catalogs:
- 'https://github.com/eelcokoelewijn/Generamba'

### Templates
templates:
- {name: FlowMVP}
- {name: FlowController}
- {name: Service}
- {name: Sourcery}
#- {name: local_template_name, local: 'absolute/file/path'}
#- {name: remote_template_name, git: 'https://github.com/igrekde/remote_template'}
```
