# logTemplates
Templates for the [logChecker](https://github.com/laimaretto/logChcker) tool.

The templates can be written either using `textFSM` or `TTP`. Thoug most of the templates in here are textFSM based.

For the case of Nokia, we are organizing those based on the Timos version.

Each Template has some `keywords` at the very begining, such as:

```
#Command: /show router interface
#filterAction: exclude
#filterColumns: 
```

- The `commmand` comment, tells `logChecker` when to start analyzing the logs.
- The `filterAction` comment, can be either `exclude` or `include-only`. This affects the variables decleared in `filterColumns`.
- The `filterColumns` comment, can be empty or can be a list of columns. The columns are the variables declared inside the template itself.