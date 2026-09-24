# <a id="ONIONARCH_Persistence_Options_DatabasePlatformOptions"></a> Class DatabasePlatformOptions

Namespace: [ONIONARCH.Persistence.Options](ONIONARCH.Persistence.Options.md)  
Assembly: ONIONARCH.Persistence.dll  

Selects the database platform for each side of the CQRS split, bound from the
<code>DatabasePlatform</code> configuration section. Supported values (case-insensitive):
<code>MSSQL</code>, <code>POSTGRESQL</code>, <code>MYSQL</code>.

```csharp
public sealed record DatabasePlatformOptions : IBaseOptionsConfig, IEquatable<DatabasePlatformOptions>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DatabasePlatformOptions](ONIONARCH.Persistence.Options.DatabasePlatformOptions.md)

#### Implements

IBaseOptionsConfig, 
[IEquatable<DatabasePlatformOptions\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="ONIONARCH_Persistence_Options_DatabasePlatformOptions_CommandDbPlatform"></a> CommandDbPlatform

Gets or sets the platform of the write (command) database.

```csharp
public string CommandDbPlatform { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="ONIONARCH_Persistence_Options_DatabasePlatformOptions_QueryDbPlatform"></a> QueryDbPlatform

Gets or sets the platform of the read (query) database.

```csharp
public string QueryDbPlatform { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="ONIONARCH_Persistence_Options_DatabasePlatformOptions_Section"></a> Section

Gets the name of the configuration section (e.g. in <code>appsettings.json</code>) that this
options type is bound from.

```csharp
public string Section { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

