# <a id="ONIONARCH_Persistence_Options_ConnectionStringOptions"></a> Class ConnectionStringOptions

Namespace: [ONIONARCH.Persistence.Options](ONIONARCH.Persistence.Options.md)  
Assembly: ONIONARCH.Persistence.dll  

Connection strings for the query and command databases, bound from the
<code>ConnectionStrings</code> configuration section.

```csharp
public sealed record ConnectionStringOptions : IBaseOptionsConfig, IEquatable<ConnectionStringOptions>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ConnectionStringOptions](ONIONARCH.Persistence.Options.ConnectionStringOptions.md)

#### Implements

IBaseOptionsConfig, 
[IEquatable<ConnectionStringOptions\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="ONIONARCH_Persistence_Options_ConnectionStringOptions_CommandDbConnection"></a> CommandDbConnection

Gets or sets the connection string for the write (command) database.

```csharp
public string CommandDbConnection { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="ONIONARCH_Persistence_Options_ConnectionStringOptions_QueryDbConnection"></a> QueryDbConnection

Gets or sets the connection string for the read (query) database.

```csharp
public string QueryDbConnection { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="ONIONARCH_Persistence_Options_ConnectionStringOptions_Section"></a> Section

Gets the name of the configuration section (e.g. in <code>appsettings.json</code>) that this
options type is bound from.

```csharp
public string Section { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

