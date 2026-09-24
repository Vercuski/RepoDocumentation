# <a id="ONIONARCH_Persistence_Providers_MySQLDatabaseProvider"></a> Class MySQLDatabaseProvider

Namespace: [ONIONARCH.Persistence.Providers](ONIONARCH.Persistence.Providers.md)  
Assembly: ONIONARCH.Persistence.dll  

[IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md) for MySQL. Uses the MySql.EntityFrameworkCore provider for
EF Core and MySqlConnector for Dapper connections.

```csharp
public sealed class MySQLDatabaseProvider : IDatabaseProvider
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MySQLDatabaseProvider](ONIONARCH.Persistence.Providers.MySQLDatabaseProvider.md)

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

### <a id="ONIONARCH_Persistence_Providers_MySQLDatabaseProvider_ConfigureEfCore_Microsoft_EntityFrameworkCore_DbContextOptionsBuilder_System_String_"></a> ConfigureEfCore\(DbContextOptionsBuilder, string\)

Configures <code class="paramref">optionsBuilder</code> to use this platform's EF Core provider.

```csharp
public void ConfigureEfCore(DbContextOptionsBuilder optionsBuilder, string connectionString)
```

#### Parameters

`optionsBuilder` [DbContextOptionsBuilder](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontextoptionsbuilder)

The EF Core options builder to configure.

`connectionString` [string](https://learn.microsoft.com/dotnet/api/system.string)

The connection string to use.

### <a id="ONIONARCH_Persistence_Providers_MySQLDatabaseProvider_CreateConnection_System_String_"></a> CreateConnection\(string\)

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

