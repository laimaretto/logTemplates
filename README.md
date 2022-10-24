# logTemplates
Templates for the [logChecker](https://github.com/laimaretto/logChecker) tool.

The templates can be written either using `textFSM` or `TTP`. Thoug most of the templates in here are textFSM based.

For the case of Nokia, we are organizing those based on the Timos version.

Inside each template file, one can include control variables. Also, some mandatory comments are needed.

#### - Mandatory
```#Command: /show router bgp summary```

The above is neede in each template file to let logChecker know which command we are trying to parse. We could use some variables as well, suche as `#Command: /show router \S+ interface`.

#### - Optional
```
#filterAction:exclude or include-only
#filterColumns:Var1,Var2,Var3
#majorDown:String1,String2
```
These are control keywords. The control keyword `#filterAction` allows only the actions `exclude` or `include-only`. This will modify the resulting columns of the report. The resulting columns sholud be declared under the control keyword `#filterColumns`.

The keyword `#majorDown` allows us to declared a number of template-specific keywords that logChecker will look for when processing the outputs. So, for example, if our output should be considerd as `down` when the string `connect` is seen, then `connect` should be placed in `#majorDown`.