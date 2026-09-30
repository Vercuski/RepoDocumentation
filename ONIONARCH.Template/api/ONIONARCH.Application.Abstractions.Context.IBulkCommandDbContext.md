# <a id="ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext"></a> Interface IBulkCommandDbContext

Namespace: [ONIONARCH.Application.Abstractions.Context](ONIONARCH.Application.Abstractions.Context.md)  
Assembly: ONIONARCH.Application.dll  

Write-side port for bulk operations on the EF Core persistence path. Defined in Application and
implemented in Persistence, so command handlers can write many rows in a few round trips without
depending on EF Core or on the bulk library behind it.

```csharp
public interface IBulkCommandDbContext
```

## Remarks

<p>
Two kinds of operation are offered:
</p>
<ul><li><b>Entity-list operations</b> ([IBulkCommandDbContext.BulkInsertAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_BulkInsertAsync__1_System_Collections_Generic_IReadOnlyCollection___0__System_Boolean_System_Threading_CancellationToken_), [IBulkCommandDbContext.BulkUpdateAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_BulkUpdateAsync__1_System_Collections_Generic_IReadOnlyCollection___0__System_Threading_CancellationToken_),
  [IBulkCommandDbContext.BulkDeleteAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_BulkDeleteAsync__1_System_Collections_Generic_IReadOnlyCollection___0__System_Threading_CancellationToken_), [IBulkCommandDbContext.BulkUpsertAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_BulkUpsertAsync__1_System_Collections_Generic_IReadOnlyCollection___0__System_Boolean_System_Threading_CancellationToken_)) take the entities to write and
  match existing rows by primary key. They load the data through the platform's bulk-copy mechanism.
  Not every database platform supports them; see the exception documentation.</li><li><b>Set-based operations</b> ([IBulkCommandDbContext.UpdateWhereAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_UpdateWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Action_ONIONARCH_Application_Abstractions_Context_IBulkUpdateSetters___0___System_Threading_CancellationToken_), [IBulkCommandDbContext.DeleteWhereAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_DeleteWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Threading_CancellationToken_))
  take a predicate and issue a single <code>UPDATE</code> or <code>DELETE</code> without loading any entities. They work
  on every platform.</li></ul>
<p>
Every method executes immediately and bypasses the change tracker: nothing is staged, entities already
tracked in the same scope are not refreshed (a later save can overwrite a bulk write with stale values),
and concurrency tokens are not checked. Avoid mixing tracked and bulk writes to the same rows.
</p>
<p>
All methods share the scoped command connection, so they enlist in a transaction begun through
[IUnitOfWork.BeginTransactionAsync](ONIONARCH.Application.Abstractions.IUnitOfWork.md#ONIONARCH_Application_Abstractions_IUnitOfWork_BeginTransactionAsync_System_Threading_CancellationToken_). Without one, each call is atomic on its own.
</p>

## Methods

### <a id="ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_BulkDeleteAsync__1_System_Collections_Generic_IReadOnlyCollection___0__System_Threading_CancellationToken_"></a> BulkDeleteAsync<TEntity\>\(IReadOnlyCollection<TEntity\>, CancellationToken\)

Deletes the rows matching <code class="paramref">entities</code> by primary key. Entities with no matching row
are ignored. Only the keys need to be populated.

```csharp
Task BulkDeleteAsync<TEntity>(IReadOnlyCollection<TEntity> entities, CancellationToken cancellationToken = default) where TEntity : Entity
```

#### Parameters

`entities` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<TEntity\>

The entities whose rows should be deleted. An empty collection is a no-op.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when the delete has finished.

#### Type Parameters

`TEntity` 

The domain entity type.

#### Exceptions

 [NotSupportedException](https://learn.microsoft.com/dotnet/api/system.notsupportedexception)

The command database platform does not support entity-list bulk operations.

### <a id="ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_BulkInsertAsync__1_System_Collections_Generic_IReadOnlyCollection___0__System_Boolean_System_Threading_CancellationToken_"></a> BulkInsertAsync<TEntity\>\(IReadOnlyCollection<TEntity\>, bool, CancellationToken\)

Inserts <code class="paramref">entities</code> using the platform's bulk-copy mechanism.

```csharp
Task BulkInsertAsync<TEntity>(IReadOnlyCollection<TEntity> entities, bool retrieveGeneratedKeys = false, CancellationToken cancellationToken = default) where TEntity : Entity
```

#### Parameters

`entities` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<TEntity\>

The entities to insert. An empty collection is a no-op.

`retrieveGeneratedKeys` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

When <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a>, store-generated keys (identity/serial columns) are read back into the
entities. This costs an extra step (a staging table on SQL Server), so leave it off unless the
caller needs the keys.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when every entity has been inserted.

#### Type Parameters

`TEntity` 

The domain entity type.

#### Exceptions

 [NotSupportedException](https://learn.microsoft.com/dotnet/api/system.notsupportedexception)

The command database platform does not support entity-list bulk operations.

### <a id="ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_BulkUpdateAsync__1_System_Collections_Generic_IReadOnlyCollection___0__System_Threading_CancellationToken_"></a> BulkUpdateAsync<TEntity\>\(IReadOnlyCollection<TEntity\>, CancellationToken\)

Updates the rows matching <code class="paramref">entities</code> by primary key, writing every non-key column
from each entity. Entities with no matching row are ignored.

```csharp
Task BulkUpdateAsync<TEntity>(IReadOnlyCollection<TEntity> entities, CancellationToken cancellationToken = default) where TEntity : Entity
```

#### Parameters

`entities` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<TEntity\>

The entities carrying the keys and new values. An empty collection is a no-op.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when the update has finished.

#### Type Parameters

`TEntity` 

The domain entity type.

#### Exceptions

 [NotSupportedException](https://learn.microsoft.com/dotnet/api/system.notsupportedexception)

The command database platform does not support entity-list bulk operations.

### <a id="ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_BulkUpsertAsync__1_System_Collections_Generic_IReadOnlyCollection___0__System_Boolean_System_Threading_CancellationToken_"></a> BulkUpsertAsync<TEntity\>\(IReadOnlyCollection<TEntity\>, bool, CancellationToken\)

Inserts or updates <code class="paramref">entities</code> by primary key: rows that exist are updated, the rest
are inserted.

```csharp
Task BulkUpsertAsync<TEntity>(IReadOnlyCollection<TEntity> entities, bool retrieveGeneratedKeys = false, CancellationToken cancellationToken = default) where TEntity : Entity
```

#### Parameters

`entities` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<TEntity\>

The entities to write. An empty collection is a no-op.

`retrieveGeneratedKeys` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

When <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a>, keys generated for inserted rows are read back into the entities.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when every entity has been written.

#### Type Parameters

`TEntity` 

The domain entity type.

#### Exceptions

 [NotSupportedException](https://learn.microsoft.com/dotnet/api/system.notsupportedexception)

The command database platform does not support entity-list bulk operations.

### <a id="ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_DeleteWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Threading_CancellationToken_"></a> DeleteWhereAsync<TEntity\>\(Expression<Func<TEntity, bool\>\>, CancellationToken\)

Deletes every row matching <code class="paramref">predicate</code> with a single set-based <code>DELETE</code>
statement. No entities are loaded.

```csharp
Task<int> DeleteWhereAsync<TEntity>(Expression<Func<TEntity, bool>> predicate, CancellationToken cancellationToken = default) where TEntity : Entity
```

#### Parameters

`predicate` [Expression](https://learn.microsoft.com/dotnet/api/system.linq.expressions.expression\-1)<[Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<TEntity, [bool](https://learn.microsoft.com/dotnet/api/system.boolean)\>\>

Selects the rows to delete. It must be translatable to SQL.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of rows deleted.

#### Type Parameters

`TEntity` 

The domain entity type.

### <a id="ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_UpdateWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Action_ONIONARCH_Application_Abstractions_Context_IBulkUpdateSetters___0___System_Threading_CancellationToken_"></a> UpdateWhereAsync<TEntity\>\(Expression<Func<TEntity, bool\>\>, Action<IBulkUpdateSetters<TEntity\>\>, CancellationToken\)

Updates every row matching <code class="paramref">predicate</code> with a single set-based <code>UPDATE</code>
statement. No entities are loaded.

```csharp
Task<int> UpdateWhereAsync<TEntity>(Expression<Func<TEntity, bool>> predicate, Action<IBulkUpdateSetters<TEntity>> setters, CancellationToken cancellationToken = default) where TEntity : Entity
```

#### Parameters

`predicate` [Expression](https://learn.microsoft.com/dotnet/api/system.linq.expressions.expression\-1)<[Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<TEntity, [bool](https://learn.microsoft.com/dotnet/api/system.boolean)\>\>

Selects the rows to update. It must be translatable to SQL.

`setters` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<[IBulkUpdateSetters](ONIONARCH.Application.Abstractions.Context.IBulkUpdateSetters\-1.md)<TEntity\>\>

Declares the columns to set and their new values. At least one is required.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of rows updated.

#### Type Parameters

`TEntity` 

The domain entity type.

#### Examples

<pre><code class="lang-csharp">await bulk.UpdateWhereAsync&lt;Order&gt;(
    o =&gt; o.Status == OrderStatus.Pending &amp;&amp; o.CreatedUtc &lt; cutoff,
    set =&gt; set
        .Set(o =&gt; o.Status, OrderStatus.Expired)            // constant value
        .Set(o =&gt; o.RetryCount, o =&gt; o.RetryCount + 1),    // computed from the current row
    cancellationToken);</code></pre>

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

<code class="paramref">setters</code> declares no assignment.

