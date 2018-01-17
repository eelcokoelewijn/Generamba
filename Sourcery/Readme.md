## Setup Sourcery
Install Sourcery template into folder/group Sourcery.

```
generamba gen Sourcery Sourcery --module_path PATH
```

`PATH` should be the target folder, like `App`. Not in the root of the project.

## Templates
Goto [Sourcery-Templates](https://github.com/krzysztofzablocki/Sourcery/tree/master/Templates/Templates) and get all the templates for your project.  
Equatable, Mockable and Lenses are really useful.

## Build phase
Setup the Xcode build phase on the target to execute Sourcery and generate code based on the templates.

```
if which sourcery>/dev/null ; then
    sourcery --sources $PROJECT_DIR/$TARGET_NAME --templates $PROJECT_DIR/$TARGET_NAME/Sourcery/Templates/ --output $PROJECT_DIR/$TARGET_NAME/Sourcery/Generated
else
    echo "Sourcery not installed"
fi
```
