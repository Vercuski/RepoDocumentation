# <a id="ONIONARCH_Persistence_Providers_SqlServerDatabaseProvider"></a> Class SqlServerDatabaseProvider

Namespace: [ONIONARCH.Persistence.Providers](ONIONARCH.Persistence.Providers.md)  
Assembly: ONIONARCH.Persistence.dll  

[IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md) for Microsoft SQL Server, using Microsoft.Data.SqlClient for
both EF Core and Dapper connections.

```csharp
public sealed class SqlServerDatabaseProvider : IDatabaseProvider
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SqlServerDatabaseProvider](ONIONARCH.Persistence.Providers.SqlServerDatabaseProvider.md)

#### Implements

[IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="ONIONARCH_Persistence_Providers_SqlServerDatabaseProvider_ConfigureEfCore_Microsoft_EntityFrameworkCore_DbContextOptionsBuilder_System_String_"></a> ConfigureEfCore\(DbContextOptionsBuilder, string\)

Configures <code class="paramref">optionsBuilder</code> to use this platform's EF Core provider.

```csharp
public void ConfigureEfCore(DbContextOptionsBuilder optionsBuilder, string connectionString)
```

#### Parameters

`optionsBuilder` [DbContextOptionsBuilder](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontextoptionsbuilder)

The EF Core options builder to configure.

`connectionString` [string](https://learn.microsoft.com/dotnet/api/system.string)

The connection string to use.

### <a id="ONIONARCH_Persistence_Providers_SqlServerDatabaseProvider_CreateConnection_System_String_"></a> CreateConnection\(string\)

Creates a new, unopened ADO.NET connection for this platform.

```csharp
public IDbConnection CreateConnection(string connectionString)
```

#### Parameters

`connectionString` [string](https://learn.microsoft.com/dotnet/api/system.string)

The connection string to use.

#### Returns

 [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection)

A new connection; the caller owns it and must dispose it.

