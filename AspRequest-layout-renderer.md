ASP Request variable. 

Supported in .NET and Mono

## Configuration Syntax
```
${asp-request:cookie=String:serverVariable=String:queryString=String
             :item=String:form=String}
```

## Parameters
### Rendering Options
* **cookie** - Cookie to be rendered.
* **serverVariable** - ServerVariables item to be rendered. See [msdn](https://msdn.microsoft.com/en-us/library/ms524602(v=vs.90).aspx)
* **queryString** - QueryString variable to be rendered.
* **item** - Item name. The QueryString, Form, Cookies, or ServerVariables collection variables having the specified name are rendered.
* **form** - Form variable to be rendered.