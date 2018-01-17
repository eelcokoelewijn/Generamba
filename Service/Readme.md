## Usages
Create a service

```
generamba gen Login Service --module_path PATH
```

`PATH` could be a shared resource folder, like `App/Services` or `Shared/Services/Login`

Custom parameters `--custom_parameters`:

- `mockable:[yes|no]`: adds AutoMockable protocol for service.
