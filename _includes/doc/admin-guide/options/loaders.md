## loaders()

|  Type: |     list of python modules|
|Default:|   empty list|

*Description:* The {{ site.product.short_name }} application imports Python modules
specified in this option, before importing the code of the Python class.
This option has effect only when the Python class is provided in an
external Python file. This option has no effect when the Python class is
provided within [[the {{ site.product.short_name }} configuration file|adm-conf-file]] (in a python{}
block). You can use the loaders() option to modify the import mechanism
that imports Python class. For example, that way you can use
hy in your Python class.

```config
python(class(usermodule.HyParser) loaders(hy))
```
