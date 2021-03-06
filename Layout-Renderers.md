Layout renderers are template macros that are used in [Layouts](Layouts), e.g. `${message}`, `${level}` etc

NLog supports creating custom layout renderers. For more information, see: [Extending NLog](Extending-NLog)


## Layout Renderers

### NLog package [![Version](https://img.shields.io/nuget/v/NLog.svg)](https://www.nuget.org/packages/NLog)
* [${activityid}](Trace-Activity-Id-Layout-Renderer) - Puts into log a System.Diagnostics trace correlation id.
* [${all-event-properties}](All-Event-Properties-Layout-Renderer) - Log all event context data.
* [${appdomain}](AppDomain-Layout-Renderer) - Current app domain. 
* [${assembly-version}](AssemblyVersion-Layout-Renderer) - The version of the executable in the default application domain.
* [${basedir}](Basedir-Layout-Renderer) - The current application domain's base directory.
* [${callsite}](Callsite-Layout-Renderer) - The call site (class name, method name and source information).
* [${callsite-linenumber}](Callsite-line-number-layout-renderer) - The call site source line number. 
* [${counter}](Counter-Layout-Renderer) - A counter value (increases on each layout rendering).
* [${date}](Date-Layout-Renderer) - Current date and time.
* [${document-uri}](DocumentUri-Layout-Renderer) - URI of the HTML page which hosts the current Silverlight application.
* [${environment}](Environment-Layout-Renderer) - The environment variable.
* [${event-properties}](EventProperties-Layout-Renderer) - Log event properties data - rename of ${event-context}.
* [${exception}](Exception-Layout-Renderer) - Exception information provided through a call to one of the Logger.*Exception() methods.
* [${file-contents}](FileContents-Layout-Renderer) - Renders contents of the specified file.
* [${gc}](Gc-Layout-Renderer) - The information about the garbage collector.
* [${gdc}](Gdc-Layout-Renderer) - Global Diagnostic Context item. Dictionary structure to hold per-application-instance values.
* [${guid}](Guid-Layout-Renderer) - Globally-unique identifier (GUID).
* [${identity}](Identity-Layout-Renderer) - Thread identity information (name and authentication information).
* [${install-context}](InstallContext-Layout-Renderer) - Installation parameter (passed to InstallNLogConfig).
* [${level}](Level-Layout-Renderer) - The log level.
* [${literal}](Literal-Layout-Renderer) - A string literal.
* [${log4jxmlevent}](Log4JXMLEvent-Layout-Renderer) - XML event description compatible with log4j, Chainsaw and NLogViewer.
* [${logger}](Logger-Layout-Renderer) - The logger name.
* [${longdate}](LongDate-Layout-Renderer) - The date and time in a long, sortable format `yyyy-MM-dd HH:mm:ss.ffff`.
* [${machinename}](MachineName-Layout-Renderer) - The machine name that the process is running on.
* [${mdc}](Mdc-Layout-Renderer) - Mapped Diagnostics Context - a thread-local structure.
* [${mdlc}](Mdlc-Layout-Renderer) - Async Mapped Diagnostics Context - a thread-local structure.
* [${message}](Message-Layout-Renderer) - The formatted log message.
* [${ndc}](Ndc-Layout-Renderer) - Nested Diagnostics Context - a thread-local structure.
* [${ndlc}](Ndlc-Layout-Renderer) - Async Nested Diagnostics Context - a thread-local structure.
* [${newline}](Newline-Layout-Renderer) - A newline literal.
* [${nlogdir}](NLogDir-Layout-Renderer) - The directory where NLog.dll is located.
* [${performancecounter}](PerformanceCounter-Layout-Renderer) - The performance counter.
* [${processid}](ProcessId-Layout-Renderer) - The identifier of the current process.
* [${processinfo}](ProcessInfo-Layout-Renderer) - The information about the running process.
* [${processname}](ProcessName-Layout-Renderer) - The name of the current process.
* [${processtime}](ProcessTime-Layout-Renderer) - The process time in format HH:mm:ss.mmm.
* [${qpc}](QPC-Layout-Renderer) - High precision timer, based on the value returned from QueryPerformanceCounter() optionally converted to seconds.
* [${registry}](Registry-Layout-Renderer) - A value from the Registry.
* [${sequenceid}](SequenceId-layout-renderer) - The log sequence id
* [${shortdate}](ShortDate-Layout-Renderer) - The short date in a sortable format yyyy-MM-dd.
* [${sl-appinfo}](Sl-AppInfor-Layout-Renderer) - Information about Silverlight application.
* [${specialfolder}](Special-Folder-Layout-Renderer) - System special folder path (includes My Documents, My Music, Program Files, Desktop, and more).
* [${stacktrace}](Stack-Trace-Layout-Renderer) - Stack trace renderer.
* [${tempdir}](TempDir-Layout-Renderer) - A temporary directory.
* [${threadid}](ThreadId-Layout-Renderer) - The identifier of the current thread.
* [${threadname}](ThreadName-Layout-Renderer) - The name of the current thread.
* [${ticks}](Ticks-Layout-Renderer) - The Ticks value of current date and time.
* [${time}](Time-Layout-Renderer) - The time in a 24-hour, sortable format HH:mm:ss.mmm.
* [${var}](Var-Layout-Renderer) - Render variable (new in 4.1)
* [${windows-identity}](Windows-Identity-Layout-Renderer) - Thread Windows identity information (username).

#### Wrappers

* [${cached}](Cached-Layout-Renderer) - Applies caching to another layout output.
* [${filesystem-normalize}](Filesystem-Normalize-Layout-Renderer) - Filters characters not allowed in the file names by replacing them with safe character.
* [${json-encode}](Json-Encode-Layout-Renderer) - Escapes output of another layout using JSON rules.
* [${lowercase}](Lowercase-Layout-Renderer) - Converts the result of another layout output to lower case.
* [${onexception}](OnException-Layout-Renderer) - Only outputs the inner layout when exception has been defined for log message.
* [${pad}](Pad-Layout-Renderer) - Applies padding to another layout output.
* [${replace}](Replace-Layout-Renderer) - Replaces a string in the output of another layout with another string.
* [${replace-newlines}](Replace-NewLines-Layout-Renderer) - Replaces newline characters with another string.
* [${rot13}](Rot13-Layout-Renderer) - Decodes text "encrypted" with ROT-13.
* [${trim-whitespace}](Trim-Whitespace-Layout-Renderer) - Trims the whitespace from the result of another layout renderer.
* [${uppercase}](Uppercase-Layout-Renderer) - Converts the result of another layout output to upper case.
* [${url-encode}](Url-Encode-Layout-Renderer) - Encodes the result of another layout output for use with URLs.
* [${when}](When-Layout-Renderer) - Only outputs the inner layout when the specified condition has been met.
* [${whenEmpty}](WhenEmpty-Layout-Renderer) - Outputs alternative layout when the inner layout produces empty result.
* [${WrapLine}](WrapLine-layout-renderer) - Wraps the result of another layout output at specified line length.
* [${xml-encode}](Xml-Encode-Layout-Renderer) - Converts the result of another layout output to be XML-compliant.
 

### NLog.Extended package  [![Version](https://img.shields.io/nuget/v/NLog.Extended.svg)](https://www.nuget.org/packages/NLog.Extended)
* [${appsetting}](AppSetting-Layout-Renderer) - App config setting.

### NLog.Web package [![Version](https://img.shields.io/nuget/v/NLog.Web.svg)](https://www.nuget.org/packages/NLog.Web)
* [${aspnet-MVC-Action}](AspNet-MVC-Action-Layout-Renderer) - ASP.NET MVC action name
* [${aspnet-MVC-Controller}](AspNet-MVC-Controller-Layout-Renderer) - ASP.NET MVC controller name
* [${aspnet-Application}](AspNetApplication-layout-renderer) - ASP.NET Application variable.
* [${aspnet-Item}](AspNetItem-layout-renderer) - ASP.NET `HttpContext` item variable.
* [${aspnet-TraceIdentifier}](AspNetTraceIdentifier-Layout-Renderer) - ASP.NET trace identifier
* [${aspnet-Request}](AspNetRequest-layout-renderer) - ASP.NET Request variable.
* [${aspnet-Request-Cookie}](AspNetRequest-Cookie-Layout-Renderer) - ASP.NET Request cookie content. 
* [${aspnet-Request-Host}](AspNetRequest-Host-Layout-Renderer) - ASP.NET Request host.
* [${aspnet-Request-Method}](AspNetRequest-Method-Layout-Renderer) - ASP.NET Request method (GET, POST etc).
* [${aspnet-Request-IP}](AspNet-Request-IP-Layout-Renderer) - Client IP.
* [${aspnet-Request-QueryString}](AspNetRequest-QueryString-Layout-Renderer) - ASP.NET Request querystring.
* [${aspnet-Request-Referrer}](AspNetRequest-Referrer-Renderer) - ASP.NET Request referrer.
* [${aspnet-Request-UserAgent}](AspNetRequest-UserAgent-Layout-Renderer) - ASP.NET Request useragent.
* [${aspnet-Request-Url}](AspNetRequest-Url-Layout-Renderer) - ASP.NET Request URL.
* [${aspnet-Session}](AspNetSession-layout-renderer) - ASP.NET Session variable. 
* [${aspnet-SessionId}](AspNetSessionId-layout-renderer) - ASP.NET Session ID variable.
* [${aspnet-User-isAuthenticated}](AspNet-User-isAuthenticated-Layout-Renderer) -  ASP.NET User authenticated? 
* [${aspnet-User-AuthType}](AspNetUserAuthType-layout-renderer) - ASP.NET User auth.
* [${aspnet-User-Identity}](AspNetUserIdentity-layout-renderer) - ASP.NET User variable.
* [${iis-site-name}](IIS-site-name-Layout-Renderer) - IIS site name.

## External packages

External packages, not maintained by the NLog team.

* [${xml}](https://github.com/loresoft/NLog.Xml) - [![Version](https://img.shields.io/nuget/v/NLog.Xml.svg)](https://www.nuget.org/packages/nlog.xml) - Converts to XML format

* [${gelf}](https://github.com/farzadpanahi/NLog.GelfLayout) - [![Version](https://img.shields.io/nuget/v/NLog.GelfLayout.svg)](https://www.nuget.org/packages/NLog.GelfLayout) - Converts log to [GELF](http://www.graylog2.org/resources/gelf) format. 

## Passing Custom Values to a Layout
Even though the layout renderers provide many pre-defined values, you may need to pass application specific values to your [Layouts](Layouts). You can pass your own values in code by adding custom properties to the event. You then retrieve the value using the [${event-properties}](Event-Context-Layout-Renderer) renderer. See the documentation for the [${event-properties}](Event-Context-Layout-Renderer) for an example.