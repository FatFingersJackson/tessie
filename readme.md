# Tesseract application
## With C# and C++ 

### !In progress!




## Please note!
- c++ fails to create tesseract object if the locale is not set to C. It looks somethin like this:
  
  ```
   !strcmp(locale, "C"):Error:Assert failed:in file [path_here]/tesseract-master/src/api/baseapi.cpp, line 209
  
    Stacktrace:

  at <unknown> <0xffffffff>
  at (wrapper managed-to-native) Program.GetString (string,byte[],int&) [0x00013] in <f57349ea9aa349a1aea438143a8d28d3>:0
  at Program.getManagedString () [0x00054] in <f57349ea9aa349a1aea438143a8d28d3>:0
  at Program.Main () [0x0000a] in <f57349ea9aa349a1aea438143a8d28d3>:0
  at (wrapper runtime-invoke) object.runtime_invoke_void (object,intptr,intptr,intptr) [0x0004c] in <98fac219bd4e453693d76fda7bd96ab0>:0

    Unhandled Exception:
    System.NullReferenceException: Object reference not set to an instance of an object
  at (wrapper managed-to-native) Program.GetString(string,byte[],int&)
  at Program.getManagedString () [0x00054] in <f57349ea9aa349a1aea438143a8d28d3>:0
  at Program.Main () [0x0000a] in <f57349ea9aa349a1aea438143a8d28d3>:0
    [ERROR] FATAL UNHANDLED EXCEPTION: System.NullReferenceException: Object reference not set to an instance ofan object
  at (wrapper managed-to-native) Program.GetString(string,byte[],int&)
  at Program.getManagedString () [0x00054] in <f57349ea9aa349a1aea438143a8d28d3>:0
  at Program.Main () [0x0000a] in <f57349ea9aa349a1aea438143a8d28d3>:0
    ```
    That was sorted out by export LC_ALL=C, but needs a proper fixing. 
