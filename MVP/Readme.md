## Usages
To name the module classes add custom parameter to `generamba gen` command. Creates a MVP module without flow controller, this should be used for additional modules within a specific flow.

```
generamba gen [MODULE-NAME] MVP --module_path [MODULE-PATH]
```

`MODULE-PATH` can contain slashes to make sub-folders, like `App/Modules/Gallery`

Custom parameters `--custom_parameters`:

- `hasDelegate:[yes|no]`: adds presenter delegate protocol to presenter, needs `delegate`.
- `delegate:[presenter/controller]`: the presenter/controller implementing the this presenters delegate protocol, needs `hasDelegate`.
