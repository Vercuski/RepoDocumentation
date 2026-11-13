# <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Persistence_Options_ConnectionStringOptions"></a> Class ConnectionStringOptions

Namespace: [Vertical\_Slice\_Clean\_Architecture.Infrastructure.Persistence.Options](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Persistence.Options.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Infrastructure.dll  

Connection strings for the read (query) and write (command) sides of the CQRS split, bound from
the <code>ConnectionStrings</code> configuration section.

```csharp
public sealed record ConnectionStringOptions : IBaseOptionsConfig, IEquatable<ConnectionStringOptions>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ConnectionStringOptions](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Persistence.Options.ConnectionStringOptions.md)

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

## Remarks

Both values are required and are validated when the host starts, so a missing connection string
fails immediately rather than on the first database call. The two sides may point at the same
database; split them when reads should go to a replica.

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Persistence_Options_ConnectionStringOptions_CommandDbConnection"></a> CommandDbConnection

Gets or sets the connection string for the write (command) database.

```csharp
[Required(AllowEmptyStrings = false)]
public string CommandDbConnection { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Persistence_Options_ConnectionStringOptions_QueryDbConnection"></a> QueryDbConnection

Gets or sets the connection string for the read (query) database.

```csharp
[Required(AllowEmptyStrings = false)]
public string QueryDbConnection { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Persistence_Options_ConnectionStringOptions_Section"></a> Section

Gets the name of the configuration section (for example in <code>appsettings.json</code>)
that this options type is bound from.

```csharp
public string Section { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

