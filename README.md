## Generamba
Initialising
```
generamba init
```

Installing templates
```
generamba template install
```

Generating code-scaffolds
```
generamba gen [MODULE-NAME] [TEMPLATE] --module_path [MODULE-PATH]
```
`[MODULE-PATH]`: optional path where to create the module, ignores `project_file_path` set in the Rambafile.

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
