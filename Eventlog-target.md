Writes log message to the Event Log. 

Supported in .NET and Mono
##Configuration Syntax
```
<targets>
  <target xsi:type="EventLog"
          name="String"
          layout="Layout"
          machineName="String"
          source="String"
          category="Layout"
          eventId="Layout"
          log="String" />
</targets>
```
Read more about using the [Configuration File](Configuration file).
##Parameters
###General Options
_name_ - Name of the target.
###Layout Options
_layout_ - Layout used to format log messages. [Layout](Data types) Required. Default: ${longdate}|${level:uppercase=true}|${logger}|${message}
###Event Log Options
_machineName_ - Name of the machine on which Event Log service is running. Default: .  
_source_ - Value to be used as the event Source. By default this is the friendly name of the current AppDomain.  
_category_ - Layout that renders event Category. [Layout](Layout)  
_eventId_ - Layout that renders event ID. [Layout](Layout)  
_log_ - Name of the Event Log to write to. This can be System, Application or any user-defined name. Default: Application