# <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Persistence_Contexts"></a> Namespace Vertical\_Slice\_Clean\_Architecture.Infrastructure.Persistence.Contexts

### Classes

 [BaseDbContext<TContext\>](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Persistence.Contexts.BaseDbContext\-1.md)

The EF Core model shared by [CommandDbContext](Vertical_Slice_Clean_Architecture.Infrastructure.Persistence.Contexts.CommandDbContext.md) and [QueryDbContext](Vertical_Slice_Clean_Architecture.Infrastructure.Persistence.Contexts.QueryDbContext.md).
Declare entity sets here so both sides of the CQRS split map the same schema.

 [CommandDbContext](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Persistence.Contexts.CommandDbContext.md)

EF Core context for the write side, connected through <code>ConnectionStrings:CommandDbConnection</code>.
Slices that change data add, update or remove entities here and call <code>SaveChangesAsync</code>.

 [QueryDbContext](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Persistence.Contexts.QueryDbContext.md)

EF Core context for the read side, connected through <code>ConnectionStrings:QueryDbConnection</code>.

