# <a id="ONIONARCH_Application_Abstractions_ConnectionFactory_IDbWriteConnectionFactory"></a> Interface IDbWriteConnectionFactory

Namespace: [ONIONARCH.Application.Abstractions.ConnectionFactory](ONIONARCH.Application.Abstractions.ConnectionFactory.md)  
Assembly: ONIONARCH.Application.dll  

Creates ADO.NET connections to the write (command) database.

```csharp
public interface IDbWriteConnectionFactory
```

## Remarks

Consumed only by Persistence-layer Dapper command repositories. Request handlers must not
depend on this factory directly — the architecture fitness tests require command handlers to
take [ICommandDbContext](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md) or a command repository port instead, so raw SQL
never runs inside the Application layer.

## Methods

### <a id="ONIONARCH_Application_Abstractions_ConnectionFactory_IDbWriteConnectionFactory_CreateConnection"></a> CreateConnection\(\)

Creates a new, unopened connection to the command database using the configured
provider and connection string.

```csharp
IDbConnection CreateConnection()
```

#### Returns

 [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection)

A new [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection); the caller owns it and must dispose it.

