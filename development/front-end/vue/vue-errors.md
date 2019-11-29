Here are some common rendering or templating errors and what might cause them.

### Property missing or misspelled
Error:
```
[Vue warn]: Property or method "changeSetting" is not defined on the instance but referenced during render. Make sure to declare reactive data properties in the data option.
```

This is probably caused by you referencing a property or method that doesn't exist, either by misspelling it or forgetting to define it.