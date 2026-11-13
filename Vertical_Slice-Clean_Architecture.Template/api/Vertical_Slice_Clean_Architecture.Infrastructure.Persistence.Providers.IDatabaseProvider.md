# <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Persistence_Providers_IDatabaseProvider"></a> Interface IDatabaseProvider

Namespace: [Vertical\_Slice\_Clean\_Architecture.Infrastructure.Persistence.Providers](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Persistence.Providers.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Infrastructure.dll  

Isolates everything that is specific to the database engine, so the rest of the persistence
code (contexts, connection factories, registration) is engine-agnostic.

```csharp
public interface IDatabaseProvider
```

## Remarks

Exactly one implementation is created at startup by <code>PersistenceRegistration</code>.
To move to a different engine, add an implementation for it, reference its ADO.NET driver
(and EF Core provider, if used), and return it from <code>CreateDatabaseProvider</code>.

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Persistence_Providers_IDatabaseProvider_Name"></a> Name

Gets a short, human-readable name for the engine (for example <code>SQL Server</code>), used in
startup and diagnostic messages.

```csharp
string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Persistence_Providers_IDatabaseProvider_ConfigureEfCore_Microsoft_EntityFrameworkCore_DbContextOptionsBuilder_System_String_"></a> ConfigureEfCore\(DbContextOptionsBuilder, string\)

Configures <code class="paramref">optionsBuilder</code> to use this engine's EF Core provider.

```csharp
void ConfigureEfCore(DbContextOptionsBuilder optionsBuilder, string connectionString)
```

#### Parameters

`optionsBuilder` [DbContextOptionsBuilder](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontextoptionsbuilder)

The EF Core options builder to configure.

`connectionString` [string](https://learn.microsoft.com/dotnet/api/system.string)

The connection string to use.

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Persistence_Providers_IDatabaseProvider_CreateConnection_System_String_"></a> CreateConnection\(string\)

Creates a new, unopened ADO.NET connection for this engine.

```csharp
DbConnection CreateConnection(string connectionString)
```

#### Parameters

`connectionString` [string](https://learn.microsoft.com/dotnet/api/system.string)

The connection string to use.

#### Returns

 [DbConnection](https://learn.microsoft.com/dotnet/api/system.data.common.dbconnection)

A new connection. The caller owns it and must dispose it.

#### Remarks

Used by the Dapper connection factories and by the database health check, which opens its
own connections so it never shares one with a request's DbContext.

