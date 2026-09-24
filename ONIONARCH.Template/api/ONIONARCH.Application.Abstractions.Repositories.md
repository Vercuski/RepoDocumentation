# <a id="ONIONARCH_Application_Abstractions_Repositories"></a> Namespace ONIONARCH.Application.Abstractions.Repositories

### Interfaces

 [ISampleEntityDapperCommandRepository](ONIONARCH.Application.Abstractions.Repositories.ISampleEntityDapperCommandRepository.md)

Write-side port for the Dapper persistence path. Defined in Application, implemented in
Persistence — mirrors [ICommandDbContext](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md) for the EF Core path so that
Application never depends on Dapper, raw SQL, or [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection).

 [ISampleEntityDapperQueryRepository](ONIONARCH.Application.Abstractions.Repositories.ISampleEntityDapperQueryRepository.md)

Read-side port for the Dapper persistence path. Defined in Application, implemented in
Persistence — mirrors [IQueryDbContext](ONIONARCH.Application.Abstractions.Context.IQueryDbContext.md) for the EF Core path so that
Application never depends on Dapper, raw SQL, or [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection).

