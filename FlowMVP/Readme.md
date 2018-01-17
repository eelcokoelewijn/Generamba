## Usages
To name the module classes add custom parameter to `generamba gen` command.

```
generamba gen MODULE-NAME FlowMVP --module_path MODULE-PATH
```
Custom parameters `--custom_parameters`:

- `windowRootVC:[yes|no]`: adds init with `UIWindow` as argument, to setup flow-controller as `window.rootViewController`.
- `hasDelegate:[yes|no]`: adds flow controller delegate protocol for flow-controller, needs `delegate`.
- `delegate:[flow-controller]`: the flow-controller implementing the delegate protocol, needs `hasDelegate`.

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
xcodeproj_path: XCODE-PROJ-FILE.xcodeproj

### Code generation settings section
# The main project target name
project_target: PROJECT-TARGET-NAME
project_file_path: [TARGET-PATH]
project_group_path: [TARGET-GROUP]

### Tests generation settings section
# The tests target name
test_target: [TARGET]Tests

# The file path for new tests
test_file_path: [TARGET-PATH]Tests

# The Xcode group path to new tests
test_group_path: [TARGET-GROUP]Tests

### Catalogs
catalogs:
- 'https://github.com/eelcokoelewijn/Generamba'

### Templates
templates:
- {name: MVP}
- {name: FlowMVP}
- {name: FlowController}
- {name: Service}
- {name: Sourcery}
#- {name: local_template_name, local: 'absolute/file/path'}
#- {name: remote_template_name, git: 'https://github.com/igrekde/remote_template'}
```
