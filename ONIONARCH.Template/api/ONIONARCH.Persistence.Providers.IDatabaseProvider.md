# <a id="ONIONARCH_Persistence_Providers_IDatabaseProvider"></a> Interface IDatabaseProvider

Namespace: [ONIONARCH.Persistence.Providers](ONIONARCH.Persistence.Providers.md)  
Assembly: ONIONARCH.Persistence.dll  

Abstracts a database platform (SQL Server, PostgreSQL, MySQL) so the EF Core and Dapper paths
can be pointed at any supported platform through configuration alone.

```csharp
public interface IDatabaseProvider
```

## Methods

### <a id="ONIONARCH_Persistence_Providers_IDatabaseProvider_ConfigureEfCore_Microsoft_EntityFrameworkCore_DbContextOptionsBuilder_System_String_"></a> ConfigureEfCore\(DbContextOptionsBuilder, string\)

Configures <code class="paramref">optionsBuilder</code> to use this platform's EF Core provider.

```csharp
void ConfigureEfCore(DbContextOptionsBuilder optionsBuilder, string connectionString)
```

#### Parameters

`optionsBuilder` [DbContextOptionsBuilder](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontextoptionsbuilder)

The EF Core options builder to configure.

`connectionString` [string](https://learn.microsoft.com/dotnet/api/system.string)

The connection string to use.

### <a id="ONIONARCH_Persistence_Providers_IDatabaseProvider_CreateConnection_System_String_"></a> CreateConnection\(string\)

Creates a new, unopened ADO.NET connection for this platform.

```csharp
IDbConnection CreateConnection(string connectionString)
```

#### Parameters

`connectionString` [string](https://learn.microsoft.com/dotnet/api/system.string)

The connection string to use.

#### Returns

 [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection)

A new connection; the caller owns it and must dispose it.

