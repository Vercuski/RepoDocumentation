# <a id="ONIONARCH_Application_Abstractions_ConnectionFactory_IDbReadOnlyConnectionFactory"></a> Interface IDbReadOnlyConnectionFactory

Namespace: [ONIONARCH.Application.Abstractions.ConnectionFactory](ONIONARCH.Application.Abstractions.ConnectionFactory.md)  
Assembly: ONIONARCH.Application.dll  

Creates ADO.NET connections to the read (query) database.

```csharp
public interface IDbReadOnlyConnectionFactory
```

## Remarks

Consumed only by Persistence-layer Dapper query repositories. Request handlers must not
depend on this factory directly — the architecture fitness tests require query handlers to
take [IQueryDbContext](ONIONARCH.Application.Abstractions.Context.IQueryDbContext.md) or a query repository port instead, so raw SQL never
runs inside the Application layer.

## Methods

### <a id="ONIONARCH_Application_Abstractions_ConnectionFactory_IDbReadOnlyConnectionFactory_CreateConnection"></a> CreateConnection\(\)

Creates a new, unopened connection to the query database using the configured
provider and connection string.

```csharp
IDbConnection CreateConnection()
```

#### Returns

 [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection)

A new [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection); the caller owns it and must dispose it.

