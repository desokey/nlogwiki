Writes log messages to the console with customizable coloring. 

Supported in .NET and Mono
##Configuration Syntax
```
<targets>
  <target xsi:type="ColoredConsole"
          name="String"
          layout="Layout"
          header="Layout"
          footer="Layout"
          useDefaultRowHighlightingRules="Boolean"
          errorStream="Boolean">
    <highlight-row backgroundColor="Enum" condition="Condition" foregroundColor="Enum"/><!-- repeated -->
    <highlight-word backgroundColor="Enum" foregroundColor="Enum" ignoreCase="Boolean"
                    regex="String" text="String" wholeWords="Boolean"/><!-- repeated -->
  </target>
</targets>
```
Read more about using the [Configuration File](Configuration file).
##Parameters
###General Options
_name_ - Name of the target.
###Layout Options
_layout_ - Text to be rendered. [Layout](Layout) Required. Default: ${longdate}|${level:uppercase=true}|${logger}|${message}  
_header_ - Header. [Layout](Layout)  
_footer_ - Footer. [Layout](Layout)
###Highlighting Rules
_useDefaultRowHighlightingRules_ - Indicates whether to use default row highlighting rules. [Boolean](Data types) Default: True
The default rules are:
<table>
<thead>
<th>Condition</th><th>Foreground Color</th><th>Background Color</th>
</thead>
<tbody>
<tr>level == LogLevel.Fatal</tr><tr>Red</tr><tr>NoChange</tr>
<tr>level == LogLevel.Error</tr><tr>Yellow</tr><tr>NoChange</tr>
<tr>level == LogLevel.Warn</tr><tr>Magenta</tr><tr>NoChange</tr>
<tr>level == LogLevel.Info</tr><tr>White</tr><tr>NoChange</tr>
<tr>level == LogLevel.Debug</tr><tr>Gray</tr><tr>NoChange</tr>
<tr>level == LogLevel.Trace</tr><tr>DarkGray</tr><tr>NoChange</tr>
</tbody>
</table>
_rowHighlightingRules_ - The row highlighting rules. [Collection](Data types)  
Each collection item is represented by \<highlight-row /> element with the following attributes:
  * _backgroundColor_ - Background color. Default: NoChange  
Possible values:
    * Black - Black Color (#000000).
    * Blue - Blue Color (#0000FF).
    * Cyan - Cyan Color (#00FFFF).
    * DarkBlue - Dark blue Color (#000080).
    * DarkCyan - Dark Cyan Color (#008080).
    * DarkGray - Dark Gray Color (#808080).
    * DarkGreen - Dark green Color (#008000).
    * DarkMagenta - Dark Magenta Color (#800080).
    * DarkRed - Dark Red Color (#800000).
    * DarkYellow - Dark Yellow Color (#808000).
    * Gray - Gray Color (#C0C0C0).
    * Green - Green Color (#00FF00).
    * Magenta - Magenta Color (#FF00FF).
    * NoChange - Don't change the color.
    * Red - Red Color (#FF0000).
    * White - White Color (#FFFFFF).
    * Yellow - Yellow Color (#FFFF00).

_condition_ - Condition that must be met in order to set the specified foreground and background color. [Condition](Data types) Required.  

_foregroundColor_ - Foreground color. Default: NoChange  
Possible values:
* Black - Black Color (#000000).
* Blue - Blue Color (#0000FF).
* Cyan - Cyan Color (#00FFFF).
* DarkBlue - Dark blue Color (#000080).
* DarkCyan - Dark Cyan Color (#008080).
* DarkGray - Dark Gray Color (#808080).
* DarkGreen - Dark green Color (#008000).
* DarkMagenta - Dark Magenta Color (#800080).
* DarkRed - Dark Red Color (#800000).
* DarkYellow - Dark Yellow Color (#808000).
* Gray - Gray Color (#C0C0C0).
* Green - Green Color (#00FF00).
* Magenta - Magenta Color (#FF00FF).
* NoChange - Don't change the color.
* Red - Red Color (#FF0000).
* White - White Color (#FFFFFF).
* Yellow - Yellow Color (#FFFF00).

_wordHighlightingRules_ - The word highlighting rules. [Collection](Data types)  
Each collection item is represented by \<highlight-word /> element with the following attributes:
* _backgroundColor_ - Background color. Default: NoChange  
Possible values:
   * Black - Black Color (#000000).
   * Blue - Blue Color (#0000FF).
   * Cyan - Cyan Color (#00FFFF).
   * DarkBlue - Dark blue Color (#000080).
   * DarkCyan - Dark Cyan Color (#008080).
   * DarkGray - Dark Gray Color (#808080).
   * DarkGreen - Dark green Color (#008000).
   * DarkMagenta - Dark Magenta Color (#800080).
   * DarkRed - Dark Red Color (#800000).
   * DarkYellow - Dark Yellow Color (#808000).
   * Gray - Gray Color (#C0C0C0).
   * Green - Green Color (#00FF00).
   * Magenta - Magenta Color (#FF00FF).
   * NoChange - Don't change the color.
   * Red - Red Color (#FF0000).
   * White - White Color (#FFFFFF).
   * Yellow - Yellow Color (#FFFF00).

_foregroundColor_ - Foreground color. Default: NoChange  
Possible values:
* Black - Black Color (#000000).
* Blue - Blue Color (#0000FF).
* Cyan - Cyan Color (#00FFFF).
* DarkBlue - Dark blue Color (#000080).
* DarkCyan - Dark Cyan Color (#008080).
* DarkGray - Dark Gray Color (#808080).
* DarkGreen - Dark green Color (#008000).
* DarkMagenta - Dark Magenta Color (#800080).
* DarkRed - Dark Red Color (#800000).
* DarkYellow - Dark Yellow Color (#808000).
* Gray - Gray Color (#C0C0C0).
* Green - Green Color (#00FF00).
* Magenta - Magenta Color (#FF00FF).
* NoChange - Don't change the color.
* Red - Red Color (#FF0000).
* White - White Color (#FFFFFF).
* Yellow - Yellow Color (#FFFF00).

_ignoreCase_ - Indicates whether to ignore case when comparing texts. [Boolean](Data types) Default: False  
_regex_ - Regular expression to be matched. You must specify either text or regex.  
_text_ - Text to be matched. You must specify either text or regex.  
_wholeWords_ - Indicates whether to match whole words only. [Boolean](Data types) Default: False  

###Output Options
_errorStream_ - Indicates whether the error stream (stderr) should be used instead of the output stream (stdout). [Boolean](Data types) Default: False