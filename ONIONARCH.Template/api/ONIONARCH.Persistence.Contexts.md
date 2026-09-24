# <a id="ONIONARCH_Persistence_Contexts"></a> Namespace ONIONARCH.Persistence.Contexts

### Classes

 [BaseDbContext<T\>](ONIONARCH.Persistence.Contexts.BaseDbContext\-1.md)

Shared EF Core model for the command and query contexts. Declare entity sets here so both
sides of the CQRS split map the same schema.

 [CommandDbContext](ONIONARCH.Persistence.Contexts.CommandDbContext.md)

EF Core context for the write side. Implements both [ICommandDbContext](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md) and
[IUnitOfWork](ONIONARCH.Application.Abstractions.IUnitOfWork.md), and both are resolved to the same scoped instance so they share
change tracking within a request.

 [QueryDbContext](ONIONARCH.Persistence.Contexts.QueryDbContext.md)

EF Core context for the read side, configured for no-tracking queries.

