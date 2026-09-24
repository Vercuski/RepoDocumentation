# <a id="ONIONARCH_Persistence_ConnectionFactory_DbReadOnlyConnectionFactory"></a> Class DbReadOnlyConnectionFactory

Namespace: [ONIONARCH.Persistence.ConnectionFactory](ONIONARCH.Persistence.ConnectionFactory.md)  
Assembly: ONIONARCH.Persistence.dll  

Creates connections to the query database using
[ConnectionStringOptions.QueryDbConnection](ONIONARCH.Persistence.Options.ConnectionStringOptions.md#ONIONARCH_Persistence_Options_ConnectionStringOptions_QueryDbConnection) and the configured query-side
[IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md).

```csharp
public sealed class DbReadOnlyConnectionFactory : IDbReadOnlyConnectionFactory
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DbReadOnlyConnectionFactory](ONIONARCH.Persistence.ConnectionFactory.DbReadOnlyConnectionFactory.md)

#### Implements

IDbReadOnlyConnectionFactory

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Persistence_ConnectionFactory_DbReadOnlyConnectionFactory__ctor_Microsoft_Extensions_Options_IOptions_ONIONARCH_Persistence_Options_ConnectionStringOptions__ONIONARCH_Persistence_Providers_IDatabaseProvider_"></a> DbReadOnlyConnectionFactory\(IOptions<ConnectionStringOptions\>, IDatabaseProvider\)

Creates connections to the query database using
[ConnectionStringOptions.QueryDbConnection](ONIONARCH.Persistence.Options.ConnectionStringOptions.md#ONIONARCH_Persistence_Options_ConnectionStringOptions_QueryDbConnection) and the configured query-side
[IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md).

```csharp
public DbReadOnlyConnectionFactory(IOptions<ConnectionStringOptions> connectionStringOptions, IDatabaseProvider databaseProvider)
```

#### Parameters

`connectionStringOptions` [IOptions](https://learn.microsoft.com/dotnet/api/microsoft.extensions.options.ioptions\-1)<[ConnectionStringOptions](ONIONARCH.Persistence.Options.ConnectionStringOptions.md)\>

The bound connection string settings.

`databaseProvider` [IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md)

The provider for the configured query database platform.

## Methods

### <a id="ONIONARCH_Persistence_ConnectionFactory_DbReadOnlyConnectionFactory_CreateConnection"></a> CreateConnection\(\)

Creates a new, unopened connection to the query database using the configured
provider and connection string.

```csharp
public IDbConnection CreateConnection()
```

#### Returns

 [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection)

A new [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection); the caller owns it and must dispose it.

