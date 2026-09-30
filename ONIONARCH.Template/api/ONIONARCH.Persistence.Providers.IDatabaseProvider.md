# <a id="ONIONARCH_Persistence_Providers_IDatabaseProvider"></a> Interface IDatabaseProvider

Namespace: [ONIONARCH.Persistence.Providers](ONIONARCH.Persistence.Providers.md)  
Assembly: ONIONARCH.Persistence.dll  

Abstracts a database platform so the EF Core and Dapper paths can be pointed at any supported
platform through configuration alone. Implemented by the provider-specific projects
(ONIONARCH.Persistence.SqlServer, .PostgreSql, .MySql); this core project owns the contract but
never references a concrete provider. Hosts opt providers in through
[DatabaseProviderRegistry](ONIONARCH.Persistence.Providers.DatabaseProviderRegistry.md).

```csharp
public interface IDatabaseProvider
```

## Properties

### <a id="ONIONARCH_Persistence_Providers_IDatabaseProvider_Platform"></a> Platform

The platform key matched, case-insensitively, against the <code>QueryDbPlatform</code> and
<code>CommandDbPlatform</code> values of the <code>DatabasePlatform</code> configuration section
(e.g. <code>MSSQL</code>, <code>PostgreSQL</code>, <code>MySQL</code>).

```csharp
string Platform { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="ONIONARCH_Persistence_Providers_IDatabaseProvider_SupportsBulkOperations"></a> SupportsBulkOperations

Gets a value indicating whether this platform supports the entity-list bulk operations of
<code>IBulkCommandDbContext</code> (insert, update, delete, upsert). They are implemented with
EFCore.BulkExtensions, which needs a platform adapter package; a provider returns
<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a> only when its project references that adapter. Set-based
<code>UpdateWhereAsync</code>/<code>DeleteWhereAsync</code> use EF Core itself and work regardless.

```csharp
bool SupportsBulkOperations { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

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

