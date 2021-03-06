Mock target - useful for testing. 

Supported in .NET, Silverlight, Compact Framework and Mono

## Configuration Syntax
```xml
<targets>
  <target xsi:type="Debug" name="String" layout="Layout" />
</targets>
```
Read more about using the [[Configuration File]].

## Parameters
### General Options
* **name** - Name of the target.

### Layout Options
* **layout** - Layout used to format log messages. [Layout](Data types) Required. Default: `${longdate}|${level:uppercase=true}|${logger}|${message}`

### Performance Options
* **OptimizeBufferReuse** - Reduce logging overhead, by allowing buffer reuse. Default: `True`
  > Introduced with NLog v4.4.2. Default became `True` with NLog v4.5

## Examples
### Logging to Debug Target
(snippet from [Debug Simple Example.cs](https://github.com/NLog/NLog/blob/43eca983676d87f1d9d9f28872304236393827ba/examples/targets/Configuration%20API/Debug/Simple/Example.cs)  )

        DebugTarget target = new DebugTarget();
        target.Layout = "${message}";

        NLog.Config.SimpleConfigurator.ConfigureForTargetLogging(target, LogLevel.Debug);

        Logger logger = LogManager.GetLogger("Example");
        logger.Debug("log message");
        logger.Debug("another log message");

        Console.WriteLine("The debug target has been hit {0} times.", target.Counter);
        Console.WriteLine("The last message was '{0}'.", target.LastMessage);

Some examples of DebugTarget use can be found in [unit tests](https://github.com/NLog/NLog/blob/43eca983676d87f1d9d9f28872304236393827ba/tests/NLog.UnitTests/Config/TargetConfigurationTests.cs)