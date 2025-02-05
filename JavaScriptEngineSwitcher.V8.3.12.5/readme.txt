﻿

   --------------------------------------------------------------------------------
                    README file for JS Engine Switcher: V8 v3.12.5

   --------------------------------------------------------------------------------

      Copyright (c) 2013-2021 Andrey Taritsyn - http://www.taritsyn.ru


   ===========
   DESCRIPTION
   ===========
   JavaScriptEngineSwitcher.V8 contains adapter `V8JsEngine` (wrapper for the
   Microsoft ClearScript.V8 (http://github.com/Microsoft/ClearScript) version
   7.1.5).

   This package does not contain the native ClearScript.V8 assemblies.
   Therefore, you need to choose and install the most appropriate package(s) for
   your platform. The following packages are available:

    * Microsoft.ClearScript.V8.Native.win-x86
    * Microsoft.ClearScript.V8.Native.win-x64
    * Microsoft.ClearScript.V8.Native.win-arm64
    * Microsoft.ClearScript.V8.Native.linux-x64
    * Microsoft.ClearScript.V8.Native.linux-arm
    * Microsoft.ClearScript.V8.Native.linux-arm64
    * Microsoft.ClearScript.V8.Native.osx-x64
    * Microsoft.ClearScript.V8.Native.osx-arm64

   =============
   RELEASE NOTES
   =============
   1. Microsoft ClearScript.V8 was updated to version 7.1.5;
   2. In configuration settings of the V8 JS engine was added one new property -
      `MaxArrayBufferAllocation` (default `UInt64.MaxValue`).

   =============
   DOCUMENTATION
   =============
   See documentation on GitHub -
   http://github.com/Taritsyn/JavaScriptEngineSwitcher