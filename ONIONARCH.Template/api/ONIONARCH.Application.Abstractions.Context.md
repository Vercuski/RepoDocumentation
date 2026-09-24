# <a id="ONIONARCH_Application_Abstractions_Context"></a> Namespace ONIONARCH.Application.Abstractions.Context

### Interfaces

 [ICommandDbContext](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md)

Write-side port for the EF Core persistence path. Defined in Application and implemented by
Persistence's <code>CommandDbContext</code>, so command handlers can stage and save changes
without taking a dependency on EF Core types.

 [IQueryDbContext](ONIONARCH.Application.Abstractions.Context.IQueryDbContext.md)

Read-side port for the EF Core persistence path. Defined in Application and implemented by
Persistence's <code>QueryDbContext</code> (configured for no-tracking queries).

