# <a id="ONIONARCH_Application_Abstractions_Context"></a> Namespace ONIONARCH.Application.Abstractions.Context

### Interfaces

 [IBulkCommandDbContext](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md)

Write-side port for bulk operations on the EF Core persistence path. Defined in Application and
implemented in Persistence, so command handlers can write many rows in a few round trips without
depending on EF Core or on the bulk library behind it.

 [IBulkUpdateSetters<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkUpdateSetters\-1.md)

Declares the column assignments of a set-based update issued through
[IBulkCommandDbContext.UpdateWhereAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_UpdateWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Action_ONIONARCH_Application_Abstractions_Context_IBulkUpdateSetters___0___System_Threading_CancellationToken_). Each call adds one <code>SET</code> clause.

 [ICommandDbContext](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md)

Write-side port for the EF Core persistence path. Defined in Application and implemented by
Persistence's <code>CommandDbContext</code>, so command handlers can stage and save changes
without taking a dependency on EF Core types.

 [IQueryDbContext](ONIONARCH.Application.Abstractions.Context.IQueryDbContext.md)

Read-side port for the EF Core persistence path. Defined in Application and implemented by
Persistence's <code>QueryDbContext</code> (configured for no-tracking queries).

