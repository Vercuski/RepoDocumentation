# <a id="ONIONARCH_Application_Abstractions_Context_IQueryDbContext"></a> Interface IQueryDbContext

Namespace: [ONIONARCH.Application.Abstractions.Context](ONIONARCH.Application.Abstractions.Context.md)  
Assembly: ONIONARCH.Application.dll  

Read-side port for the EF Core persistence path. Defined in Application and implemented by
Persistence's <code>QueryDbContext</code> (configured for no-tracking queries).

```csharp
public interface IQueryDbContext
```

## Remarks

Exposes [IQueryable](https://learn.microsoft.com/dotnet/api/system.linq.iqueryable-1) rather than EF Core's <code>DbSet&lt;T&gt;</code> so the
Application layer never references EF Core. Because EF Core's async LINQ operators live in
EF Core itself, the async materialization methods are surfaced here instead
([IQueryDbContext.ToListAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IQueryDbContext.md#ONIONARCH_Application_Abstractions_Context_IQueryDbContext_ToListAsync__1_System_Linq_IQueryable___0__System_Threading_CancellationToken_), [IQueryDbContext.SingleOrDefaultAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IQueryDbContext.md#ONIONARCH_Application_Abstractions_Context_IQueryDbContext_SingleOrDefaultAsync__1_System_Linq_IQueryable___0__System_Threading_CancellationToken_)).

## Methods

### <a id="ONIONARCH_Application_Abstractions_Context_IQueryDbContext_Set__1"></a> Set<TEntity\>\(\)

Returns a composable query over all entities of type <code class="typeparamref">TEntity</code>.

```csharp
IQueryable<TEntity> Set<TEntity>() where TEntity : Entity
```

#### Returns

 [IQueryable](https://learn.microsoft.com/dotnet/api/system.linq.iqueryable\-1)<TEntity\>

An [IQueryable](https://learn.microsoft.com/dotnet/api/system.linq.iqueryable-1) that can be further filtered and projected before execution.

#### Type Parameters

`TEntity` 

The domain entity type to query.

### <a id="ONIONARCH_Application_Abstractions_Context_IQueryDbContext_SingleOrDefaultAsync__1_System_Linq_IQueryable___0__System_Threading_CancellationToken_"></a> SingleOrDefaultAsync<TEntity\>\(IQueryable<TEntity\>, CancellationToken\)

Asynchronously executes <code class="paramref">query</code> and returns its single result, or
<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a> if it matched nothing.

```csharp
Task<TEntity?> SingleOrDefaultAsync<TEntity>(IQueryable<TEntity> query, CancellationToken cancellationToken = default) where TEntity : Entity
```

#### Parameters

`query` [IQueryable](https://learn.microsoft.com/dotnet/api/system.linq.iqueryable\-1)<TEntity\>

A query obtained from [IQueryDbContext.Set<TEntity\>](ONIONARCH.Application.Abstractions.Context.IQueryDbContext.md#ONIONARCH_Application_Abstractions_Context_IQueryDbContext_Set__1).

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<TEntity?\>

The matching entity, or <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a> if none was found.

#### Type Parameters

`TEntity` 

The domain entity type.

#### Exceptions

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

The query matched more than one entity.

### <a id="ONIONARCH_Application_Abstractions_Context_IQueryDbContext_ToListAsync__1_System_Linq_IQueryable___0__System_Threading_CancellationToken_"></a> ToListAsync<TEntity\>\(IQueryable<TEntity\>, CancellationToken\)

Asynchronously executes <code class="paramref">query</code> and materializes the results into a list.

```csharp
Task<List<TEntity>> ToListAsync<TEntity>(IQueryable<TEntity> query, CancellationToken cancellationToken = default) where TEntity : Entity
```

#### Parameters

`query` [IQueryable](https://learn.microsoft.com/dotnet/api/system.linq.iqueryable\-1)<TEntity\>

A query obtained from [IQueryDbContext.Set<TEntity\>](ONIONARCH.Application.Abstractions.Context.IQueryDbContext.md#ONIONARCH_Application_Abstractions_Context_IQueryDbContext_Set__1).

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<TEntity\>\>

A list containing every entity matched by the query (empty if none).

#### Type Parameters

`TEntity` 

The domain entity type.

