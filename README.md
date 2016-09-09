# Serilog.Sinks.NUnit

[![Build status](https://ci.appveyor.com/api/projects/status/18wk0i4a58e14wdl/branch/master?svg=true)](https://ci.appveyor.com/project/luk355/serilog-sinks-nunit/branch/master)
[![MyGet CI](https://img.shields.io/myget/luk355-ci/v/Serilog.Sinks.NUnit.svg)](http://myget.org/gallery/luk355-ci)
[![NuGet](https://img.shields.io/nuget/v/Serilog.Sinks.NUnit.svg)](https://www.nuget.org/packages/Serilog.Sinks.NUnit/)

Basic NUnit sink for Serilog. Any log attempts are being displayed in the test output window by default in following format:

```csharp
{Timestamp:yyyy-MM-dd HH:mm:ss} [{Level}] {Message}{NewLine}  {Exception}
```

 Works in Resharper and NUnit console runner as well.

**Package** - [Serilog.Sinks.NUnit](http://nuget.org/packages/serilog.sinks.nunit)

```csharp
var log = new LoggerConfiguration()
	.WriteTo.NUnitOutput()
	.CreateLogger();
```

Issues
--------------------------------
Logging currently does not work in VS Test Adapter as TestContext.Out is not being populated there. 