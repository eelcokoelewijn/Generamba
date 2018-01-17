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
