Use the Mapped Diagnostic Logical Context when you have information that you want available to every logger executing on the current logical context (Similar to "Thread Context Map" in Log4j)

Mapped Diagnostic Logical Context is the async version of the [Mapped Diagnostics Context](Mdc-Layout-Renderer) - a logical call context structure that keeps a dictionary of strings and provides methods to output them in layouts. Allows for maintaining state across asynchronous tasks and call contexts. 

Supported in .NET 4.0 and 4.5.

- As of NLog 4.1 in the NLog package.
- As of NLog 4.1.1, the Mapped Diagnostics Context supports any `Object` type, not just `String`.

## Configuration Syntax
```
${mdlc:item=String}
```

## Parameters
### Rendering Options
* **item** - Name of the item. Required.

## Example
### Simple Properties
The following example demonstrates the basic usage of the Mapped Diagnostic Logical Context.

```c#
MappedDiagnosticsLogicalContext.Set("PropertyName", "PropertyValue");
MappedDiagnosticsLogicalContext.Set("PropertyName2", "AnotherPropertyValue");
```

Add the following to your logger configuration to reference the above properties.
```xml
${mdlc:item=PropertyName}
${mdlc:item=PropertyName2}
```
